---
layout: page
title: Molecular Visualization
banner: molviz.jpg
description: Digital stage design using real-time projections
permalink: /projects/molviz
image_sliders:
  - molecular_visualization
---

As I worked on the computational problem of folding proteins from their amino-acid sequence, I became interested in the 3D visualization of such molecules, and ended up writing my own protein structure visualizer. This gave me the oportunity to learn about the [OpenGL programming interface](https://opengl.org/){:target="_blank"} to create interactive 3D graphics. My visualizer, called YAPView (Yet Another Protein Viewer), was able to render protein molecules in a variety of representaions, from all-atom to ribbon diagrams:

{% include slider.html selector="molecular_visualization" %}
*Some protein renderings generated with YAPView.*

YAPView's Windows installer and source code (written in Delphi!) are still available on [Sourceforge](https://sourceforge.net/projects/protlib/files/yapview/0.7-BETA/){:target="_blank"}, even though I'm no longer maintaining it. As the name of the tool suggests, there are many other [biomolecular visualization tools](https://www.rcsb.org/pdb/static.do?p=software/software_links/molecular_graphics.html){:target="_blank"}. The idea of using ribbons to represent these complex molecules goes back to the [Jane Richardson](https://research.duke.edu/ribbon-diagrams){:target="_blank"} at Duke University, which originally used this technique to crate beautiful hand-drawn renderings of proteins such as the one below:


<img width="740" src="/assets/images/ribbon-richardson.jpg" style="background:none; border:none; box-shadow:none"/>

Later on, algrithms to generate these ribbon structures automatically with a computer were proposed by Mike Carson and Charles Bugg in the mid-80s:

<img width="600" src="/assets/images/ribbon-algorithm.jpg" style="background:none; border:none; box-shadow:none"/>

Below you can see a screenshot of my implementation of Carson and Bugg's algorithm, in Delphi Pascal:

<img width="600" src="/assets/images/ribbon-code-pascal.png" style="background:none; border:none; box-shadow:none"/>

This code eventually became handy in projects that had nothing to do with protein visualization, like [Latent State](/projects/latent) and [Trazos Club](/projects/trazos) ;-)


