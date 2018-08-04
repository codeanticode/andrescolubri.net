---
layout: page
title: Dome Projection
banner: dome.jpg
description: Tools to project real-time graphics on semicircular domes
permalink: /projects/dome
image_sliders:
  - endo_corral_augier
---

I have created a number tools for dome projection, following the [amazing resources on the topic](http://paulbourke.net/dome/){:target="_blank"} by [Paul Bourke](http://paulbourke.net/){:target="_blank"}. The [Planetarium library](http://processing.andrescolubri.net/libraries/planetarium/){:target="_blank"} is one of such tools that can be used to create a 360 degree rendering of a Processing sketch, suitable to display on a full dome like those available in science planetariums. Artist [Alba Corral](https://blog.albagcorral.com/){:target="_blank"} recently used this library for the visuals of the live piece [end(O)](https://www.elektramontreal.ca/augier-corral-endo){:target="_blank"} that she and electronic musician [Alex Augier](http://www.alexaugier.com/){:target="_blank"} performed at the Elektra 2018 festival in Montreal. I contributed with some custom code for shader rendering that used during some passages of the piece.


{% include slider.html selector="endo_corral_augier" %}
*Pictures from end(O)'s performance at the [Satosphere](https://sat.qc.ca/en/satosphere){:target="_blank"}.*

Another option to easily display Processing sketches on full domes is to use the [Syphon]({{ site.url }}/projects/syphon){:target="_blank"} library in combination with a simple fish eye shader derived from one of Paul Bourke's [dome projection algorithms](http://paulbourke.net/dome/fisheye/){:target="_blank"}. This is detailed in [this post]({{ site.url }}/blog/2017/06/17/full_some_projection_with_syphon.html){:target="_blank"} in my blog.

<img width="800" src="{{ site.url}}/assets/posts/fulldome_syphon/hayden-fulldome-processing.jpg" style="background:none; border:none; box-shadow:none"/>

Jason Fletcher's [The Fulldome Blog](https://thefulldomeblog.com/){:target="_blank"} also has plenty of useful resources on dome projection, including 360° video, open source tools, news and shows. 
