---
title: "Noise-cuts-Noise Approach for Mitigating the JPEG Distortions in Deep Learning"
collection: publications
permalink: /publication/2023-02-20-paper-title-number-IC15
date: 2023-02-20
venue: 'IEEE International Conference on Artificial Intelligence in Information and Communication (ICAIIC)'
author_profile: false
---
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<h3>Abstract</h3>
<p>Lossy image compression provides an efficient
solution to the exchange and storage of large volumes of image
data for various applications. The main design principle of a
lossy compression algorithm is to discard visually insignificant
information as much as possible while keeping the resulted
visible artifacts at a minimum. However, these unperceivable
defects significantly degrade the performance of a trained deep
learning (DL) model. Therefore, to improve the classification
performance of the models on noisy images, we propose a noise-based
data augmentation technique called <i>noise-cuts-noise</i> (as the noise is used to mitigate the noise impact) approach. The simulation analysis have shown that the
proposed method efficiently mitigates the performance gap on
highly compressed images for example, the accuracy difference
is reduced from 11% to 2% for classification of natural images.
For uncompressed images, the model performance is either
preserved or improved. In addition, to validate the usefulness of
the proposed method, we considered a case study of multi-label
classification task in chest X-ray (CXR) images. The model
accuracy on highly compressed images with the proposed
augmentation method increased 2% on higher resolution
images while the accuracy difference reduced from 6% to 1%
on smaller resolution images.</p>

<h3>Contributions</h3>
<ul>
	<li>Noise-based image augmentation method to make DL robust against the JPEG distortions. </li>
	<li> Optimal level of distortion for noise-based augmentation method. </li>
	<li>As an application of our proposed method, we designed a case study of multi-label classification task for medical image analysis. </li>
</ul>

<h3>Proposed Method</h3>

<p>For an image \(I\), its JPEG compressed image \(I_{c}\) without the chroma-subsampling function can obtained as</p>
<div style="overflow-x:auto">\[I_{c}=[Q(D(C_{YCbCr}(I)),Qf)],\]</div>

<p>and \(I_{c}\) can be decompressed to obtain \(I_{d}\) as</p>

<div style="overflow-x:auto">\[I_{d}=[C_{RGB}([D^{-1}(Q^{-1}(I_{c},Qf))])]|_0^{255}\]</div>

<h3>Conclusion</h3>
We proposed a noise-based image augmentation method to make DL models robust against compression distortions -- <i>noise-cuts-noise</i>. The analysis have shown that choosing varying level of noise helps the model to perform well on the future noisy images. Besides improving the model performance on noisy images, the main advantage of the proposed method is that it does not require any preprocessing for the artifacts correction.

<br>[Full Article](https://ieeexplore.ieee.org/document/10067012)