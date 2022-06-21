---
title: "Krita Sprint: long fight with jaggy lines on OSX"
date: "2018-06-04"
categories: 
  - "news"
---

Two weeks ago we had a very nice and motivating sprint in Deventer, where many members of the Krita team gathered in one place and met each other. Boud has already written a [good post](/item/krita-2018-sprint-report) about it, so I will try to avoid repetitions and only tell a saga of my main goal for this sprint... fix OSX tablet problems!

\[caption id="attachment\_7338" align="aligncenter" width="917"\][![](../images/krita_jagged_lines_on_osx.png)](https://krita.org/wp-content/uploads/2018/06/krita_jagged_lines_on_osx.png) Jagged lines caused by OSX input events compression: main symptom – they disappear as soon as one disables openGL\[/caption\]

### Tablet events compression

Since the very first release of Krita on OSX we've had a weird problem. When the user painted too quickly, the strokes became jagged, or as we call it "bent". The problem happened because tablet events coming from the stylus were being lost somewhere on their way from the driver to Krita.

I should say that this problem has already happened in Krita multiple times on Linux and Windows. In most of the cases it was caused by a Qt update that introduced/activated "input events compression": a special feature of Qt to drop extra tablet/mouse move events if the application becomes too slow to process them in time. This feature is necessary for normal non-painting applications, which do not expect so many tablet move events and can simply sink in them. The main symptom of such compression is that "jagged lines" almost disappear when you disable the openGL canvas, and it was reported that on OSX this symptom is also present. I have already fixed such compression problems multiple times on other systems, so I was heading to the sprint in quite an optimistic mood...

But I became less optimistic when I arrived at the sprint and checked Qt's sources: there was no events compression implemented for OSX! I was a bit shocked, but it was so. Tests proved that all events that arrived to Qt were successfully delivered to Krita. That was a bit unexpected. It looked like OSX itself dropped the events if the application's event loop didn't fetch them from the queue in time (I still think that is the case).

So we couldn't do anything with this compression: it happened somewhere inside the operating system or driver. The only way out was to make the main Krita GUI thread more responsive, but there was another thing... openGL!

### Prevent openGL from blocking Krita's GUI thread

The main symptom of the compression problem, was related to the fact that sometimes openGL needs quite a bit of time to upload updated textures or do the rendering of the canvas. Very simplified, our rendering pipeline looked like this:

1. Image is updated by brush
2. GUI thread uploads the textures to GPU using glTexImage2D or glTexSubImage2D
3. GUI thread calls QOpenGLWidget::update() to start new rendering cycle
4. Qt calls QOpenGLWidget::paintGL(), where we generate mipmaps for the updated textures and render them on screen.

This pipeline worked equally good on all platforms except OSX. If we ran it on OSX, Krita would render the textures with **corrupted mipmaps**. Long time ago, when we first found this issue, we couldn't understand why it happened and just added a dirty hack to workaround the problem: we added glFinish() between uploading the textures and rendering. It solved the problem of corrupted mipmaps, but it made the rendering loop slower. We never understood why it was needed, but it somehow fixed the problem, and the OSX-specific pipeline started to look like this:

1. Update the image
2. Upload textures
3. **Call glFinish() /\* VEEERY SLOOOW \*/**
4. Call QOpenGLWidget::update()
5. Generate mipmaps and render the textures

We profiled Krita with [apitrace](https://github.com/apitrace/apitrace) and it became obvious that this glFinish() is really a problem. It blocks the event loop for long time periods, making OSX drop input events. So we had to remove it, but why it was needed at all? OpenGL guarantees that all GPU calls are executed in chronological order, why do they become reordered?

I spent almost two days at the sprint trying to find out why this glFinish() was needed and two more days after returning back home. I even thought that it was a bug in OSX's implementation of openGL protocol... but the thing was much simpler.

It turned out that we used two separate openGL contexts: one (Qt's one) that uploaded the textures, and the other one (QOpenGLWidget's one) that rendered the image. These contexts were shared, so we thought that they were equivalent, but they are not. Yes, they share all the resources, but the way how they process GPU command queues was undefined. On Linux and Windows they seem to share the commands queue so the commands were executed sequentially; but on OSX the queues were separate, so the commands became reordered and we got corrupted mipmaps...

In real life our pipeline looked like this:

1. **\[openGL context 1\]** Update the image
2. **\[openGL context 1\]** Upload textures
3. **\[openGL context 2\]** Call QOpenGLWidget::update()
4. **\[openGL context 2\]** Generate mipmaps and render the textures /\* renders corrupted mipmaps, because uploading is not yet finished \*/

So we just had to move the uploading into the correct openGL context and the bug went away. [The patch](https://phabricator.kde.org/R37:fb43d4e5be6112c7d9df2ee3f33697d07a614ca6) is now in master and is going to be released in Krita 4.0.4!

### The moral of the story

Always take care about what openGL context you use for accessing GPU. If you are not inside QOpenGLWidget::paintGL(), the context might be random!

PS: Of course, this patch hasn't fixed the tablet problem completely. Compression still happens somewhere deep inside OSX, but it became almost impossible to notice! :)

PPS: The 2018 Krita sprint was sponsored by KDE e.V. (travel) and the Krita Foundation (accommodation and food).

PPPS:

Apple is [deprecating](https://developer.apple.com/macos/whats-new/) OpenGL...
