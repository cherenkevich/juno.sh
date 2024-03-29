---
layout: post
title: "Juno Connect v.1.0.9 beta"
description: "A new beta release of Juno Connect, Jupyter/IPython client for iPad."
image: /images/blog/demo_notebooks_v_1_0_6.png
lang: "en_GB"
date: 2017-11-20 12:00:00
author: Alex Staravoitau
---

Today we are releasing Juno Connect v.1.0.9 update to our beta testers! This release includes improved typography, visual design updates, as well as a number of bug fixes and performance improvements. <!--more-->

<div style="text-align: center;">
	<img src="{{ "/images/blog/demo_notebooks_v_1_0_6.png" | prepend: site.baseurl }}" alt="Juno Connect demo notebooks">
</div>

## What's new
* Bundled notebooks. We have included a couple of introductory notebooks in the app, so that you can try Jupyter without any preliminary configuration!
* Undo/Redo. Can't believe it took us so long to fix that one. Undo finally works in individual cells!
* Typography. We have worked on fonts across notebooks, so they should be easier to work with on your mobile devices.
* Various visual design changes and usability improvements. As negligible as they may seem, those will let us bring more substantial features in the next couple of releases!
* Fixes for a number of smaller bugs and issues reported by our beta testers.

## Public beta
If you would like to participate and try out **Juno Connect** early, simply [sign up here](/#mce-EMAIL){:target="_blank"} and don't forget to confirm your e-mail address. We will then send you instructions on how to install **Juno Connect** build on your iPad. You will also get updates with new features as soon as they go live.

Unless it's just demo notebooks that you are after — please, keep in mind that you will need a remote Jupyter Notebook server to use the app, as it doesn't allow running notebooks locally on your iPad. If you have a self-signed SSL certificate which doesn't work in Safari on iOS, take a look at our [step-by-step instructions](/ssl-self-signed-cert){:target="_blank"} on how to configure certificates and enable SSL, so that you are able to connect to your server from iPad. In case you still can't get it to work, please, check out [Jupyter documentation](http://jupyter-notebook.readthedocs.io/en/latest/public_server.html){:target="_blank"} on running a notebook server, or send an e-mail to [help@juno.sh](mailto:help@juno.sh).
