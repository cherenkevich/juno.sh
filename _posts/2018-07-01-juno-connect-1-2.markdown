---
layout: post
title: "Juno Connect 1.2 brings Jupyter to iPhone!"
description: "Juno Connect 1.2 is out bringing Jupyter to iPhone"
image: /images/blog/appstore_release_v_1_2_0.png
lang: "en_GB"
date: 2018-07-01 12:00:00
author: Alex Staravoitau
---

Juno Connect 1.2 is out, and it is our first major update since hitting the AppStore! Juno Connect is now a universal app, which means you can install it on both your iPhone _and_ iPad, bringing Jupyter to all mobile devices running iOS 10.3 or later. _Juno Connect Pro_ works for all of your devices, too: if you previously purchased Juno Connect Pro on iPad, simply restore purchase on your iPhone. Juno Connect supports same features on iPhone as the iPad version, so you will get full access to your Jupyter server wherever you are. <!--more-->

<span style="display:block; height: 20px;"></span>
<div style="text-align: center;">
	<img src="{{ "/images/blog/appstore_release_v_1_2_0.png" | prepend: site.baseurl }}" alt="Juno Connect demo notebooks">
</div>
<span style="display:block; height: 20px;"></span>

Other changes include:
* **Updated interface**. We updated the editor look and feel, so that it is just as easy to navigate on smaller iPhone screens.
* **JupyterLab servers fallback**. Although Juno Connect is designed to work with Jupyter Notebook, it will now work with your JupyterLab servers by automatically requesting classic Notebook interface.
* **Resetting sessions**. You can now clear active web session for your JupyterHub server, or reset all web-based sessions initiated in Juno Connect altogether.
* **Notebook web content fixes**. We fixed a bunch of bugs related to how notebooks handle external web content, which affected some of R plotting packages, embedded videos, cells requesting user input and a few other things. Thanks for reporting!
* **Notebook editing lag**. We fixed a number of issues related to typing lag while editing notebooks, which should improve things for majority of our users.
* **Bug fixes and performance improvements**. There are many smaller performance related improvements that might be less prominent, but should still make a difference altogether.

## Juno Connect and Juno Connect Pro
Juno Connect is still available for free, with an optional in-app purchase to unlock Juno Connect Pro if you want to connect to an arbitrary Jupyter server, or use your cloud computing service account — you only purchase it **once for all of your devices**! However, we did our best to make free version of Juno Connect fun as well: you can play with introductory notebooks on Jupyter, Python, NumPy, Matplotlib and SciPy right out of the box without paying anything, those notebooks will be launched on a temporary server just for you using [Binder](https://mybinder.org) service. We plan to keep adding new intoductory notebooks in order to keep things interesting. 🙂

## We Need Your Support
We honestly hope that Juno Connect turns out to be a good fit for your workflow and that you find it useful. If you like Juno Connect, keep in mind that **there are many ways to support its development** and keep it going:

* Consider leaving a positive [review on the AppStore](https://apps.apple.com/app/id1315744137): this honestly means the world to us.
* [Check out Juno Connect on Product Hunt](https://www.producthunt.com/posts/juno-767a5996-5c93-4d62-880d-14268d1093e5) and leave feedback: the more people hear about Juno Connect the better.
* [Share your feedback with us](mailto:feedback@juno.sh) if you think Juno Connect lacks or needs to improve something. We are listening!

Thank you once again, and we hope you enjoy Juno Connect so far! Stay tuned for more stuff coming later this year. 😉

<a href="https://apps.apple.com/app/id1315744137" target="blank">
	<span style="display:block; height: 20px;"></span>
    <img class="download-appstore-badge" style="height: 60px;" alt="Download Juno Connect on AppStore" src="{{ "/images/download_black.svg" | prepend: site.baseurl }}">
</a>
{: style="text-align: center;"}


