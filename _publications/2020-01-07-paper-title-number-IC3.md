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

<h3>Contributions</h3>

<ul>
<li>We have analyzed the number of moduli (i.e.block size) effect on the compression performance of CRT-based compression methods. </li> 
<li>We have tested various block sizes and different values for moduli proposed in the literature.</li>
</ul>

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

<p>
The pixel intensity values range from \(0\) to \(255\). Therefore, a block of k pixels can be represented with a unique CRT
solution x using (2) by taking k numbers of moduli whose values are greater than \(255\) and are relative co-prime. The
result of this operation is a compressed image. The image can be decompressed using the same set of moduli for (4).
</p>

<h3>Results Summary</h3>
<p>
The experimental results indicate that as the block size is reduced, the CRT based compression method progresses towards achieving compression of data. The highest compression ratio is achieved for smaller block size of \(k=2\). For block size of \(2\) and moduli values \(n_{1}=257\) and \(n_{2}=258\), we have achieved \(8.65%\) average compression ratio on KODAK dataset. For block size greater than \(2\), our analysis agreed with the literature that the original data expanded rather than being compressed. However, for \(k=2\) we have achieved a significant compression of original data on the contrary of what was previously observed in the literature. 
</p>

<h3>Conclusion</h3>
We have analyzed the parameters that effect the performance of CRT based compression methods. Our results linked the degraded performance of CRT based compression with improper selection of moduli number (i.e. pixels block size). The experiments have shown that a significant compression ratio can be achieved with smaller block size.

<br>[Full Article](https://ieeexplore.ieee.org/document/9016442)