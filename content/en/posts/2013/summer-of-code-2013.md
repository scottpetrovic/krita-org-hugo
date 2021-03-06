---
title: "Summer of Code 2013"
date: "2013-01-09"
---

You might not have noticed it, but it's that time of the year again. We're in 2013 now and before you know it, Google announces a new Summer of Code. Krita has always participated, and we might participate this year, too. But!

This year students applying for Krita should start getting into the community around January (that is _now_), fixing bugs and getting into the code base. Additionally, if  you think you want to participate with a Krita project, you should be honest with yourself: unless you already have a pretty good level of programming competence, it's not going to work. The easy things are done, now we've got some real challenges! There are no entry-level projects.

As a community, we also really insist on this: you're not in it for the summer, we need a firm commitment that you will maintain your work, branch out into the rest of Krita and join the project for the long term.

In return, you get to work on one of the coolest graphics applications out there, used by professional artists all over the world.

Here are some ideas for good Summer of Code projects -- but keep this in mind, if you use Krita and get passionate about fixing some thing or adding a big feature, then go ahead and propose it. It's passion, persistence and programming power  we're looking for!

- **Rewrite the OpenGL canvas mode**: currently, the OpenGL canvas uses outdated api's and doesn't work on Windows. We need a more modern approach, using the OpenGL 2ES subset to be compatilbe with mobile environments, as well as direct integration of OpenColorIO.
- **Painting and Separation of 3D Textures**: As one of it’s use cases, Krita’s vision statement includes painting textures for 3D. 3D textures are typically comprised of a number of separate black and white, RGB or RGBA images. Thus painting for textures typically requires painting on more than one single layer / channel at a time. For example painting a scratch into a metal surface may require painting black onto the bump channel, another colour on the diffuse channel, and another to the specularity channel (as well as possibly some others such as the displacement channel). All of these are affected simultaneously.  
      
    Currently Krita’s painting system is only able to paint onto single layers at a time and brushes have not been designed in such a way as to allow adjusting multiple channels simultaneously as would be needed. This topic would require looking at how Krita’s current painting system could be extended to paint the necessary adjustments to the channels used in 3D rendering, show the textures created in OpenGL and then export those channels for use in 3D applications.
- **Animation Support**: Animations are a hot topic among Krita users. There is already a start of animation support, but the author did not finish his work. Either you continue his work, or (better) start from scratch. This entails working with animators in our community to design and implement

1. a new file format for storing animations based on Krita's native file format
2. a gui for creating and manipulating animations
3. a system to render animation frames

- **3D Material Image Maps**:3D materials are made up of a bunch of images called image maps. If the user could associate layers as image maps in Krita, and paint on all of them at the same time, artists could paint whole 3D materials - something currently only available in high end 3d apps like zBrush (not even Photoshop / Corel Painter). The trick is that the position of what's painted needs to match on every map/layer, but the colours vary. For example, a scratch on a human characters skin would have a red colour map, a white (=raised) bump map, a light grey (=semi-shiny) specularity map etc, all in the exact same location on the each image map. Traditional methods of trying to create each image from scratch or by manipulating the colour map are very, very slow and painful. A simple version of this could be done as follows:  
    
    1. Each layer has a toggle in the layers docker called "texture map" or similar. This is turned off by default. When active, the brush paints on \*all\* layers that currently have "texture map" active.
    2. When picking a colour, a dropdown lets the user pick "Default" or any active texture map layer. "Default" is just the current behaviour. If the user selects a layer in the dropdown, then the selected colour will be applied to that layer when painting on \*any\* layer.
    3. In the file or layer menu is an option "Export texture maps" which saves each texture map layer as an image. The layer name and extension appended automatically to the file name. For example, on a file called character.kra, the layer titled "colour" would be saved as "character-colour.jpg" (or whatever format was selected).
    
    For step 3, a simple, one click / shortcut, method is vital, as artists often have to check their material in their 3d app every few minutes, and wading through saving 10 layers individually, each with manual file naming and confirming file format settings each time is unacceptably slow. For any artist who requires this level of control, they can use Layers menu -> "Save Layer as Image" already in krita.  
    Allowing artists to paint a single material rather than creating multiple separate image maps by hand, would make Krita formidable for painting 3D textures, and the most advanced open source application for 3D texturing.  
      
    
- **Matte painting**: One of Krita's main use cases is as a professional tool for painting textures and mattes in digital film. Mattes are primarily made of sequences of images generated by a combination of two methods, first by animatable spline based shapes, which currently exists and is being developed in blender, and then after that, by hand painting frames for detailed areas and corrections. The trouble is that no currently maintained FOSS application currently tries to provide the ability to create hand painted mattes. This project is to extend Krita for this purpose. What's needed here is the following:

1. The ability for Krita to load manually selected sequences of color managed images as frames to be represented as a single layer in Krita. Optionally would be the ability to display playback at reduced resolutions to increase performance and to offset the time at which sequences were inserted.
2. A "Timeline" docker which would display the current frame displayed, and allow clicking and dragging to different points in time, updating the image displayed in the canvas to match. Optional would be the ability to zoom and scroll the timeline, mark modified frames on the timeline, playback the image sequence, forwards and backwards as video (most likely only in the openGL mode of Krita or with an external tool like ffplay) and display times in a range of formate EG SMTP, PAL, NTSC, Secam etc.
3. Updating the paint and transparency layer types, so that when Krita is using a frame sequence and one of these layer types is created, they also represent a series of frames rather than just a single image. This could possibly be a toggle switch on layers, much as visibility, alpha lock etc. are now.
4. The ability to save layers that are displaying frame sequences out as frame sequences also, giving them user definable names (eg where to insert the frame number, how many digits to pad).
5. Keyboard shortcuts to move forwards and backwards 1/10/100 frames, to jump to the start and end of the timeline and forward / backwards play if video playback is supported.

- **Cartoon Text Balloon System**: Krita already has two text tools, but neither is suited for creating cartoon balloons. The system should allow the creation of vector-based balloons in different styles. The balloons can contain styled text. The text and balloons should be translatable and a system to select the current language should be created. It should be possible to save the balloon text to a separate file that can be used as input for translations. Finally, care must be taken to support right-left languages.
