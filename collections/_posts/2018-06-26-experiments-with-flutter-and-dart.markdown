---
layout: post
title:  "Experiments with Flutter and Dart"
date:   2018-06-26 19:00:00 -0400
categories: experiments, code, processing, android, ios, cross-platform development, api
comments: true
permalink: /blog/2018/06/26/experiments_with_flutter_and_dart.html
---

Some time ago I heard about the [Flutter SDK](https://flutter.io/) for cross-platform mobile development. Having written some apps as part of my research that needed to be available for both iOS and Android, and feeling sometimes frustrated by the fact that I could run Processing sketches on iPhones, I've been interested in this kind of cross-platform SDKs. In fact, I used [Kivy](https://kivy.org/) in the past to create [an app](https://play.google.com/store/apps/details?id=org.broadinstitute.ebolacare) for prognosis of Ebola patients. I liked that Kivy is based on Python and had a simple UI toolkit. However, it was not clear to me if Kivy would allow to create native UIs on iOS and Android, and implementing the Processing API as a Python library that could be used in Kivy seemed difficult at the time (although, with the new [P5 library](https://github.com/p5py/p5) from Abhik Pal, this may be easier now). More recently, I revisited the prognosis app and created a new version which incorporates a more sophisticated visualization of prognosis predictions, as well as patient care and management recommendations. The Android version is [here](https://play.google.com/store/apps/details?id=org.broadinstitute.ebolarisk), and the iOS version [here](https://itunes.apple.com/us/app/ebola-risk/id1376937550). In this case, I ended up creating separate projects for each version, one with Android Studio and the Android SDK from Google, and the other with XCode and the iOS SDK from Apple (and consequently, the development time doubled).

_(To be fair, you can use the [Processing iCompiler](https://itunes.apple.com/us/app/processing-icompiler/id648955851?mt=8) from [Frogg](https://frogg.io/) to write and run Processing sketches directly on your phone, but that's a different use scenario)_

In any case, I was also aware of a number of other existing SDK/frameworks for cross-platform mobile develoment: Xamarin, React Native, Cordova, PhoneGap... but never got enough time to explore at least a few of them in some detail. [React Native](https://facebook.github.io/react-native/) seems very popular nowadays and it is JavaScript-based (there is even a [p5-wrapper](https://www.npmjs.com/package/react-p5-wrapper) that one can use to embed [p5.js](https://p5js.org/) sketches into mobile apps). Coming more from a Java background, and being quite involved in the [Processing for Android](https://android.processing.org/) project, I was looking for something closer to these programming languages/environments. 

Flutter is based on a relatively new language called [Dart](https://www.dartlang.org/), which according to what I found online, Dart is easy to learn for people with experience in Java. So, I decided to give it a try and see how hard would be to write Processing-like sketches with the Dart language together with the Flutter SDK.


I had to get used to Flutter's widget and layout system first, but eventually got to understand the basics of it (the online documentation is [pretty good](https://flutter.io/tutorials/)) and to access lower-level rendering functions in Flutter. The [CustomPainter](https://docs.flutter.io/flutter/rendering/CustomPainter-class.html) class was key to achieve this, as it allows to paint on the canvas of a widget pretty much anything you want:

```dart
class PPainter extends ChangeNotifier implements CustomPainter {
  @override
  void paint(Canvas canvas, Size size) {
    draw(); 
  }

  void draw() {
    // draw anything you want...
  }
}
```

Next, I had to figure out how to animate the drawing, and handle touch events. Luckily, Flutter includes [several built-in classes](https://flutter.io/animations/) to generate UI animations, and I could use them to trigger the drawing in the custom painter on a continuous loop. Finally, [some online code](https://stackoverflow.com/questions/45578209/how-to-touch-paint-a-canvas) gave me enough hints to implement basic input handling:

```dart
class PWidget extends StatelessWidget {
  PPainter painter;
  
  @override
  Widget build(BuildContext context) {
    return new Container(
      child: new ClipRect(
          child: new CustomPaint(
            painter: painter,
            child: new GestureDetector(
              onTapDown: (details) {
                painter.onTapDown(context, details);
              },
              onTapUp: (details) {
                painter.onTapUp(context, details);
              },
            ),
          )
      ),
    );
  }              

```

With these basic elements in place, I was able to start implementing a few functions from the [Processing API](https://processing.org/reference/) in order to create a simple proof-of-concept [Dart package](https://github.com/codeanticode/p5.dart) that encapsulates these functions and can be imported into a Flutter app. In the end, a Dart sketch in Flutter looks surprisingly similar to a Java Processing sketch:

```dart
class MySketch extends PPainter {
  var strokes = new List<List<PVector>>();

  void setup() {
    fullScreen();
  }

  void draw() {
    background(color(255, 255, 255));

    noFill();
    strokeWeight(10);
    stroke(color(10, 40, 200, 60));
    for (var stroke in strokes) {
      beginShape();
      for (var p in stroke) {
        vertex(p.x, p.y);
      }
      endShape();
    }
  }

  void mousePressed() {
    strokes.add([new PVector(mouseX, mouseY)]);
  }

  void mouseDragged() {
    var stroke = strokes.last;
    stroke.add(new PVector(mouseX, mouseY));
  }
}
```

This sketch can be embedded into a minimal UI layout in Flutter, if the purpose is just to show the sketch's output with no other UI components. This is how the sketch above looks like when running on an iPhone and and Android, side to side:

![Running a simple Processing sketch on iOS and Android]({{ site.url }}/assets/posts/flutter_p5dart/draw-p5.dart.jpg)

So far, the experiment proved to be quite succesful! I published the [p5 package](https://pub.dartlang.org/packages/p5) on the Dart Pub repository, so it can be easily imported into any Flutter app. Currently, it only includes a hanful of the Processing API functions, so it is not that useful, but an promising starting point nonetheless!

And in the end, I was able to write a Processing sketch and run it on an iPhone and an Android device from Android Studio, which was pretty satisfying:


![Using Android Studio to debug on an iPhone]({{ site.url }}/assets/posts/flutter_p5dart/androidstudio-iphone.jpg)
