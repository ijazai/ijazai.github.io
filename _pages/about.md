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
<h2>News</h2>

<ul  align="justify">
	<li>We submitted a paper to the ISCIT 2023 conference.</li>
	<li>We submitted a paper to the KICS Summer 2023 conference.</li>
	<li>Our paper <i><a href="https://www.mdpi.com/1424-8220/23/8/4057" target="_blank" style="color:#64B2CB">'Comprehensive Analysis of Compressible Perceptual Encryption Methods—Compression and Encryption Perspectives'</a></i>  is now online.</li>
	<li>We submitted a paper to the KICS Summer 2023 conference.</li>
</ul>

<span id="dotsC12">...</span>

<h3>Past Events</h3>
<ul align="justify">
	<li>Our paper <i>'Comprehensive Analysis of Compressible Perceptual Encryption Methods—Compression and Encryption Perspectives'</i> got accepted for publication in the Sensors journal! &#127881;&#127881;</li>
	<li>Our paper won one of the best papers award at the ICOIN 2023 conference!&#127881;&#127881;</li>
	<li>Our paper <i>'Noise-cuts-Noise Approach for Mitigating the JPEG Distortions in Deep Learning'</i> got accepted for the ICAIIC 2023 conference! &#127881;</li>
</ul>

<ul id="moreC12" style="display:none"  align="justify">
	<li>Our paper <i>'Robustness of Deep Learning enabled IoT Applications Utilizing Higher Order QAM in OFDM Image Communication System'</i> got accepted for the ICAIIC 2023 conference! &#127881;</li>
	<li>Our paper <i>Perceptual Encryption-based Privacy-Preserving Deep Learning for Medical Image Analysis</i> got accepted for the ICOIN 2023 conference &#127881;</li>
</ul>


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