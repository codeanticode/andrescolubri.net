---
layout: page
title: Syphon libray for Processing 
banner: syphon.jpg
description: Processing library to share graphics between Mac applications
permalink: /projects/syphon
---

[Syphon](http://syphon.v002.info/){:target="_blank"} is an open source Mac OS X technology that allows applications to share frames - full frame rate video or stills - with one another in realtime. I wrote a [Processing library](https://github.com/Syphon/Processing) that easily allows using Syphon from a Processing sketch and share frams with any other Syphon-enabled application on a Mac computer. The following video from [this tutorial](https://vdmx.vidvox.net/tutorials/vdmx-processing-syphon-osc-intro) shows how to install the library and use it to connect Processing with the [VDMX VJ software](https://vidvox.net/):


<div style="padding:75% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/252549790?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

Below you have the documentation of an interactive installation using Syphon:

<div style="padding:75% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/74480202?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

The power of Syphon lies in that it allows combining the strenghts of different tools for real-time graphics, and thus creating visuals that would not be possible or very hard to achieve with a one single tool. I have used the Syhon library myself to quickly get dome projections going by sharing the Processing output with mapping sofware, as described in [this blog post]({{ site.url }}/blog/2017/06/17/full_some_projection_with_syphon.html){:target="_blank"}. A similar technology is available on Windows through the [Spout library](http://spout.zeal.co/).

