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


<h2>An unordered HTML list</h2>

<span>
<ul align="justify">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
  <span id="dots1">...</span>
</ul>
</span>

<span id="more1" style="display:none">
<ul align="justify">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
</span>
<button onclick="moreLessFtn('dots1','more1','moreLessBttn1')" id="moreLessBttn1" style="border:none; background-color:transparent; color:dodgerblue">Read more</button>



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