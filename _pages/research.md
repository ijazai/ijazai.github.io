---
layout: archive
title: ""
permalink: /research/
author_profile: true
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

.stickyDiv {
  position: fixed;
  top: 0;
}

</style>



<div style="font-size: 12pt; overflow: hidden; background-color: #FFFFFF; width: 100%;" id="myHeader"><strong> Jump to:
<a href="#researchArea">Research Area</a>
| <a href="#phdThesis">PhD Thesis</a>
| <a href="#currentWork">Current Work</a>
</strong></div>

<p align="justify" id="researchArea"><span style="font-size: 12pt;"><strong>Research Area</strong></span></p>

<p align="justify"><span style="font-size: 11pt;">

My research interests are in privacy preservation during data transmission – <i>in transit</i>, data storage – <i>at rest</i>, and computation – <i>in use</i>. The scope of my research spans across multiple fields, from image encryption to computer vision, including Machine Learning (ML) in the image analysis domain. <br><br>

There are two main challenges in the development and implementation of Deep Learning (DL) solutions: First, DL algorithms are characterized as compute-intensive tasks, and their training requires innovative technology and high computational resources. Second, training DL models for a particular task needs a large volume of sample data, which in some domains such as in the field of medical image analysis, is expensive and difficult to acquire. These challenges can be efficiently addressed by taking advantage of powerful infrastructures such as cloud services. For example, in the first case, organizations can avail cloud-computing services to access the latest technology to speed-up the training process and allow DL models to scale efficiently with a lower capital cost. Similarly, to mitigate the data deficiency challenge, an organization can benefit from a community cloud, where services are shared by organizations with common interests to achieve their goals. In this case, cloud storage services can be utilized as a shared data repository for joint collaborative learning. <br><br>

This avail of third-party resources provides an efficient solution for a well-trained DL model; however, this can lead to privacy concerns as data outsourcing comes with a risk of information leakage. Though the traditional image encryption techniques guarantee data security in transit and at rest, data decryption is necessary prior to performing any computations on them, which makes them inadequate to cater to the requirements of data security in use. On the other hand, techniques specifically proposed to enable computation in the encryption domain have either their associated computational cost, communication overhead or specialized design requirement that may reduce data utility and degrade the DL model performance. In addition, when transmitting large volumes of data (especially images), compression is necessary to efficiently utilize the available bandwidth. Therefore, I argue for a holistic privacy-preserving solution that can satisfy the dual requirements of data transmission, data storage and computation in the encryption domain to fully reap the benefits of DL for data-driven applications.

</span></p>

<hr style="height:1px;border-width:0;color:gray;background-color:gray">

<p align="justify" id="phdThesis"><span style="font-size: 12pt;"><strong>PhD Thesis</strong></span></p>

<p align="justify"><span style="font-size: 11pt;"> 
Compression and encryption deal with the redundancy of a source but each with their own purpose. The unwanted redundancy of a source is reduced in compression to achieve a data representation that requires lesser number of bits while in encryption it is reduced to make the source unintelligible by the addition of randomness. The order in which the compression and encryption operations are carried out affects the overall efficiency of the system. The common approach is to complete compression prior to encryption. Otherwise there is less or no compressibility as the encryption process would have significantly reduced the correlation and altered the statistical distribution of the image data. <br><br>
In my PhD thesis, I investigated the order of performing compression and encryption to find proper trade-offs between maintaining a desired level of compression savings, preserving necessary privacy while achieving acceptable downstream application performance by means of implementing suitable encryption and compression techniques, and avoiding (or at best, reducing) the potential negative impact of the visual degradation (because of applying either privacy preservation or compression technique) on the DL model performance. The main contributions of my thesis are summarized as below:

<ul>
<li><p align="justify"><span style="font-size: 11pt;"><strong>A simultaneous image compression and encryption algorithm</strong><br>
Image compression and encryption are often coupled together for efficient and secure image transmission and/or storage. A straightforward way is to perform compression and encryption as two separate processes. However, the problem with such an approach is that if the encryption is performed before, then the compression efficiency is severely reduced. Conversely, it is challenging to ensure reasonable security in the compression domain while preserving the compression savings. We  proposed a hybrid simultaneous image encryption and compression algorithm in [1] that incorporates the compression requirement of a data communication system into the encryption algorithm. In our scheme, encryption is based on Chaos theory and is carried out in two steps, i.e., permutation and substitution. The lossless compression is performed on the shuffled image and then the compressed bitstream is grouped into 8-bit blocks for the substitution stage. Furthermore, to improve the performance of the entropy encoder in the compression algorithm, we proposed a novel data-to-symbol mapping method based on the Chinese remainder theorem to represent adjacent pixel values as a block. Such representation improved the compression savings on average from 5.76% to 15.45%.
</span></p> </li>

<li><p align="justify"><span style="font-size: 11pt;"><strong>A data augmentation technique to mitigate compression artifacts on DL</strong><br>
Lossy image compression provides an efficient solution to the exchange and storage of large volumes of image data for various applications. The resulting human unperceivable defects in the compressed images significantly degrade the performance of a trained DL model. Towards which we proposed a noise-based data augmentation technique in [2] to enhance the quality of training datasets such that the model generalizes well on noisy images in the future. Specifically, we considered the JPEG distortions to generate new images. The main advantages of the proposed method are that it does not require artifact correction as a preprocessing step and can preserve the model performance on the uncompressed images. Simulation results showed that the proposed technique mitigates the impact of the lossy compression artifacts on the trained DL model performance, and on heavily compressed images the accuracy difference is reduced from 11% to 2% for classification of natural images and 6% to 1% for COVID-19 detection in chest X-ray images.
</span></p> </li>

<li><p align="justify"><span style="font-size: 11pt;"><strong>A new geometric transformation function for perceptual encryption methods</strong><br>
In the conventional PE methods, for better security, a larger number of blocks is achieved by decreasing the block size; therefore, the key size expansion is limited by the smallest allowable block size used in the compression algorithm. In addition, the extended PE methods that process each color component independently to achieve a larger number of blocks degrade image quality and compression savings, and remove color information, which limits their applications. To overcome these limitations, we proposed inter and intra block processing in [3] (healthcare applications in [4], [5]) that performs the encryption steps that only change correlation’s direction on a sub-block level, thereby improving the encryption efficiency without compromising the compression performance. The intra block processing results in a new transformation called inside-out transformation function. Compared to the plain image compression, the JPEG performance on the cipher images is reduced ~3% at best.
</span></p> </li>

<li><p  align="justify"><span style="font-size: 11pt;"><strong>Privacy-preserving DL applications</strong><br>
Besides better security, the main advantage of the proposed PE method is that the spatial information is retained in each color channel, which makes it suitable for privacy-preserving computations. For privacy-preserving natural images classification task presented in [3], [6], our proposed scheme at best introduces a decrease of ~5% in the prediction accuracy of the trained models. For privacy-preserving face recognition applications presented in [7], the proposed scheme delivers the same recognition accuracy as that of the plain images. For COVID-19 screening in chest X-ray images presented in [8], the proposed PE-based privacy-preserving scheme at best introduces ~3% drop in the model's accuracy and sensitivity scores.
</span></p> </li>

</ul>


</span></p>

<hr style="height:1px;border-width:0;color:gray;background-color:gray">

<p align="justify" id="currentWork"><span style="font-size: 12pt;"><strong>Current Work</strong></span></p>
<p align="justify"><span style="font-size: 11pt;">
Currently, I am working on representation learning to quantify perceptual distortions in wirelessly transmitted images. This is motivated by an observation that the existing Image Quality Assessment (IQA) metrics either rely on or are optimized to coincide with human judgment and do not account for the perceptual distortions (for example, because of imperfect communication system) that are responsible for the degradation in DL model performance. Given the popularity of DL solutions in various domains, it is necessary to quantify perceptual loss in distorted images using machine perception. Towards this we proposed an IQA metric that compares the perceptual similarity between distorted and original images in the semantic feature space defined by latent-variable models. It is anticipated that the proposed method will give an important indication of a DL model performance implemented on a remotely located server for a downstream application and can be used to optimize the parameters of a communication system.
</span></p>


<hr style="height:1px;border-width:0;color:gray;background-color:gray">

<p align="justify" id="currentWork"><span style="font-size: 12pt;"><strong>References</strong></span></p>

<p align="justify"><span style="font-size: 11pt;">
[1]	I. Ahmad and S. Shin, “A novel hybrid image encryption–compression scheme by combining chaos theory and number theory,” Signal Processing: Image Communication, vol. 98, p. 116418, Oct. 2021, doi: 10.1016/j.image.2021.116418.</span>
[<a href="https://www.sciencedirect.com/science/article/abs/pii/S0923596521001983" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2021-08-19-paper-title-number-J1.md %}) </p>

<p align="justify"><span style="font-size: 11pt;">
[2]	I. Ahmad and S. Shin, “Noise-cuts-Noise Approach for Mitigating the JPEG Distortions in Deep Learning,” in 2023 International Conference on Artificial Intelligence in Information and Communication (ICAIIC), Bali, Indonesia: IEEE, Feb. 2023, pp. 221–226. doi: 10.1109/ICAIIC57133.2023.10067012.</span></p>
[<a href="https://ieeexplore.ieee.org/document/10067012" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2023-02-20-paper-title-number-IC15.md %})

<p align="justify"><span style="font-size: 11pt;">
[3]	I. Ahmad and S. Shin, “IIB–CPE: Inter and Intra Block Processing-Based Compressible Perceptual Encryption Method for Privacy-Preserving Deep Learning,” Sensors, vol. 22, no. 20, p. 8074, Oct. 2022, doi: 10.3390/s22208074.</span></p>
[<a href="https://www.mdpi.com/1424-8220/22/20/8074" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2022-10-21-paper-title-number-J3.md %})

<p align="justify"><span style="font-size: 11pt;">
[4]	I. Ahmad and S. Shin, “Encryption-then-Compression System for Cloud-based Medical Image Services,” in 2022 International Conference on Information Networking (ICOIN), Jeju-si, Korea, Republic of: IEEE, Jan. 2022, pp. 30–33. doi: 10.1109/ICOIN53446.2022.9687214. <b>[Best Paper Award] </b></span></p>
[<a href="https://ieeexplore.ieee.org/document/9687214" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2022-01-12-paper-title-number-IC7.md %})

<p align="justify"><span style="font-size: 11pt;">
[5]	I. Ahmad and S. Shin, “A Perceptual Encryption-Based Image Communication System for Deep Learning-Based Tuberculosis Diagnosis Using Healthcare Cloud Services,” Electronics, vol. 11, no. 16, p. 2514, Aug. 2022, doi: 10.3390/electronics11162514.</span></p>
[<a href="https://www.mdpi.com/2079-9292/11/16/2514" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2022-08-11-paper-title-number-J2.md %})

<p align="justify"><span style="font-size: 11pt;">
[6]	I. Ahmad and S. Shin, “Perceptual Encryption-based Privacy-Preserving Deep Learning in Internet of Things Applications,” in 2022 13th International Conference on Information and Communication Technology Convergence (ICTC), Jeju Island, Korea, Republic of: IEEE, Oct. 2022, pp. 1817–1822. doi: 10.1109/ICTC55196.2022.9952589.</span></p>
[<a href="https://ieeexplore.ieee.org/document/9952589" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2022-10-19-paper-title-number-IC11.md %})

<p align="justify"><span style="font-size: 11pt;">
[7]	I. Ahmad, E. Kim, S.-S. Hwang, and S. Shin, “Privacy-Preserving Surveillance for Smart Cities,” presented at the The 13th International Confernce on Ubiquitous and Future Networks, Barcelona, Spain, Jul. 2022.</span></p>
[<a href="https://ieeexplore.ieee.org/document/9829680" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2022-07-05-paper-title-number-IC9.md %})

<p align="justify"><span style="font-size: 11pt;">
[8]	I. Ahmad and S. Shin, “Perceptual Encryption-based Privacy-Preserving Deep Learning for Medical Image Analysis,” in 2023 International Conference on Information Networking (ICOIN), Bangkok, Kingdom of Thailand: IEEE, Jan. 2023, pp. 224–229. <b>[Best Paper Award] </b></span></p>
[<a href="https://ieeexplore.ieee.org/document/10048970" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2023-01-11-paper-title-number-IC13.md %})


<script>
window.onscroll = function() {myFunction()};

var header = document.getElementById("myHeader");
var stickyDiv = header.offsetTop;

function myFunction() {
  if (window.pageYOffset > stickyDiv) {
    header.classList.add("stickyDiv");
  } else {
    header.classList.remove("stickyDiv");
  }
}
</script>