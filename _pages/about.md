---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<br>
<p align="justify">
I am pursuing a PhD degree in computer engineering from the Chosun university, Korea, under the supervision of Prof. Seokjoo Shin. I am a research assistant with the Dept. of Computer Engineering, Chosun univesirty, where I am a part of the Wireless Communication and Networking (WHYNET) group.

<br><br>
Currently, I am working on <i>Perceptual Encryption-based Privacy-Preserving Deep Learning applications</i>.

<br><br>
My research focuses on <b>Image Compression</b>, <b>Image Encryption</b>, <b>Image Communication</b>, and <b>Privacy-Preserving Deep Learning</b>.
</p>

<br>
<h2>News&#128276;</h2>&#128276;

&#128307; We submitted a paper to the ISCIT 2023 conference &#9203;
&#128306; We submitted a paper to the KICS Summer 2023 conference &#9203;
&#11093; Our paper <i><a href="https://www.mdpi.com/1424-8220/23/8/4057" target="_blank" style="color:#64B2CB">'Comprehensive Analysis of Compressible Perceptual Encryption Methods—Compression and Encryption Perspectives'</a></i>  is now online.
&#9899; We submitted a paper to the KICS Summer 2023 conference &#9203;


<b>Performance Analysis of Cloud-based Deep Learning Models on Images Recovered without Channel Correction in OFDM System</b><br>
Ijaz Ahmad, Nazmul Islam and Seokjoo Shin <br>
IEEE Asia Pacific Conference on Communication (APCC): 255-259, Oct. 2022. <br>
[<a href="https://ieeexplore.ieee.org/abstract/document/9943691" target="_blank" style="color:#64B2CB">Full Article</a>]
[Summary]({{ site.baseurl }}{% link _publications/2022-10-19-paper-title-number-IC12.md %})<br>

<u>Description</u>: <i> Channel correction plays an important role in performance of wireless communication systems.<span id="dotsC12">...</span><span id="moreC12" style="display:none">In this study, we considered the otherwise to bypass channel estimation of an Orthogonal Frequency Division Multiplexing (OFDM) based image communication system designed to enable cloud-based deep learning (DL) computation
.</span></i>
<button onclick="moreLessFtn('dotsC12','moreC12','moreLessBttnC12')" id="moreLessBttnC12" style="border:none; background-color:transparent; color:dodgerblue">Read more</button>

<br>



<script>
function moreLessFtn(dotsID, moreID, myBtnID) {
  var dots = document.getElementById(dotsID);
  var moreText = document.getElementById(moreID);
  var btnText = document.getElementById(myBtnID);

  if (dots.style.display === "none") {
    dots.style.display = "inline";
    btnText.innerHTML = "Read more"; 
    moreText.style.display = "none";
  } else {
    dots.style.display = "none";
    btnText.innerHTML = "Read less"; 
    moreText.style.display = "inline";
  }
}
</script>