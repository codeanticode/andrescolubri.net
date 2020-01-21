---
layout: post
title:  "Espacio de Datos: immersive fulldome visualization"
date:   2019-06-17 12:00:00 -0400
categories: experiments, code, processing, android, ios, cross-platform development, api
comments: true
permalink: /blog/2019/06/17/espacio-de-datos.html
---

[Espacio de Datos](http://andrescolubri.net/projects/espacio) is a site-specific, immersive audiovisual installation, consisting of a fulldome projection and a spatialized audio track that I created in collaboration with sound artist [Mene Savasta](http://menesavasta.com.ar/) for the [+CODE 2018 festival](http://pluscode.cc/festival-code-2018/) in Buenos Aires, Argentina. It was originally comissioned by Cristian Reynaga and Merlina Rañi, organizers of the festival. Espacio de Datos was also shown at the 2018 edition of the [Domo Lleno festival](http://domolleno.gov.co/node/29) in Bogotá, Colombia, the [9th International Festival of Science Visualization](https://www.ifsv.org/en/index.html) in Tokyo, Japan, in February 2019, and finally at the [Elektra Festival XX](https://www.elektramontreal.ca/festival) in Montréal, Canada, in June 2019. This blog post goes in more depth into the background for this project, and the process we followed to create its images and sounds.

<!-- <div style="padding:100% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/386175070?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<script src="https://player.vimeo.com/api/player.js"></script> -->

## Data performance

Our motivation for this piece was the emergence of new observational devices (interactive visualization, dimensionality reduction) that allow us to explore vast data spaces and discover new information structures. Even though the immediate materiality of data is intangible, we can make it tangible through visualization and sonification. This is why we have decided to draw a parallel with astronomy and the celestial constellations as a representational metaphor for the relationships found in the data. By giving shapes and textures to those relationships, we were able to create the audiovisual landscapes that constitute the experience of our performance.

![t-SNE plot]({{ site.url }}/assets/posts/espacio_de_datos/tsne.jpg) Dimensionality reduction methods such as t-SNE became very useful tools to visualize large datasets.

For this piece, I converted a custom visualization software I developed earlier for my own scientific research, [Mirador](https://fathom.info/mirador/), into a “data performance” tool. Working with Mirador to explore scientific datasets as part of my research made me consider how data exploration software work as observational devices of large abstract data-spaces. Eventually, I implemented a generative algorithm that turned the visualization interactions in Mirador into “constellations” or "asterisms" in data space. The idea of this data performance was to take the sequence of user operations in Mirador and transform it into a representation of how the user is navigating through “informational space”. Each variable in the dataset becomes a point or “star”, and the distance between each pair of stars is the statistical correlation between the variables, quantified by their [mutual information](https://en.wikipedia.org/wiki/Mutual_information). As the user explores a dataset in Mirador, some "stars" are no longer visible, and new ones come into view, while their distances change based on modifications they apply through Mirador’s UI -- for example, by filtering out some data points based on the range of a variable, which in turn can affect the association between the rest of the variables. The video below shows that process, with Mirador on the left and the resulting "meta-visualization" on the right, with a [fish-eye filter](http://andrescolubri.net/blog/2017/06/17/full_some_projection_with_syphon.html) applied to it for projection on a semispherical dome surface.

<!-- <div style="padding:100% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/386164355?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<script src="https://player.vimeo.com/api/player.js"></script> -->

After observing these "meta visualizations" of search trajectories in dataspace, can we find constellations unique to each dataset and/or user?

## Sonification

A major challenge was to synchronize a workflow between the two of Mene and I. We did not know each other beforehand, and were separated by thousands of kilometers (Andres in Boston, Mene in Buenos Aires). Through many video calls and exchange of references we agreed on how to approach this project in a “deterritorialized” manner. 

![Mene Savasta]({{ site.url }}/assets/posts/espacio_de_datos/mene.jpg) Mene performing live.

Mene applied an “artisanal” process for the sonification. I provided video renders, and Mene assigned specific sounds to each movement. This was a linear and meticulous work, that allowed Mene to handle the sync at the frame level. As in a Foley exercise, the audio rhythm is proposed by the dynamics of the visible.

The sound palette was informed by the thematic field of the data, which contained anonymized clinical information of patients affected by Lassa fever, a [virual hemorrhagic fever endemic in West Africa](http://andrescolubri.net/blog/2018/05/07/lassa_fever_in_nigeria_lessons_learnt.html). The tragedy of a deadly disease, reduced to indices and values that are then visualized in a cosmic and minimalistic vision. Mene considered these aspects to construct a noisy and glitchy while simultaneously clean palette, where the tragic element is manifested in the dynamic range, such as contrasts and accumulation.

## Visual script

The narrative arc was built around the exploration of a dataset from the initial moment in which the data has no specific form yet, passing through a stage of structure search, and ending with the identification of correlations and the selection of a final hypothesis. The original script for Espacio de Datos included three parts:

* Intro ("Data Bang") ~ 1 minute: Starting blank, you begin to see "data filaments" with no defined structure yet, at the end of the intro these filaments are grouped in points, which represent the variables in the data

![Data constellations]({{ site.url }}/assets/posts/espacio_de_datos/constellations.jpg) Variables in a dataset represented as constellations.

* Main Sequence ("Shannon's Asterisms") ~ 6-7 minutes: Once the variables have been formed, there is a back and forth between the traces of these variables in dataspace, and the "constellations" of points when the user/viewer zooms in to study each pair of variables more closely. The two visual modes (traces and constellations) would be repeated a couple of times in a kind of loop (1 ~ 2 min per cycle).

![Binary system]({{ site.url }}/assets/posts/espacio_de_datos/binary_system.jpg) A pair of variables in the dataset seen as a star binary system.

* Outro ("Hypothesis Crunch") ~ 1 minute: The orbits that started in the previous section start to cover the visual field completely, and there is a final transition to a 3D view, where the orbits define a sort of upwards tunnel at the end, which converges into the final result of the data search, and then to black.

![SAT screening]({{ site.url }}/assets/posts/espacio_de_datos/satosphere.jpg) Screening of Espacio de Datos at the Satosphère at SAT in Montréal, during the Elektra XX festival.






