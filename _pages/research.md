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
| <a href="#phdThesis">Ph.D. Thesis</a>
| <a href="#currentWork">Current Work</a>
</strong></div>

<p align="justify" id="researchArea"><span style="font-size: 12pt;"><strong>Research Area</strong></span></p>

<p align="justify"><span style="font-size: 11pt;">

My research interests are in privacy preservation during data transmission – <i>in transit</i>, data storage – <i>at rest</i>, and computation – <i>in use</i>. The scope of my research spans across multiple fields, from image encryption to computer vision, including Machine Learning (ML) in the image analysis domain. <br><br>

There are two main challenges in the development and implementation of Deep Learning (DL) solutions: First, DL algorithms are characterized as compute-intensive tasks, and their training requires innovative technology and high computational resources. Second, training DL models for a particular task needs a large volume of sample data, which in some domains such as in the field of medical image analysis, is expensive and difficult to acquire. These challenges can be efficiently addressed by taking advantage of powerful infrastructures such as cloud services. For example, in the first case, organizations can avail cloud-computing services to access the latest technology to speed-up the training process and allow DL models to scale efficiently with a lower capital cost. Similarly, to mitigate the data deficiency challenge, an organization can benefit from a community cloud, where services are shared by organizations with common interests to achieve their goals. In this case, cloud storage services can be utilized as a shared data repository for joint collaborative learning. <br><br>

This avail of third-party resources provides an efficient solution for a well-trained DL model; however, this can lead to privacy concerns as data outsourcing comes with a risk of information leakage. Though the traditional image encryption techniques guarantee data security in transit and at rest, data decryption is necessary prior to performing any computations on them, which makes them inadequate to cater to the requirements of data security in use. On the other hand, techniques specifically proposed to enable computation in the encryption domain have either their associated computational cost, communication overhead or specialized design requirement that may reduce data utility and degrade the DL model performance. In addition, when transmitting large volumes of data (especially images), compression is necessary to efficiently utilize the available bandwidth. Therefore, I argue for a holistic privacy-preserving solution that can satisfy the dual requirements of data transmission, data storage and computation in the encryption domain to fully reap the benefits of DL for data-driven applications.

</span></p>

<hr style="height:1px;border-width:0;color:gray;background-color:gray">

<p align="justify" id="phdThesis"><span style="font-size: 12pt;"><strong>Ph.D. Thesis</strong></span></p>

<p align="justify"><span style="font-size: 11pt;"> 
Compression and encryption deal with the redundancy of a source but each with their own purpose. The unwanted redundancy of a source is reduced in compression to achieve a data representation that requires lesser number of bits while in encryption it is reduced to make the source unintelligible by the addition of randomness. The order in which the compression and encryption operations are carried out affects the overall efficiency of the system. The common approach is to complete compression prior to encryption. Otherwise there is less or no compressibility as the encryption process would have significantly reduced the correlation and altered the statistical distribution of the image data. <br><br>
In my Ph.D. thesis, I investigated the order of performing compression and encryption to find proper trade-offs between maintaining a desired level of compression savings, preserving necessary privacy while achieving acceptable downstream application performance by means of implementing suitable encryption and compression techniques, and avoiding (or at best, reducing) the potential negative impact of the visual degradation (because of applying either privacy preservation or compression technique) on the DL model performance. The main contributions of my thesis are summarized as below:

<ul>
<li><p align="justify"><span style="font-size: 11pt;"><strong> Design and evaluation of a simultaneous image compression and encryption algorithm for image data sharing and archiving applications</strong><br>

Compression and encryption are often performed together for image sharing and/or storage. Both processes deal with the redundancy of a source but each with their own purpose. The unwanted redundancy of a source is reduced in compression to achieve a data representation that requires lesser number of bits while in encryption it is reduced to make the source unintelligible by the addition of randomness. The order in which these two processes are coupled together affects the overall efficiency of digital image services. For example, encrypted data has less or no compressibility while it is challenging to ensure reasonable security without downgrading the compression performance. The problem lies in treating compression and encryption as two separate processes. We<sup>1</sup> proposed a hybrid simultaneous image encryption and compression algorithm in [1] that incorporates the compression requirement of a data communication system into the encryption algorithm. Encryption is based on Chaos theory and is carried out in two steps, i.e., permutation and substitution. The lossless compression is performed on the shuffled image and then the compressed bitstream is grouped into 8-bit blocks for substitution stage. In addition, to compensate for any degradation in compression efficiency resulting from the permutation step, we proposed a novel data-to-symbol mapping method based on the Chinese remainder theorem to represent adjacent data elements as a block [2]. The proposed method aids the compression efficiency of the scheme for two reasons: first, treating a block of data elements as a single symbol extends the alphabet source, thereby the most probable symbol has a probability much lesser than 1 and, as a result, improves the average number of bits per symbol. Secondly, the block representation enables the Huffman coding to assign non-integer-length codeword to each symbol separately, and for larger block size the average bitrate monotonically reaches the source entropy. Simulation analysis showed that with such representation, the compression saving was improved on average from 5.76% to 15.45%. Furthermore, the lossless nature of the proposed scheme makes it suitable for medical image compression and encryption applications.
<br><br>
<sup>1</sup>The standard pronoun “We” is used for reporting collaborative research; however, I have carried out the main research activities.
</span></p> </li>

<li><p align="justify"><span style="font-size: 11pt;"><strong> Design and evaluation of a data augmentation technique to mitigate compression artifacts on DL</strong><br>
Lossy image compression provides an efficient solution to the exchange and storage of large volumes of image data for various applications. The main design principle of a lossy compression algorithm is to discard visually insignificant information as much as possible while keeping the resulting visible artifacts at a minimum. The JPEG standard is one of the widely used image compression standards and is available on most consumer devices and on the internet. The JPEG algorithm was designed in the early 90s with human subjects in mind. Therefore, the perceptual quality in the lossy compressed images is based on the characteristics of human visual system (HVS). For example, HVS is more sensitive to brightness and low frequencies than color and high frequencies. Therefore, two images with same brightness but one with lower color resolution than the other will appear same to a human. However, these unperceivable defects significantly degrade the performance of a trained DL model. Because for an efficient model, it is necessary that the training and testing are performed against the data that come from the same target application distribution. Furthermore, a large volume of data is necessary for training an efficient DL model to avoid overfitting and to generalize well on the unseen data, which is difficult and expensive to acquire. Data augmentation is one of the effective solutions to this problem that can improve the model generalization, for which the existing techniques are not adequate as they do not take noise into consideration. We proposed a novel noise-based data augmentation technique in [3] to enhance the quality of training datasets such that the model generalizes well on the noisy images in future. Specifically, we considered the JPEG distortions to generate new images. The main advantages of the proposed method are that it does not require artifact correction as a preprocessing step and can preserve the model performance on the uncompressed images. Simulation results showed that the proposed technique mitigated the impact of the compression artifacts on the trained DL model performance and on heavily compressed images, the accuracy difference was reduced from 11% to 2% for classification of natural images and 6% to 1% for COVID-19 detection in chest X ray (CXR) images. In addition, for larger resolution images the model is immune against noise but with the proposed method there was a 2% gain in the model’s performance.
</span></p> </li>

<li><p align="justify"><span style="font-size: 11pt;"><strong> Analysis and taxonomy of the state-of-the-art perceptual encryption techniques for encryption-then-compression systems</strong><br>
In general, when encryption is completed prior to compression then less or no redundancy is left for the compression algorithm to exploit to reduce the image size. Therefore, in all cases it is preferred to perform compression before encryption – compression-then-encryption (CtE). However, when multimedia applications such as photo-storage services have the requirement of preserving the image format after the compression and encryption processes, then it is beneficial to reverse the conventional order of CtE. In this direction, a new class of image encryption techniques called perceptual encryption (PE) algorithms is emerging, which hides identifiable information of an image in such a way that its intrinsic characteristics such as correlation on a block level and intensity distribution, remain intact. The PE methods provide a necessary level of security while preserving the compression savings of the JPEG algorithm. A tradeoff in these methods, however, is between the security efficiency and compression savings due to the chosen block size. Several methods (such as the processing of each color component independently, image representation, and sub-block-level processing) have been proposed to effectively manage this tradeoff. We adapted these assorted practices into a uniform framework to provide a fair comparison of their results [4]. Specifically, their compression quality is investigated under various design parameters, such as the choice of colorspace, image representation, chroma subsampling, quantization tables, and block size. Our analyses showed that at best the PE methods introduced a decrease of 6% and 3% in the JPEG compression performance with and without chroma subsampling, respectively. Additionally, their encryption quality was quantified in terms of several statistical analyses. The simulation results showed that block-based PE methods exhibited several favorable properties for the encryption-then-compression schemes. Nonetheless, to avoid any pitfalls, their principal design should be carefully considered in the context of the applications for which we outlined probable future research directions.
</span></p> </li>

<li><p align="justify"><span style="font-size: 11pt;"><strong> Design of a new geometric transformation function for perceptual encryption methods</strong><br>
In the conventional PE methods, for better security, a larger number of blocks is achieved by decreasing the block size; therefore, the key size expansion is limited by the smallest allowable block size used in the compression algorithm. In addition, the extended PE methods that process each color component independently to achieve a larger number of blocks degrade image quality and compression savings, and remove color information, which limits their applications. To overcome these limitations, we proposed inter and intra block processing in [5], [6] (extended applications to healthcare domain in [7], [8]) that performed the encryption steps that only change correlation’s direction on a sub-block level, thereby improved the encryption efficiency without compromising the compression performance. The intra block processing resulted in a new transformation called <i>inside-out</i> transformation function. Compared to plain image compression, the JPEG performance on the cipher images was reduced ≈3% at best.
</span></p> </li>

<li><p  align="justify"><span style="font-size: 11pt;"><strong> Perceptual Encryption-based Privacy-Preserving DL Applications</strong><br>
Compared to full-image encryption methods, the PE algorithms make the images visually unrecognizable by hiding only the perceptual information in them. The PE algorithms trade security to enable other multimedia applications requirements such as low computational complexity, format compatibility and compression of the cipher images. Their applications have been extended to privacy-preserving cloud-based photo storage services, social networking services and image retrieval. The human unperceivable information preserved in the cipher images can be exploited to enable different image processing and computer vision algorithms computations in encryption domain. However, the existing PE methods (block-based compressible PE methods) are designed to provide bandwidth/storage efficiency and security during image data transmission and/or storage. Therefore, naïvely extending them for Privacy Preserving Deep Learning (PPDL) applications raises major concerns such as the secured PE methods disrupt the spatial information thus rendering the cipher images useless for DL computations. In addition, they have color image input as a prerequisite for encryption efficiency, which limits their applications such as ones in medical image analysis domain. The proposed PE method eliminates the security vulnerabilities and limitations of the conventional methods and can be utilized to provide security and bandwidth efficiency during image data transmission and can enable privacy-preserving computation on third-party cloud resources without disclosing the secret information. In this thesis, I extended the scope of applications of the proposed PE algorithm to three privacy-preserving domains as below:

<br><br>
<i>Privacy-Preserving Face Recognition Scheme</i><br>
Surveillance is one of the main building blocks of smart cities, which provides safer communities and efficient city operations. However, this convenience comes at the cost of relinquishing personal data and privacy. Given the large volume of data, cloud-based storage is emerging as a cost effective and efficient solution. In addition, the data is often outsourced to third party computational resource providers for performing several computer vision tasks such as action and activity recognition, people counting, age and gender estimation, fire and smoke detection and vehicle detection. The data collected by the surveillance system often consists of privacy sensitive data that can be exploited to recognize an individual. Therefore, it is important to keep the citizens data secure while providing them with the facilities. Towards this we proposed PE-based privacy-preserving face recognition task in [9]. We have implemented support vector machines (SVMs) with randomized principal component analysis (PCA) for dimensionality reduction. The simulation analysis on the Labeled Faces in the Wild (LFW) dataset showed that the proposed encryption algorithm did not affect the SVMs performance, and the same recognition accuracy can be achieved on the encrypted images as that of the plain images.

<br><br>
<i>Privacy-Preserving Natural Image classification</i><br>
As an application of our PE method, we proposed an end–to–end image communication system for PPDL–based image classification [5], [6]. The proposed system considered a secure and efficient transmission of images to a remote location, thereby end–to–end, and enabled classification in the encryption domain without the need for decryption, thereby privacy– preserving deep learning. We implemented PyramidNet model with ShakeDrop regularization for multi-label classification tasks. The simulation analysis showed that the proposed method at best introduced a decrease of ≈5% in the prediction accuracy of a DL model for natural image classification task.

<br><br>
<i>Privacy-Preserving COVID-19 Detection</i><br>
The widespread adoption of DL solutions in healthcare organizations is obstructed by their compute intensive nature and dependability on massive datasets. In this regard, cloud–services such as cloud storage and computational resources are emerging as an effective solution. However, when the image data are outsourced to avail such services, there is a privacy concern that the data should be kept protected not only during transmission but during computations as well. We extended the applications of the proposed PE algorithm for privacy-preserving medical image analysis in [10]. We have implemented a binary classifier based on EfficientNetV2 model for the COVID-19 screening in the chest X-ray images. The proposed PE-based privacy preserving scheme at best introduced a ≈3% drop in the model's accuracy and sensitivity scores.
</span></p> </li>

</ul>


<p align="justify" id="phdThesis"><span style="font-size: 11pt;"><strong>Conclusion</strong></span></p>

<p align="justify"><span style="font-size: 11pt;"> 
For an efficient DL model, a large volume of sample data and high computation resources are needed. These requirements can be fulfilled by taking advantage of powerful infrastructures such as cloud-computing services, to avail high-powered computational resources, and cloud storage services, for adopting collaborative learning. However, this comes with security and privacy concerns as there are potential risks of leakage of privacy-sensitive information associated with outsourcing the data. The existing privacy-preserving schemes have their associated computational cost, communication overhead and specialized design requirement that may reduce data utility and degrade the DL model performance. In addition, given the large volume of data, bandwidth and storage efficiencies should also be considered. Traditional privacy preservation approaches treat the requirements of data transmission and computation separately even though both are necessary to be fulfilled to fully reap the benefits of DL for data-driven applications. Therefore, in this thesis we proposed an end-to-end framework to satisfy the dual requirements (compression and encryption) of a communication system while preserving user’s privacy in downstream applications. Our proposed privacy scheme was based on PE and was compatible with the widely used image compression standard such as the JPEG format. Importantly, the proposed system supported lossless DL model construction which did not modify any of the computation of the original model training algorithm. Therefore, it can be used with the existing state-of-the-art DL models without any modification. We presented applications for the proposed privacy scheme in three different domains. For natural images classification task, our proposed PE-based privacy preserving scheme at best introduced a decrease of ≈5% in the prediction accuracy of the trained models. For face recognition application, the proposed privacy preservation scheme delivered the same recognition accuracy as that of the plain images. For COVID-19 screening in CXR images, the proposed PE-based privacy preserving scheme at best introduced a ≈3% drop in the model's accuracy and sensitivity scores.
</span></p>

<hr style="height:1px;border-width:0;color:gray;background-color:gray">

<p align="justify" id="currentWork"><span style="font-size: 12pt;"><strong>Current Work</strong></span></p>
<p align="justify"><span style="font-size: 11pt;">
Currently, I am working on representation learning to quantify perceptual distortions in wirelessly transmitted images. This is motivated by an observation that the existing Image Quality Assessment (IQA) metrics either rely on or are optimized to coincide with human judgment and do not account for the perceptual distortions (for example, because of imperfect communication system) that are responsible for the degradation in DL model performance. Given the popularity of DL solutions in various domains, it is necessary to quantify perceptual loss in distorted images using machine perception. Towards this we proposed an IQA metric that compares the perceptual similarity between distorted and original images in the semantic feature space defined by latent-variable models. It is anticipated that the proposed method will give an important indication of a DL model performance implemented on a remotely located server for a downstream application and can be used to optimize the parameters of a communication system.
</span></p>


<hr style="height:1px;border-width:0;color:gray;background-color:gray">

<p align="justify" id="currentWork"><span style="font-size: 12pt;"><strong>References</strong></span></p>
<p align="justify"><span style="font-size: 11pt;">

[1] I. Ahmad and S. Shin, “A novel hybrid image encryption–compression scheme by combining chaos theory and number theory,” Signal Processing: Image Communication, vol. 98, p. 116418, Oct. 2021, doi: 10.1016/j.image.2021.116418. <br>
[2] I. Ahmad, B. Lee, and S. Shin, “Analysis of Chinese Remainder Theorem for Data Compression,” in 2020 International Conference on Information Networking (ICOIN), Barcelona, Spain: IEEE, Jan. 2020, pp. 634–636. doi: 10.1109/ICOIN48656.2020.9016442. <br>
[3] I. Ahmad and S. Shin, “Noise-cuts-Noise Approach for Mitigating the JPEG Distortions in Deep Learning,” in 2023 International Conference on Artificial Intelligence in Information and Communication (ICAIIC), Bali, Indonesia: IEEE, Feb. 2023, pp. 221–226. doi: 10.1109/ICAIIC57133.2023.10067012. <br>
[4] I. Ahmad, W. Choi, and S. Shin, “Comprehensive Analysis of Compressible Perceptual Encryption Methods—Compression and Encryption Perspectives,” Sensors, vol. 23, no. 8, p. 4057, Apr. 2023, doi: 10.3390/s23084057. <br>
[5] I. Ahmad and S. Shin, “IIB–CPE: Inter and Intra Block Processing-Based Compressible Perceptual Encryption Method for Privacy-Preserving Deep Learning,” Sensors, vol. 22, no. 20, p. 8074, Oct. 2022, doi: 10.3390/s22208074. <br>
[6] I. Ahmad and S. Shin, “Perceptual Encryption-based Privacy-Preserving Deep Learning in Internet of Things Applications,” in 2022 13th International Conference on Information and Communication Technology Convergence (ICTC), Jeju Island, Korea, Republic of: IEEE, Oct. 2022, pp. 1817–1822. doi: 10.1109/ICTC55196.2022.9952589. <br>
[7] I. Ahmad and S. Shin, “Encryption-then-Compression System for Cloud-based Medical Image Services,” in 2022 International Conference on Information Networking (ICOIN), Jeju-si, Korea, Republic of: IEEE, Jan. 2022, pp. 30–33. doi: 10.1109/ICOIN53446.2022.9687214. <b>[Best Paper Award] </b><br>
[8] I. Ahmad and S. Shin, “A Perceptual Encryption-Based Image Communication System for Deep Learning-Based Tuberculosis Diagnosis Using Healthcare Cloud Services,” Electronics, vol. 11, no. 16, p. 2514, Aug. 2022, doi: 10.3390/electronics11162514. <br>
[9] I. Ahmad, E. Kim, S.-S. Hwang, and S. Shin, “Privacy-Preserving Surveillance for Smart Cities,” presented at the The 13th International Conference on Ubiquitous and Future Networks, Barcelona, Spain, Jul. 2022. <br>
[10] I. Ahmad and S. Shin, “Perceptual Encryption-based Privacy-Preserving Deep Learning for Medical Image Analysis,” in 2023 International Conference on Information Networking (ICOIN), Bangkok, Kingdom of Thailand: IEEE, Jan. 2023, pp. 224–229. <b>[Best Paper Award] </b><br>
</span></p>



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