---
layout: page
title: Mirador
banner: mirador.jpg
description: Tool to explore complext dataset
permalink: /projects/mirador
image_sliders:
  - acegid_mirador
---

[Mirador](https://fathom.info/mirador/){:target="_blank"} is a visualization tool I have created for exploratory analysis of complex tabular datasets that include mixture of discrete and continuous variables. Mirador started from a collaboration between the [Sabeti Lab](https://www.sabetilab.org/){:target="_blank"} and [Fathom Information Design](https://fathom.info/){:target="_blank"}. I have been using this tool in my own research to perform quick checks of correlation patterns between pairs of variables and univariate distributions. 

<div style="padding:55% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/110323353?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

My goal with Mirador is to create an "universal visualizer", and by that I mean a tool capable to handle a wide range of datasets and allowing users to explore “all the data” at once with no prior knowledge of which patterns could be the most “interesting”. This goal poses a number of challenges though: how to consistenly represent ([qualitatively](https://fathom.info/notebook/6246/){:target="_blank"} and [quantitatively](https://fathom.info/notebook/7028/){:target="_blank"}) associations between variables of different types, and how to account for "false discoveries", which are the result of looking at the data long enough until finding a significant correlation that's not real but the result of chance (see [P-Hacking](https://fivethirtyeight.com/features/science-isnt-broken/){:target="_blank"}). 

Models, and more generally any kind of insights, derived from visual exploratory analysis will be affected by biases and significance over-estimation unless the false discovery rate in interactive visualization is accounted for. From [Daniel Russo and James Zou in 2015](https://arxiv.org/abs/1511.05219){:target="_blank"}: _"Any data-exploration renders standard statistical theory invalid."_ This is an ongoing area of research and I'm using Mirador as an testing platform to evaluate new methodologies to control for [false discovery rate in interactive exploration](https://arxiv.org/abs/1612.01040){:target="_blank"}.

We have also used Mirador in data analysis workshops as part of the African Center of Excellence for Genomics of Infectios Disease's (ACEGID) [training program](https://acegid.org/index.php?active=page&pgcat=training){:target="_blank"} at Harvard and the Broad institute:


{% include slider.html selector="acegid_mirador" %}
*ACEGID data analysis workshop with Mirador.*

Mirador is open-source and installers are freely available for [Windows](https://github.com/mirador/mirador/releases/tag/latest-windows){:target="_blank"}, [Mac](https://github.com/mirador/mirador/releases/tag/latest-macos){:target="_blank"}, and [Linux](https://github.com/mirador/mirador/releases/tag/latest-linux){:target="_blank"}, as well as its source from [GitHub](https://github.com/mirador/mirador){:target="_blank"}. You can find tutorials and other resources in its [homepage](https://fathom.info/mirador/){:target="_blank"}.
