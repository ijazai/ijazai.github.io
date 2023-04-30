---
title: "Analysis of Chinese Remainder Theorem for Data Compression"
collection: publications
permalink: /publication/2020-01-07-paper-title-number-IC3
date: 2020-01-07
venue: 'IEEE International Conference on Information Networking (ICOIN)'
author_profile: false
---

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<h3>Abstract</h3>
<p>Chinese remainder theorem (CRT) forms the
foundation of recent simultaneous encryption and compression
schemes for image data. In the schemes moduli sequence is being
used as the secret key while, the number of moduli is being
considered as the achievable compression ratio. However, some
studies have discredited these schemes and reported the
compression performance of CRT as poor or even negative. In
this study, we have investigated parameters that effect the
compression performance of CRT. We have performed our
experiments on KODAK dataset. Our analysis links the
degraded compression performance of CRT with the number of
moduli i.e. the block size to be compressed. Further, our results
have shown an improved performance for smaller number of
moduli. We have achieved an average compression ratio of
about 8% on KODAK dataset.</p>

<h3>Chinese Remainder Theorem</h3>
<p>Chinese Remainder Theorem (CRT) states that if \(n_{1},n_{2},\cdot\cdot\cdot,a_{k}\) are pairwise prime positive integers, then for any arbitrary integers \(a_{1},a_{2},\cdot\cdot\cdot,a_{k}\) the system of congruences </p>

<div>\[x\equiv a_{i}\bmod{n_{i}}, i=1,2,\cdot\cdot\cdot,k\]</div>

<p>has a unique solution</p>

<div>\[x\equiv \sum_{i=1}^k a_{i}N_{i}M_{i}\bmod N\]</div>

<p>Given that; \(n_{1},n_{2},\cdot\cdot\cdot,n_{k}>\max\left(a_{1},a_{2},\cdot\cdot\cdot,a_{k}\right),k\) is the number of congruences and </p>

<div>
\[
N=\prod_{i=1}^k n_{i},
N_{i}=\frac{N}{n_{i}}, 
M_{i}\equiv N_{i}^{-1}\bmod n_{i}
\]
</div>

<p>The CRT can be extended to an arbitrary finite number of congruences with \(n_{k}\) relatively prime. The intgers \(a_{1},a_{2},\cdot\cdot\cdot,a_{k}\) can be recovered from Equation (2) by finding modulus of \(x\) with corresponding \(n_{1},n_{2},\cdot\cdot\cdot,a_{k}\) as, </p>

<div>
\[a_{i}\equiv x\bmod n_{i}\]
</div>

<br>[Full Article](https://ieeexplore.ieee.org/document/9016442)