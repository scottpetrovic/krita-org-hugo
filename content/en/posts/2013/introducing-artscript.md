---
title: "Introducing ArtScript"
date: "2013-12-13"
---

Today, we have Ivan Yossi, the maintainer of the Windows XP packages of Krita over here to introduce a utility he's been working for some time that's really interesting for aritsts using Krita. Without further ado, here is... Artscript:  

Hi I'm Ivan Yossi, a digital artist and the main developer of Artscript, a tool for digital painters I've been heavily working on lately. A tool I would like to present you.

The idea for Artscript was first developed by David Revoy using kdialog. It was simple and worked quite nice on KDE. I felt attracted to the idea and so I contacted David with my intentions to make the script more universal. I settled on TCL/Tk for making the new dialogs and scripting functions and released the first version a few weeks later.

  
![](https://lh3.googleusercontent.com/-ZF2bvGCDHux5yQsOn6TqBpkrb2i62dkG8am6q58nPbz95qZySlRWH2HZHu7_yhlbUXDKmgSbejQY_VxthvRQxckgbOmY8IkPSuLG_FposbWMg59OFzFKoIRrA)

The script is a small app to easy convert file formats from Gimp, MyPaint, Inkscape and Krita (KRA, XCF, PSD, ORA, SVG, PNG) to universal formats (JPG, PNG, GIF or WEBM). The main target is painters and designers that need quick deployment of their images in different formats for different needs. I tweaked the options to keep the best quality even in the lowest settings.

The available options today include.

- Adding watermark image and/or a text label to the resulting image
    
- Resize one or multiple in one operation.
    
- Make a collage/composition of supplied images into a tiled array.
    

For version 2 I tried to make the use super easy with a simple GUI, keyboard shortcuts and the use of a configuration file for instant deployment of common used options. While I'm not an expert coder and sometimes I tend to break functionality, I feel the script could help all linux artists around.

You can find ArtScript on github: [https://github.com/vanyossi/artscriptk/releases](https://github.com/vanyossi/artscriptk/releases)
