---
title: "Noise-cuts-Noise Approach for Mitigating the JPEG Distortions in Deep Learning"
collection: publications
permalink: /publication/2023-02-20-paper-title-number-IC15
date: 2023-02-20
venue: 'IEEE International Conference on Artificial Intelligence in Information and Communication (ICAIIC)'
author_profile: false
---

<style>
a:link {
  text-decoration: none;
}

a:visited {
  text-decoration: none;
}

a:hover {
  text-decoration: none;
}

a:active {
  text-decoration: none;
}

.sticky {
  position: fixed;
  top: 0;
}
</style>

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<div style="font-size: 12pt; overflow: hidden; background-color: #FFFFFF; width: 100%;" id="myHeader"><strong> Jump to:
<a href="#abstract">Abstract</a>
| <a href="#contributions">Contributions</a>
| <a href="#proposedMethod">Proposed Method</a>
| <a href="#conclusion">Conclusion</a>
| <a href="#relatedArticles">Related Articles</a>
</strong></div>

<h3 id="abstract">Abstract</h3>
<p>Lossy image compression provides an efficient solution to the exchange and storage of large volumes of image data for various applications. The main design principle of a lossy compression algorithm is to discard visually insignificant information as much as possible while keeping the resulted visible artifacts at a minimum. However, these unperceivable defects significantly degrade the performance of a trained deep learning (DL) model. Therefore, to improve the classification performance of the models on noisy images, we propose a noise-based data augmentation technique called <i>noise-cuts-noise</i> (as the noise is used to mitigate the noise impact) approach. The simulation analysis have shown that the proposed method efficiently mitigates the performance gap on highly compressed images for example, the accuracy difference is reduced from 11% to 2% for classification of natural images. For uncompressed images, the model performance is either preserved or improved. In addition, to validate the usefulness of the proposed method, we considered a case study of multi-label classification task in chest X-ray (CXR) images. The model accuracy on highly compressed images with the proposed augmentation method increased 2% on higher resolution images while the accuracy difference reduced from 6% to 1% on smaller resolution images.</p>

<h3 id="contributions">Contributions</h3>
<ul>
	<li>Noise-based image augmentation method to make DL robust against the JPEG distortions. </li>
	<li> Optimal level of distortion for noise-based augmentation method. </li>
	<li>As an application of our proposed method, we designed a case study of multi-label classification task for medical image analysis. </li>
</ul>

<h3 id="proposedMethod">Proposed Method</h3>

<p>For an image \(I\), its JPEG compressed image \(I_{c}\) without the chroma-subsampling function can obtained as</p>
<div style="overflow-x:auto">\[I_{c}=\left[Q\left(D\left(C_{YCbCr}\left(I\right)\right),Qf\right)\right],\]</div>

<p>and \(I_{c}\) can be decompressed to obtain \(I_{d}\) as</p>

<div style="overflow-x:auto">\[I_{d}=\left[C_{RGB}\left(\left[D^{-1}\left(Q^{-1}\left(I_{c},Qf\right)\right)\right]\right)\right]\rvert_0^{255}\]</div>

<p>where, \(\left[.\right]\) and \(.\rvert_0^{255}\) rounds and truncates the values to a valid range in the spatial domain, respectively.</p>

<p>In the JPEG algorithm, the information loss is resulted from the quantization forward function \(Q\) as in Equation (\(3\)) and inverse function \(Q^{-1}\) as in Equation (\(4\)). The two transformation functions that is, the colorspace conversion function \(C\) and discrete cosine transform function \(D\) are lossless in nature; however, when their values are rounded or truncated then certain information are lost.</p>

<div style="overflow-x:auto">\[\widehat{F}_{(u,v)}=round\left(\frac{F_{(u,v)}}{QT_{(u,v)}}\right),\]</div>
<p>where \(F_{\left(u,v\right)}\) is the DCT matrix and \(QT_{\left(u,v\right)}\) is the quantization table.</p>
<div style="overflow-x:auto">\[\widetilde{F}_{\left(u,v\right)}=\widehat{F}_{\left(u,v\right)}\times QT_{\left(u,v\right)}.\]</div>

<h3 id="conclusion">Conclusion</h3>
We proposed a noise-based image augmentation method to make DL models robust against compression distortions -- <i>noise-cuts-noise</i>. The analysis have shown that choosing varying level of noise helps the model to perform well on the future noisy images. Besides improving the model performance on noisy images, the main advantage of the proposed method is that it does not require any preprocessing for the artifacts correction.

<br>[Full Article](https://ieeexplore.ieee.org/document/10067012)

<h3 id="relatedArticles">Related Articles</h3>
[Assessment of the JPEG compression artifacts due to chroma subsampling, impact on a deep learning model performance]({{ site.baseurl }}{% link _publications/2022-10-08-paper-title-number-IC10.md %})<br>


<script>
window.onscroll = function() {myFunction()};

var header = document.getElementById("myHeader");
var sticky = header.offsetTop;

function myFunction() {
  if (window.pageYOffset > sticky) {
    header.classList.add("sticky");
  } else {
    header.classList.remove("sticky");
  }
}
</script>