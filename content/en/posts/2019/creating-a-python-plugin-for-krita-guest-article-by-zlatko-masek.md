---
title: "Creating a Python Plugin for Krita: Guest Article by Zlatko Mašek"
date: "2019-03-04"
categories: 
  - "news"
---

# About me:

My name is Zlatko Mašek and I am a programmer originally from Croatia, but I live in Ireland. As you can find on [my blog](https://www.offsetlab.net/) I am interested in art, cooking and social change; not necessarily in that order. I have a master's in Information Science and in university I fell in love with Python working on early stuff with natural language processing. Today it is my programming language of choice and career-wise I am trying to find a more meaningful application for coding that benefits the society. However, Python, as a general purpose programming language, also allows me to tinker on small projects as a hobby for myself. When it comes to art, I was always drawn to it, even if it took me years to get myself doing it. It's currently just a hobby, not a career, and I do things both traditionally and digitally with a graphics tablet. It helps me relax and push my mind into a wandering mode.

# Krita Plug-in:

Ever since Krita allowed scripting in Python, I was eyeing what I could do with it. Since it's using QT and I had no previous experience with it, I wanted to learn a bit about it because I'm programming with Python as my day job. Doing image manipulation to transform images for different usages between different systems is always a fun challenge. I wanted to switch from direct image scripting to a plug-in based workflow so I didn't have to do too much context switching between work-time and hobby-time. Krita being cross-platform also helped because I didn't have to deal with installing Python on operating systems that don't have it pre-installed. The plug-in I made is simple enough. It slices the image and prepares tiles for the usage in a tiling library like [Leaflet](https://leafletjs.com/). You need to make sure that you have a flattened image _saved_ beforehand and it's the last thing you do when preparing for an export. Also make sure that the image is rectangular if you don't want the plug-in to crop it by itself. The plug-in is fired up by going to the Tools -> Scripts -> Krita - Leaflet in the menu bar.

> [![](../images/plugin-selection.png)](https://krita.org/wp-content/uploads/2019/03/plugin-selection.png)![plugin-selection.png](../images/plugin-selection.png)

Then you pick a folder for exporting the tiles and the zoom level. I will use a low zoom level here because the higher the zoom level, the longer it takes for the plug-in to finish processing and it's heavier on the resource usage. You press the "Leafletize" button and wait for it to finish processing.

> ![plugin.png](../images/plugin.png)[![](../images/plugin.png)](https://krita.org/wp-content/uploads/2019/03/plugin.png)

You'd obviously check the output folder then and reload the image back to the saved version since the processing is destructive. The tiles are of 256x256 px dimensions separated in folders that Leaflet can use. Creating a basic JavaScript code to load them is trivial enough. Just to test it, you can create an index.html in the output folder and fill it up with this code that is using the CDN libraries so you don't have to download anything:

<!doctype html>
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width, minimum-scale=1.0, initial-scale=1.0, user-scalable=yes">
    <title>Krita - Leaflet example</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" integrity="sha512-puBpdR0798OZvTTbP4A8Ix/l+A4dHDD0DGqYW6RQ+9jxkRFclaxxQb/SJAWZfWAkuyeQUytO7+7N4QKrDh+drA==" crossorigin=""/>
    <script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js" integrity="sha512-QVftwZFqvtRNi0ZyCtsznlKSWOStnDORoefr1enyq5mVL4tmKB3S/EnC3rRJcxCPavG10IcrVGSmPh6Qw5lwrg==" crossorigin=""></script>
    <style type="text/css">
        body {
            text-align: center;
        }
        #map {
            margin: auto;
            width: 800px;
            height: 600px;
        }
    </style>
  </head>
  <body>
      <div id="map"></div>
      <script type="text/javascript">
          var map = L.map('map').setView(\[0.0, -0.0\], 0);
          L.tileLayer('./{z}/{x}/{y}.png', {
              maxZoom: 4,
              noWrap: true
          }).addTo(map);
      </script>
  </body>
</html>

Loading the HTML is also easy. Here, I will execute the Python server as a module. It has to be in the same folder in order to pick it up.:

python -m SimpleHTTPServer

You can fire up the browser of choice to see the results on [http://localhost:8000/](http://localhost:8000/)

> [![](../images/leaflet.png)](https://krita.org/wp-content/uploads/2019/03/leaflet.png)![leaflet.png](../images/leaflet.png)

I wanted to create that plug-in so I could tile and slice a custom map for a browser based video game that needed a map functionality. It wasn't going to use any fancy libraries for canvas processing, but ordinary web technologies. That's why I made this plug-in. You can get it from the [Krita-Leaflet repository](https://bitbucket.org/zmasek/krita-leaflet/).
