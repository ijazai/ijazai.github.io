---
title: "Noise-cuts-Noise Approach for Mitigating the JPEG Distortions in Deep Learning"
collection: publications
permalink: /publication/2023-02-20-paper-title-number-IC15
date: 2023-02-20
venue: 'IEEE International Conference on Artificial Intelligence in Information and Communication (ICAIIC)'

---
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
data augmentation technique called noise-cuts-noise
approach. The simulation analysis have shown that the
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

[Full Article](https://ieeexplore.ieee.org/document/10067012)


<h3 id="citation">Citation</h3>

<p>Please cite our paper if it has helped you:</p>

<div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code>@inproceedings{ICAIIC2022,
author    = {Ahmad, Ijaz and Shin, Seokjoo},
title     = {Noise-cuts-Noise Approach for Mitigating the JPEG Distortions in Deep Learning},
booktitle = {IEEE International Conference on Artificial Intelligence in Information and Communication (ICAIIC)},
pages     = {221--226},
year      = {2023}
}
</code></pre></div></div>