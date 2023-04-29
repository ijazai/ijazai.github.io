---
title: "Quantitative Assessment of the Impact of Lossy JPEG Compression on Deep Learning Models"
collection: publications
permalink: /publication/2022-10-08-paper-title-number-IC10
date: 2022-10-08
venue: 'KINGPC International Conference on Next Generation Computing (ICNGC)'
author_profile: false
---
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
	<li> We present a quantitative assessment of DL-based classifier under the influence of different types of information loss that happens in the JPEG algorithm. 
	<li> We consider image quality degradation due to chroma subsampling, quantization, and rounding functions of the JPEG algorithm. </li>
	<li> We analyze three types of interpolation methods (<i>nearest neighbor</i>, <i>bilinear</i>, and <i>bicubic</i> interpolation methods</i>)in the chroma upsampling function.</li>
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


<h3>Conclusion</h3>
This study presented quantitative assessment of the impact that the JPEG compression has on DL-based image classification. The analysis have shown that the quantization of DCT coefficients preserves model accuracy while delivering better compression savings. However, to avoid the computational cost of quantization step, simple chroma subsampling and simple chroma upsampling with the nearest neighbor interpolation can be used, which achieved the same accuracy with a slight degradation in the compression savings.


<br>[Full Article](https://www.earticle.net/Article/A419789)