---
layout: post
title: "Open beta for a new app 🚀"
description: "TestFlight beta for Juno with embedded Jupyter"
image: /images/blog/juno_embedded_jupyter.png
lang: "en_GB"
date: 2019-07-11 12:00:00
author: Alex Staravoitau
---

Although Juno has been designed as a remote client, running Jupyter locally on your iPhone or iPad has always been an interesting opportunity. That's why over the last year I've been working on a new app, which is based on Juno, but doesn't need an external server to run: all computations happen locally, right on your iOS device. I'm pleased to announce that this app is now in open beta! 
<!--more-->

#### Features

You can edit and run notebooks using embedded **Python** kernel. The app ships with **NumPy** and **Matplotlib** libraries pre-installed, and you can also add pure-Python modules manually, see issue tracker's README for more info. Due to a self-contained nature of the app, it allows a much better OS integration, among other things:

* **Powerful notebook editor**. The app uses notebook editor from Juno client, utilising hardware keyboard support, code completion, on-screen keyboard extension and other existing features.
* **Works everywhere**. Just as the Juno client, the new app works on all devices, supporting both iPhone and iPad.
* **File management**. The app offers a fully-functioning iOS file browser, similar to the one in Files app.
* **Open notebooks from anywhere**. The app registers itself with Jupyter notebook document type, so you can open notebooks from anywhere in iOS with a single tap.
* **Edit notebooks in place**. Whenever you open a notebook, all your changes will be saved in the original location — even when opened from another app!
* **Access notebook directory**. By default, you can only access notebook's directory when running notebooks in the app's sandbox, i.e. in app's folder on device or in iCloud. This means that you won't be able to read or write files from code in notebook, if said notebook is in another app's sandbox — say, when you are editing in place. However, you can now explicitly grant access to the notebook's directory by tapping the folder-lock button and selecting the folder with your notebook. As easy as that!

#### Call for beta testers
If you would like to help test it, please install using **TestFlight** link below:

<a href="https://testflight.apple.com/join/XRjYzgMU" target="blank">
	<b>https://testflight.apple.com/join/XRjYzgMU</b>
</a>
{: style="text-align: center;"}

#### Bug reporting
Please, keep in mind that the app is still in active development, so quite a few things might not work. Please, report any requests or defects you encounter by opening an issue in tracker (you can use the link below, or go to _About -> Report an issue_ in the app). Also, please report any modules or packages that you would like to be pre-installed. Don't forget to search for existing issues first, in case someone else has reported your thing already. **Issue tracker** is available on GitHub:

<a href="https://github.com/rationalmatter/Juno-Issue-Tracker" target="blank">
	<b>https://github.com/rationalmatter/Juno-Issue-Tracker</b>
</a>
{: style="text-align: center;"}

#### What happens to Jupyter client?
In case you are wondering how it fits with Juno, the Jupyter client app, which is currently available on App Store — worry not, it's not going anywhere! Juno with embedded Jupyter will be released as a separate app some time later this year; however, Juno the Jupyter client will keep evolving on its own. To avoid confusion, it will be rebranded as Juno Connect in one of the next few updates (and will get a cool new icon!). Both apps will share new features whenever possible, as they are using the same notebook editor component under the hood.

<span style="display:block; height: 20px;"></span>
![Juno demo notebooks](/assets/img/blog/juno_embedded_jupyter.png)
{: style="text-align: center;"}
<span style="display:block; height: 20px;"></span>

Thanks again for your support, and I hope you are as excited as I am about how Juno apps are moving forward! Stay tuned for more updates. 😉