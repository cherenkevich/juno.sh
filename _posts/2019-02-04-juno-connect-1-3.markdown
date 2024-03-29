---
layout: post
title: "Juno Connect 1.3 adds Binder integration"
description: "Juno Connect 1.3 is out bringing Binder integration, kernel switcher and more"
image: /images/blog/appstore_release_v_1_3_0.png
lang: "en_GB"
date: 2019-02-04 12:00:00
author: Alex Staravoitau
---

Juno Connect 1.3 is out now, bringing a whole bunch of new features and bug fixes! Juno Connect now supports [Binder](https://mybinder.org), a service for launching git repositories with notebooks as executable Jupyter environments: you can specify a GitHub or GitLab repo containing Jupyter notebooks you would like to run, and it will be launched as a temporary Jupyter server in Juno Connect. <!--more-->

<span style="display:block; height: 20px;"></span>
<div style="text-align: center;">
	<img src="{{ "/images/blog/appstore_release_v_1_3_0.png" | prepend: site.baseurl }}" alt="Juno Connect demo notebooks">
</div>
<span style="display:block; height: 20px;"></span>

Other changes include:

* **Kernel switcher**. You can now switch between kernels that are available on your server from the Kernel menu in notebook editor.
* **Improved Azure Notebooks integration**. Some new projects couldn't be accessed in Juno Connect, now you should be able to launch all of them.
* **Improved CoCalc integration**. CoCalc connection should now be more reliable in terms of keeping your server alive, and all of your projects should now be displayed with correct status.
* **More control over your custom server**. You can now check the URL your custom server is loading and change it on the go: for instance, if your JupyterHub is using some non-conventional authentication.
* **Unsaved changes alerts**. Juno Connect will now alert you when closing a notebook with unsaved changes, as well as display unsaved changes indicator while editing the notebook.
* **Fix for broken edit mode**. Sometimes Juno Connect couldn't re-enter edit mode when switching between apps in iOS 12, this should now be properly detected and handled.
* **Optional Esc key binding**. You can now map Esc key to your hardware keyboard's Control or Option key, or disable mapping altogether.
* **Improved JupyterLab fallback detection**. Whenever you connect to a JupyterLab server, it should now be correctly identified and accessed via fallback Jupyter Notebook route.
* **Improved kernel reporting**. Previously Juno Connect would sometimes fail to display notebook's kernel, this should now be fixed.
* **R markdown notebooks support**. R markdown files (.rmd) should now open in notebook editor as usual notebooks.
* **Basic HTTP Authentication support**. Juno Connect will now allow you to authenticate against your Jupyter server if it's using Basic HTTP Authentication.
* **Bug fixes and performance improvements**. There are many smaller performance related improvements that might be less prominent, but should still make a difference altogether.

## Juno Connect and Juno Connect Pro
Juno Connect is still available for free, with an optional in-app purchase to unlock Juno Connect Pro if you want to connect to an arbitrary Jupyter server, or use your cloud computing service account — you only purchase it **once for all of your devices**! However, I did my best to make free version of Juno Connect fun as well: you can play with introductory notebooks on Jupyter, Python, NumPy, Matplotlib and SciPy right out of the box without paying anything, those notebooks will be launched on a temporary server just for you using [Binder](https://mybinder.org) service. I plan to keep adding new intoductory notebooks in order to keep things interesting. 🙂

## Juno Connect Needs Your Support
I honestly hope that Juno Connect turns out to be a good fit for your workflow and that you find it useful. If you like Juno Connect, keep in mind that **there are many ways to support its development** and keep it going:

* Consider leaving a positive [review on the AppStore](https://apps.apple.com/app/id1315744137): this honestly means the world to me.
* [Check out Juno Connect on Product Hunt](https://www.producthunt.com/posts/juno-767a5996-5c93-4d62-880d-14268d1093e5) and leave feedback: the more people hear about Juno Connect the better.
* [Share your feedback](mailto:feedback@juno.sh) if you think Juno Connect lacks or needs to improve something, or [get in touch](mailto:help@juno.sh) if you can't get it to work with your Jupyter server, I'll be happy to help. 🙂

<a href="https://apps.apple.com/app/id1315744137" target="blank">
	<span style="display:block; height: 20px;"></span>
    <img class="download-appstore-badge" style="height: 60px;" alt="Download Juno Connect on AppStore" src="{{ "/images/download_black.svg" | prepend: site.baseurl }}">
</a>
{: style="text-align: center;"}


