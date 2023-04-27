---
title: "An Approach to Run Pre-Trained Deep Learning Models on Grayscale Images"
collection: publications
permalink: /publication/2021-04-13-paper-title-number-IC5
date: 2021-04-13
venue: 'IEEE International Conference on Artificial Intelligence in Information and Communication (ICAIIC)'

---
<h3>Abstract</h3>
<p>Transfer learning helps the performance of a
learning algorithm significantly when training deep learning
models on challenging datasets. However, the pre-trained
networks have certain constraints in terms of their architecture.
For example, due to the wide availability of color images, stateof-
the-art pre-trained networks expect an input image with
three color channels. Grayscale images have small sizes as
compared to color images and thus can enable real time
computer vision applications in scenarios where there are
constraints on device memory and bandwidth. Therefore, in this
work we propose an approach to run pre-trained models on
grayscale images for image classification tasks. We have used
the VGG16 pre-trained model to classify Kaggle Dogs vs. Cats
dataset. We have compared our results with VGG16 applied on
color images. Our results have shown that when the weights for
the first hidden layer are initialized as the mean of the pretrained
network weights then the classification accuracy with
only 0.04% error can be achieved. Our analysis has shown that
comparable benefits can be reaped when using grayscale images
for deep learning based classification tasks with only one-third
of the bandwidth and storage requirements.</p>

[Full Article](https://ieeexplore.ieee.org/document/9415275)