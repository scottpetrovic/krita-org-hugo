---
title: "Pencils down! Or what our Summer of Code students have achieved"
date: "2020-09-09"
categories: 
  - "news"
---

The final evaluations of the Google Summer of Code projects are open now; it's pencils down time for the students. In 2020, four students have worked really hard on four really exciting projects, of course, so let's take a look at their achievements!

## Dynamic Fill Layers in Krita using SeExpr

**Amy Spark** implemented a new type of fill layers. Fill layers are dynamically generated layers in Krita. SeExpr is a library created by Disney to generate patterns, with a set of UI elements written in Qt.

As part of this project, Amyspark has made it possible to translate SeExpr, as well as improving the provided the widgets and usability of the expression editor.

But the main work was, of course, creating the new fill layer type, making Krita preview your SeExpr script and making it possible to save scripts as resources, so you can share your scripts with others!

<iframe src="https://diode.zone/videos/embed/b441f360-0b94-470a-8365-5a5f44b3a617" width="560" height="315" frameborder="0" sandbox="allow-same-origin allow-scripts allow-popups" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe>

Hugely impressive work, and real fun to play with. Everything is already in the nightly builds, too, and will be available in Krita 4.4 which we'll release in September! You can also read Amyspark's [report,](https://community.kde.org/GSoC/2020/StatusReports/LeonardoEmanuelSegovia) or head over to the manual:

\[caption id="attachment\_10913" align="aligncenter" width="1024"\][![](/images/posts/2020/1096px-SeExpr_manual_1-1024x840.jpg)](https://docs.krita.org/en/tutorials/seexpr.html) SeExpr Manual\[/caption\]

## Integrating the MyPaint Brush Engine in Krita

**Ashwin Daikata** has successfully integrated the [MyPaint](http://mypaint.org/) brush engine in Krita. This is actually the second time we have a MyPaint based brush engine, but the previous engine was very slow and based directly on the MyPaint internal code. When the MyPaint developers separated their brush engine into a library, it became possible to once more integrate the engine in Krita.

[![](/images/posts/2020/Particules_eraser_2.png)](https://krita.org/wp-content/uploads/2020/08/Particules_eraser_2.png)

Ashwin has done a really good job: when painting on default 8 bit RGBA layers, the brushes are as fast as in MyPaint itself.

[![](/images/posts/2020/preset_selector.png)](https://krita.org/wp-content/uploads/2020/08/preset_selector.png)And they not only behave exactly right, you can even edit and create brushes right in Krita!

[![](/images/posts/2020/Preset_editor-1024x568.png)](https://krita.org/wp-content/uploads/2020/08/Preset_editor.png)

The MyPaint brush engine will be merged soon, and will be released Krita 5.0, planned for this year.

Ashwin has prepared a [report](https://community.kde.org/GSoC/2020/StatusReports/AshwinDhakaita) on his work, well worth a read!

## A Storyboard Docker for Krita

**Saurabh Kumar** implemented storyboard functionality for Krita. This includes a docker to manage the storyboard, piggy-backing on Krita's animation feature to switch the canvas between boards and exporting the storyboards to SVG and PDF -- including specifying a layout .

\[caption id="attachment\_10957" align="aligncenter" width="601"\][![](/images/posts/2020/Storyboard_custom_options.png)](https://krita.org/wp-content/uploads/2020/09/Storyboard_custom_options.png) Specifying a layout\[/caption\]

You can view just the thumbnail, just the comments, or everything together:

\[caption id="attachment\_10956" align="aligncenter" width="473"\][![](/images/posts/2020/Storyboard_row_mode.png)](https://krita.org/wp-content/uploads/2020/09/Storyboard_row_mode.png) Storyboard docker in row mode\[/caption\]

And Saurabh has his [report](https://community.kde.org/GSoC/2020/StatusReports/SaurabhKumar) as well.

## SVG Mesh Gradients in Krita

**Sharaf Zaman** returns after his 2019 project porting Krita to Android with something completely different: the second independent implementation of mesh gradients. The first implementation was [done in Inkscape](http://tavmjong.free.fr/blog/?p=316) by Tavmjon Bah.

Of course, the trickiest part was actually rendering the gradients:

\[caption id="attachment\_10919" align="aligncenter" width="296"\][![](/images/posts/2020/Screenshot_2020-07-23_11-46-06.png)](https://krita.org/wp-content/uploads/2020/08/Screenshot_2020-07-23_11-46-06.png) A mesh gradient imported from Inkscape\[/caption\]

The main problems with rendering were due to differences between the 2D graphics libary used to actually paint the pixels, but Sharaf overcame the issues and now Krita renders the mesh gradients just like Inkscape.

But before that could be done, Sharaf had to extend Krita's SVG parster with support for the mesh gradient extensions. After parsing and rendering came saving.

And then, of course, creating mesh gradients in Krita needed an actual UI:

[![](/images/posts/2020/Handles-meshgradient-1024x554.png)](https://krita.org/wp-content/uploads/2020/08/Handles-meshgradient.png)

You'll find the the options in the vector object tool options docker:

![](/images/posts/2020/Tooloptions-meshgradient.png)

Please check out Sharaf's [final report](https://community.kde.org/GSoC/2020/StatusReports/SharafZaman) for more details!
