---
layout: page
title: Espacio de Datos
banner: espacio.jpg
description: Fulldome visualization and sonification of data exploration with Mirador
permalink: /projects/espacio
image_sliders:
  - espacio_de_datos
---

This project is a fulldome video piece generated from infectious disease data I study as part of [my scientific research]({{ site.url }}/blog/2018/05/07/lassa_fever_in_nigeria_lessons_learnt.html){:target="_blank"}. It has been shown at the [+CODE 2018 festival](https://pluscode.cc/festival-code-2018/){:target="_blank"} in Buenos Aires, Argentina. It was originally comissioned by Cristian Reynaga and Merlina Rañi, organizers of the festival. Espacio de Datos was also shown at the 2018 edition of the [Domo Lleno festival](https://domolleno.gov.co/node/29){:target="_blank"} in Bogotá, Colombia, the [9th International Festival of Science Visualization](https://www.ifsv.org/en/index.html){:target="_blank"} in Tokyo, Japan, in February 2019, and finally at the [Elektra Festival XX](https://www.elektramontreal.ca/festival){:target="_blank"} in Montréal, Canada, in June 2019.


The visuals represent data exploration conducted with the visualization software [Mirador](https://fathom.info/mirador){:target="_blank"}. Points stand for variables in the dataset, and their relative movements are calculated by evaluating the ["information distance"]({{ site.url }}projects/metric){:target="_blank"} between each pair of variables. Blue lines indicate statistically significant correlations, which determine constellation-like patterns, or ["asterisms"](https://en.wikipedia.org/wiki/Asterism_(astronomy)){:target="_blank"}. The audio was created by sound artist [Mene Savasta](https://menesavasta.com.ar/){:target="_blank"} specifically for this piece. [This blog post]({{ site.url }}/blog/2019/06/17/espacio-de-datos.html){:target="_blank"} goes over the inspiration and process of creating the piece. 


{% include slider.html selector="espacio_de_datos" %}
*Pictures from the fulldome show during the +CODE festival in Buenos Aires.*

A 1024x1024 render of the video shown at the planetarium can be played back below:

<div style="padding:100% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/304056470?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

The video was created with a custom [Processing](https://processing.org/){:target="_blank"} program, including a [fish-eye shader]({{ site.url }}/projects/dome){:target="_blank"} to output the image with the correct deformation to project on a 180 degree dome.



