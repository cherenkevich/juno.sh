---
layout: post
title: "Juno Connect v.1.0.5 beta"
description: "A new beta release of Juno Connect, Jupyter/IPython client for iPad."
image: /images/blog/server_configurations_v_1_0_5.png
lang: "en_GB"
date: 2017-10-19 12:00:00
author: Alex Staravoitau
---

Today we are releasing Juno Connect v.1.0.5 update to our beta testers! That's right, the first obvious change is the name, of course. This release also adds support for multiple server configurations, access to a temporary notebook server, as well as includes a number of bug fixes and performance improvements. <!--more-->

<div style="text-align: center;">
	<img src="{{ "/images/blog/server_configurations_v_1_0_5.png" | prepend: site.baseurl }}" alt="Juno Connect server configurations">
</div>

## What's new
* NAME. That's right, our app got a cool new name: it's **Kernels** no more, and is **Juno Connect** instead — as in **Ju**pyter **No**tebook, and as in, well, goddess Juno, wife of Jupiter (the god), and as in probe Juno that was sent to explore Jupiter (the planet) and got there earlier this year.
* Multiple server configurations. You can now configure multiple servers and switch between them in settings.
* Integration with a [temporary Jupyter Notebook service](https://try.jupyter.org) (hosted by Rackspace). Essentially, you can try our app without any preliminary configuration now!
* Various performance improvements, specifically for notebook scrolling.
* Fixes for a number of smaller bugs and issues reported by our beta testers.

## Public beta
If you would like to participate and try out **Juno Connect** early, simply [sign up here](/#mce-EMAIL){:target="_blank"} and don't forget to confirm your e-mail address. We will then send you instructions on how to install **Juno Connect** build on your iPad. You will also get updates with new features as soon as they go live.

Please, keep in mind that you will need a remote Jupyter Notebook server to use the app, as it doesn't allow running notebooks locally. If you have a self-signed SSL certificate which doesn't work in Safari on iOS, take a look at our [step-by-step instructions](/ssl-self-signed-cert){:target="_blank"} on how to configure certificates and enable SSL, so that you are able to connect to your server from iPad. In case you still can't get it to work, please, check out [Jupyter documentation](http://jupyter-notebook.readthedocs.io/en/latest/public_server.html){:target="_blank"} on running a notebook server, or send an e-mail to [help@juno.sh](mailto:help@juno.sh).
