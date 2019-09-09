---
layout: doc
title: "Install Python packages in Juno"
description: "Follow these steps to install pure Python packages from PyPI with Juno on your iPad or iPhone"
image: ""
lang: "en_GB"
date: 2019-09-10 10:00:00
author: Alex Staravoitau
---

Although Juno ships with a few important libraries pre-installed, such as NumPy, Matplotlib and Pandas, you can also install additional pure Python modules yourself. To make this process a bit easier, Juno comes with a package installer, letting you browse and install packages from PyPI ([Python Package Index](https://pypi.org){:target="_blank"}).  

<!--more-->

## How to install

There are two ways to install additional pure Python packages in Juno:

* Manually put package sources into _/site-packages_ directory in Juno's on-device storage.
* Install using Juno's PyPI package installer.

<div style="text-align: center;">
    <img src="{{ "/images/docs/pypi_installer.png" | prepend: site.baseurl }}" alt="Juno's PyPI package installer">
</div>

Juno's package installer is supposed to make installation process a bit easier. Simply provide package name in the search bar (the name you would otherwise use with `pip` command), and Juno will fetch package details from [PyPI](https://pypi.org){:target="_blank"} and, if it has supported distributions, will attempt to install it to your iPad or iPhone.

<div style="text-align: center;">
    <img src="{{ "/images/docs/pypi_package.png" | prepend: site.baseurl }}" alt="PyPI package details">
</div>

## Supported packages

Due to platform restrictions, only pure Python packages are supported — i.e. those that consist exclusively of .py files. If a package relies on native extensions, which need to be compiled for a particular platform, Juno will either display a _"No supported distributions"_ message, or will fail to install the package with an error. Due to restictions above, only purelib Wheel and source Egg distributions are supported.

## Installation

Juno installs packages into _/site-packages_ directory in Juno's on-device storage — into the same location where you can install packages manually.

Under the hood, Juno simply unpacks Wheel distributions, and installs Egg distributions using `distutils`. Wheel distributions are preferred over Egg ones.

## Dependencies

Juno's PyPI installes does **not** install package dependencies automatically, you will need to install each one yourself. Juno will try to list dependencies on the package page, and will let you select and install each one individually. You may do this while other packages are being downloaded or installed, all of them will be handled concurrently.

## Updating packages

Juno doesn't keep track of previously installed packages, and always overwrites whatever package version is currently installed in _/site-packages_.

Furthermore, Juno handles packages that are pre-installed slightly differently. It will not let you update pre-installed modules, and will display a message listing currently installed version on the package page — only for packages that Juno initially ships with.

## Removing packages

Since Juno doesn't keep track of previously installed packages, removing them is a manual process — you can do so by deleting their files and/or folders in _/site-packages_ directory in Juno's on-device storage.

{:refdef: .notice}
<i class="fa fa-info-circle fa-2x" aria-hidden="true" style="color: #CCCCCC; vertical-align: middle;"></i><span style="display:inline-block; width: 8px;"></span> <span>Juno's package installer is clearly **not** a package manager, and does not let you manage previously installed packages or dependencies (although this is certainly something we will be working on). You can think of it as a completely "stateless" installer, which is not aware of what is currently installed, and which simply overwrites whatever happens to be in _/site-packages_ with every installation — leaving package management to the user.</span>
{: refdef}


