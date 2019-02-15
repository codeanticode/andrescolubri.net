---
layout: page
title: Espacio de Datos
banner: espacio.jpg
description: Fulldome visualization and sonification of data exploration with Mirador
permalink: /projects/espacio
image_sliders:
  - espacio_de_datos
---

This project is a fulldome video piece generated from infectious disease data I study as part of [my scientific research]({{ site.url }}/blog/2018/05/07/lassa_fever_in_nigeria_lessons_learnt.html){:target="_blank"}. It has been shown at the [+CODE festival](http://pluscode.cc/){:target="_blank"} in Buenos Aires, the [Domo Lleno](http://domolleno.gov.co/){:target="_blank"} festival in Colombia, during November 2018, and the [International Festival of Science Visualization](https://www.ifsv.org/) in Tokyo, between February 17 and 19, 2019. 


The visuals represent data exploration conducted with the visualization software [Mirador](http://fathom.info/mirador){:target="_blank"}. Points stand for variables in the dataset, and their relative movements are calculated by evaluating the ["information distance"]({{ site.url }}projects/metric){:target="_blank"} between each pair of variables. Blue lines indicate statistically significant correlations, which determine constellation-like patterns, or ["asterisms"](https://en.wikipedia.org/wiki/Asterism_(astronomy)){:target="_blank"}. The audio was created by sound artist [Mene Savasta](http://menesavasta.com.ar/){:target="_blank"} specifically for this piece. 

{% include slider.html selector="espacio_de_datos" %}
*Pictures from the fulldome show during the +CODE festival in Buenos Aires.*

A 1024x1024 render of the video shown at the planetarium can be played back below:

<div style="padding:100% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/304056470?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

The video was created with a custom [Processing](https://processing.org/){:target="_blank"} program, including a [fish-eye shader]({{ site.url }}/projects/dome){:target="_blank"} to output the image with the correct deformation to project on a 180 degree dome.



