---
layout: post
title:  "Full dome projection with Syphon"
date:   2017-06-17 19:00:00 -0400
categories: experiments, art, dome projection, processing, syphon
comments: true
---

This post is actually reporting on something that happen a while ago (in fact, over a year ago, around the time when I unsuccessfully tried to restart my blog), but I think is still worth bringing it up now, as my blog is finally up and running again :-) So, back then Jason Fletcher, Science Visualizer & Live Presenter at the [Charles Hayden Planetarium](https://www.mos.org/planetarium){:target="_blank"} at the Boston Museum of Science and author of [The Full Dome Blog](http://thefulldomeblog.com/){:target="_blank"} gave myself and a few other lucky fellows a tour of the planetarium and allowed us to play with his real-time setup to project on the dome with a single computer running [Blendy Dome VJ](http://www.blendydomevj.com/){:target="_blank"}. 

A really cool thing about his setup is that is was really simply to hook up to. In essence, all one needs is a software that applies a fish eye projection on the visuals to project onto the dome, and then outputs it through [Syphon](http://www.syphon.v002.info/).

For example, in Processing this was quite easy to accomplish using the [Syphon library](https://github.com/Syphon/Processing) and a fish eye shader. The outcome of our experiments can be appreciated in the picture below:

![Visual Computing workshop group]({{ site.url }}/assets/posts/hayden-fulldome-processing.jpg)

In terms of the Processing code, the important elements to have are the Syphon server to send the frames over to Blendy Dome, and a offscreen PGraphics surface to render the scene to, so it can be then transformed with the fish eye shader:

```java
import codeanticode.syphon.*;

SyphonServer server;
PShader fisheye;
PGraphics canvas;

void settings() {
  size(1920, 1920, P3D);
  PJOGL.profile=1;
}

void setup() {
  server = new SyphonServer(this, "Processing Syphon");
  canvas = createGraphics(width, height, P3D);

  fisheye = loadShader("FishEye.glsl");
  fisheye.set("aperture", 180.0);
}

void draw() {
  // Draw the scene into the PGraphics
  canvas.beginDraw();  
  canvas.background(0);  
  canvas.stroke(255, 0, 0);
  canvas.strokeWeight(2);
  for (int i = -width; i < 2 * width; i += 50) {
    canvas.line(i, -height, -100, i, 2 *height, -100);
  }
  for (int i = -height; i < 2 * height; i += 50) {
    canvas.line(-width, i, -100, 2 * width, i, -100);
  }  
  canvas.lights();
  canvas.noStroke();
  canvas.translate(mouseX, mouseY, 200);
  canvas.rotateX(frameCount * 0.01);
  canvas.rotateY(frameCount * 0.01);  
  canvas.box(100);  
  canvas.endDraw(); 
  
  // Apply fish eye transformation on offscreen canvas
  shader(fisheye);
  image(canvas, 0, 0, width, height);
  
  // Send over Syphon
  server.sendScreen();
}  
```

The fish eye shader was inspired by the "Angular Fisheye à la Bourke" sketch from Jonathan Cremieux, as shown in the [OpenProcessing website](https://www.openprocessing.org/sketch/12140){:target="_blank"}, and uses the inverse transform of the angular fisheye as explained in [Paul Bourke's website](http://paulbourke.net/dome/fisheye/){:target="_blank"}:


```glsl
uniform sampler2D texture;
uniform mat4 texMatrix;

varying vec4 vertColor;
varying vec4 vertTexCoord;

uniform float aperture;

const float PI = 3.1415926535;

void main(void) {    
  float apertureHalf = 0.5 * aperture * (PI / 180.0);
  
  // This factor ajusts the coordinates in the case that
  // the aperture angle is less than 180 degrees, in which
  // case the area displayed is not the entire half-sphere.
  float maxFactor = sin(apertureHalf);
  
  // The st factor takes into account the situation when non-pot
  // textures are not supported, so that the maximum texture
  // coordinate to cover the entire image might not be 1.
  vec2 stFactor = vec2(1.0 / abs(texMatrix[0][0]), 1.0 / abs(texMatrix[1][1]));  
  vec2 pos = (2.0 * vertTexCoord.st * stFactor - 1.0);
  
  float l = length(pos);
  if (l > 1.0) {
    gl_FragColor = vec4(0, 0, 0, 1);  
  } else {
    float x = maxFactor * pos.x;
    float y = maxFactor * pos.y;
    
    float n = length(vec2(x, y));
    
    float z = sqrt(1.0 - n * n);
  
    float r = atan(n, z) / PI; 
  
    float phi = atan(y, x);

    float u = r * cos(phi) + 0.5;
    float v = r * sin(phi) + 0.5;

    gl_FragColor = texture2D(texture, vec2(u, v) / stFactor) * vertColor;
  }
}
```