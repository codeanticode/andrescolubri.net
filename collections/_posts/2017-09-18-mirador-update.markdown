---
layout: post
title:  "Mirador update"
date:   2017-09-18 13:00:00 -0400
categories: visualization, mirador, updates, fixes, tools
comments: true
permalink: /blog/2017/09/18/mirador_update.html
---

Mirador is an open source visualization tool I have been developing at the [Sabeti lab](https://www.sabetilab.org/){:target="_blank"},
in collaboration with [Fathom Information Design](https://fathom.info){:target="_blank"}.
The main goal of this tool is to facilitate the initial exploratory analysis of tabular datasets, by providing a graphical interface
that allows to quickly visualize arbitrary combinations of variable pairs in the data, inspect the effects of confounding factors, and rank
explanatory variables by the strength of their association with any outcome variable of interest. For more information about this project,
take a look at its [homepage](https://fathom.info/mirador){:target="_blank"}.

During the past year, however, I was not able to work on Mirador as much as I wanted. Fortunately, I recently had a chance to come
back to it, and a new release, 1.4.2, is finally available for download. Although it does not introduce any changes or improvements to its UI or
statistics module, it brings some important tweaks and fixes. First of all, Mirador now starts up with a small launch screen providing info about
the project, a link to the home page, and a couple of buttons, one to choose a dataset to work with, and the other to quit:

<center><img src="{{ site.url }}/assets/posts/mirador_update/mirador-1.4.2-welcome-screen.png" alt="Mirador 1.4.2 launch screen"></center>

This simple launch screen could be expanded later on, with a few additional options (e.g.: a list of recently opened files).

More importantly, the previous Windows version of Mirador was broken, as reported by [some users](https://github.com/mirador/mirador/issues/59){:target="_blank"}.
Release 1.4.2 solves this issue, while also introducing support for HiDPI displays:

![Mirador 1.4.2 on Windows]({{ site.url }}/assets/posts/mirador_update/mirador-1.4.2-windows.png)

Another first, this release now includes 32 and 64 bit packages for Linux:

![Mirador 1.4.2 on Linux]({{ site.url }}/assets/posts/mirador_update/mirador-1.4.2-linux.png)

All things considered, Mirador does not try to be a a "big data" or "business analytics" tool, but rather, a platform to experiment with some ideas about visual exploration
of complex datasets (by complex, I mean containing arbitrary combinations of numerical and categorical data), and about using measures of statistical association to guide
the data analysis while minimizing biases due to the search process itself. To give it a try, download the latest installation or zip packages for
[Windows](https://github.com/mirador/mirador/releases/tag/latest-windows){:target="_blank"}, [macOS](https://github.com/mirador/mirador/releases/tag/latest-macos){:target="_blank"}, or
[Linux](https://github.com/mirador/mirador/releases/tag/latest-linux){:target="_blank"}, or check the [Wiki](https://github.com/mirador/mirador/wiki){:target="_blank"} for details on
how to build Mirador from source.
