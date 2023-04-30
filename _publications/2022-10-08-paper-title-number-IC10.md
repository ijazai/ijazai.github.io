---
title: "Quantitative Assessment of the Impact of Lossy JPEG Compression on Deep Learning Models"
collection: publications
permalink: /publication/2022-10-08-paper-title-number-IC10
date: 2022-10-08
venue: 'KINGPC International Conference on Next Generation Computing (ICNGC)'
author_profile: false
---
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<h3>Abstract</h3>
<p>Lossy image compression provides an efficient
solution to the exchange and storage of image data for consumer
applications. The design of lossy algorithms is based on a
principle to discard information that are not perceivable by
human visual system (HVS). With the popularity of deep
learning models (DL) in computer vision (CV), it is necessary to
characterize the loss in image quality with respect to computer
vision systems as well. Recent studies have analyzed the image
distortions resulted from blur and noise, mainly from an
adversarial attack perspective. However, fewer studies have
dealt with the lossy nature of the JPEG algorithm. Therefore,
the current study presents a quantitative assessment of different
types of data loss that occurs due to chroma subsampling,
quantization, and rounding functions of the JPEG algorithm. In
addition, we have analyzed impact of different interpolation
methods that are used for chroma upsampling. The analysis
have shown that for compression savings, performing either
subsampling or quantization preserved the model accuracy
while their combination degraded the accuracy by 6%.</p>

<h3>Contributions</h3>
<ul>
	<li> We present a quantitative assessment of DL-based classifier under the influence of different types of information loss that happens in the JPEG algorithm.</li>
	<li> We consider image quality degradation due to chroma subsampling, quantization, and rounding functions of the JPEG algorithm. </li>
	<li> We analyze three types of interpolation methods (<i>nearest neighbor</i>, <i>bilinear</i>, and <i>bicubic</i> interpolation methods) in the chroma upsampling function.</li>
</ul>

<h3>Lossy Components of the JPEG Algorithm</h3>

<p>
In the JPEG standard, loss of information is a result of sub-sampling (\(H\)), Quantization (\(Q\)), rounding and truncation
functions. The two transformation functions namely, colorspace conversion (\(C_{YCbCr}\) or \(C_{RGB}\)) and DCT function (\(D\)) do not result in any information loss; however, rounding and truncation of their values do. The JPEG compression of a block (\(B_{c}\) is:
</p>


<div style="overflow-x:auto">\[B_{c}=\left[Q\left(D\left(H_{sub}\left(C_{YCbCr}\left(B\right)\right),Qf\right)\right)\right],\]</div>

<p>and the JPEG decompression \(B_{d}\) can be defined as:</p>

<div style="overflow-x:auto">\[B_{d}=\left[C_{RGB}\left(H_{up}\left(\left[D^{-1}\left(Q^{-1}\left(B_{c},Qf\right)\right)\right]\right)\right)\right]\rvert_0^{255}\]</div>

<p>where, \(\left[.\right]\) and \(.\rvert_0^{255}\) rounds and truncates the values to a valid range in the spatial domain, respectively.</p>

<h4>JPEG Chroma Subsampling and Upsampling</h4>
<p>The Human Visual System (HVS) is highly sensitive to changes in brightness than color. The JPEG algorithm exploits this property to achieve better compression savings by storing chroma components with a lower resolution. This process is called subsampling. In the JPEG standard, subsampling in a region (\(4\) pixels wide and \(2\) pixels high) is defined by a three-ratio as \(J:a:b\), where \(J\) is width, \(a\) is number of color samples in first row of \(J\) pixels and \(b\) is the samples between first and second row of \(J\) pixels. The commonly used ratios are \(4:2:2\) and \(4:2:0\). When decoding, the chrominance components are scaled back to original resolution by an upsampling process.<br>

Different types of sub- and upsampling algorithms are available. The straightforward way for sub-sampling is to
calculate the average of the source pixels and assigned it to an output pixel. This technique is named as “<i>simple subsampling</i>”. The area covered by the pixel depends on the subsampling ratio <u> [to-do: add figure] as shown in Fig. (a) and (d)</u> for ratios \(4:2:2\) and \(4:2:0\), respectively. In the first case, only \(1 \times 2\) pixels area is stored whereas, in the second case \(2 \times 2\) pixels area is stored. For an image \(I\) with \(M \times N\) pixels, the down-sampled \(4:2:2\) image \(I\) with \(M \times \left(N/2\right)\) pixels is defined as </p>

<div style="overflow-x:auto">\[\widehat{I}_{\left(s,t\right)}=\frac{I_\left(i,2j-1\right)+I_\left(i,2j\right)}{2}\]</div>

<p>    where \(i,s=1,2,3,\cdot\cdot\cdot,M, j=1,2,3,\cdot\cdot\cdot,N\) and \(t=1,2,3,\cdot\cdot\cdot,N/2\). Similarly, when \(I\) is subsampled with 4:2:0 ratio, then the downsampled image \(I\) has \(\left(M/2\right)\times\left(N/2\right)\) elements and is defined as     </p>

<div style="overflow-x:auto">\[\widehat{I}_{\left(s,t\right)}=\frac{I_\left(2i-1,2j-1\right)+I_\left(2i-1,2j\right)+I_\left(2i,2j-1\right)+I_\left(2i,2j\right)}{4}\]</div>

<p>   here \(s=1,2,3,\cdot\cdot\cdot,M/2\) and varaibles \(i,j,t\) remain the same as stated before. The simple subsampling can be reversed by "<i>simple upsampling</i>", which copies the exact value of each pixel to its closest neighbor pixels as shown in Figure for ratios \(4:2:2\) and \(4:2:0\), respectively. This technique is sometimes referred to as a box filter. Besides simple subsampling, the standard provides more complex upsampling techniques, referred to as "<i>fancy upsampling</i>". The algorithms perform linear interpolation of input pixels and each chrominance pixel is assigned with weight based on its proximity as shown in Figure for \(4:2:2\) and \(4:2:0\) ratios, respectively. In the first case, the nearest pixel is assigned a weight value of \(3/4\) and the furthest pixel is assigned a weight value of \(1/4\). Similarly, in the second case, the weight values \(9/16\), \(3/16\) and \(1/16\) are assigned to the nearest, two orthogonall adjacent, and diagonally adjacent pixels, respectively. both these techniques are sometimes referred to as traingle fliters. <br>

For chroma subsampling ratios other than the mentioned ones, the JPEG uses simple upsampling. The simple upsampling cane regarded as <i>nearest neighbor interpolation</i> method as it assigns the nearest neighbor to value to each new location. This approach is simple and computationally less expensive; however, it results in undesirable artifacts. The fancy upsampling can be performed with <i>bilinear interpolation</i> in which four nearest neighbors are used to estimate a pixel value at a given location. To assign a value \(P\) at a location \(\left(x,y\right)\), bilinear interpolation performs

<div>
\[P_{\left(x,y\right)}=ax+by+cxy+d\]
</div>

The four coefficients are calculated as teh four nearest neighbors of point \(\left(x,y\right)\). The bilinear interpolation results better quality than the nearest neighbor with acceptable computation cost. Another interpolation technique is <i>bicubic interpolation</i>, which takes sixteen nearest neighboring pixels into account. The values of \(P\) at a location \(\left(x,y\right)\) is

<div>
\[P_{\left(x,y\right)}=\sum_{i=0}^{3}\sum_{j=0}^{3}a_{\left(i,j\right)}x^{i}y^{j}\]
</div>

the sixteen coefficient are calculated as the sixteen nearest neighbors of point \(\left(x,y\right)\). Bicubic interpolation preserves finer details than bilinear interpolation with additional computational cost.

</p>


<h3>Conclusion</h3>
This study presented quantitative assessment of the impact that the JPEG compression has on DL-based image classification. The analysis have shown that the quantization of DCT coefficients preserves model accuracy while delivering better compression savings. However, to avoid the computational cost of quantization step, simple chroma subsampling and simple chroma upsampling with the nearest neighbor interpolation can be used, which achieved the same accuracy with a slight degradation in the compression savings.




<br>[Full Article](https://www.earticle.net/Article/A419789)

<h3>Related Articles</h3>
[How to mitigate the JPEG compression artifacts impact on a deep learning model performance?]({{ site.baseurl }}{% link _publications/2023-02-20-paper-title-number-IC15.md %})<br>