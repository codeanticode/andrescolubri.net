---
layout: page
title: GLGraphics &amp; GSVideo libraries for Processing
banner: p5glggsv.jpg
description: Processing libraries for real-time graphics and video
permalink: /projects/p5glggsv
image_sliders:
  - glgraphics_gsvideo_showcase
---

The [GLGraphics](http://glgraphics.sourceforge.net/){:target="_blank"} and [GSVideo](http://gsvideo.sourceforge.net/){:target="_blank"} libraries were my first contributions to the [Processing project](https://processing.org/){:target="_blank"}, developed mostly while I was doing an MFA at the [Design Media Arts](https://dma.ucla.edu/){:target="_blank"} program at UCLA between 2007 and 2009.

Processing is a software sketchbook and a language for learning how to code within the context of the visual arts, as well as a prototyping and production tool for artists and designers. As such, it looks for a balance between ease of use and performance. Some of my projects at UCLA, inspired by my earlier work with Moldeo, required real-time graphics and video, which where areas that, at the time, Processing had limitations in terms of performance. So I wrote these libraries in order to expand the real-time capabilties of Processing for visual and video work, with GLGraphics simplifying the use of advanced OpenGL features, including GLSL shaders, and GSVideo wrapping a powerful cross-platform multimedia toolking called [GStreamer](https://gstreamer.freedesktop.org/){:target="_blank"}. Many people find these libraries useful and created numerous projects that would I had not imagined before:


{% include slider.html selector="glgraphics_gsvideo_showcase" %}
*A showcase of projects using GLGraphics and GSVideo.*

And below some videos:

<div style="padding:55% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/74066023?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<br>

<div style="padding:55% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/32760578?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<br>

<div style="padding:55% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/105277131?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<br>

{% include youtube.html id="g4y6cppFxgo"  width="100%" %}

GLGraphics and GSVideo eventually became part of the core OpenGL renderer and video library in Processing 2 and 3, and the underlying infraestructure that enabled high-performance video playback and capture in GSVideo evolved into a widely used set of [Java bindings](https://github.com/gstreamer-java/){:target="_blank"} for GStreamer. 

I have compiled a list of projects made with GLGraphics and GSVideo [here](https://gist.github.com/codeanticode/6bc0f45a88ac960417328dd0b38cd204){:target="_blank"}, send me an email if you would like to see project added there!

