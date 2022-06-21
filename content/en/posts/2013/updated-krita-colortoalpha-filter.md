---
title: "Updated Krita ColorToAlpha filter"
date: "2013-03-15"
---

[![](../images/substitute_bg.png)](http://dimula73.blogspot.ru/2013/03/updated-krita-colortoalpha-filter.html)

[Dmitry Kazakov](http://www.blogger.com/profile/00589041569298003008 "author profile") just updated Krita's **Color to Alpha** filter on the development 2.7pre-alpha version ( already on Git master ) , so it can now be easily used for removing background from scanned sketches.

**To find the feature, in the menu : Filter > Color > Color to alpha.**

Algorithm differs from the one used in Gimp ( also named 'Color to Alpha' ) : Krita use CIE deltaE \[0\] function to calculate the difference between the image and the base color, so it is more flexible and configurable. You can choose to what extent you want to remove the background by changing threshold value.

Dmitry explain the filter's algorithm on [his blog](http://dimula73.blogspot.ru/) :

1. Firstly, Krita calculate the difference between the image pixel and the base color and decrease the pixel's opacity according this difference. The less the difference, the more opacity is decreased. As already mentioned ; Krita use deltaE function to calculate this difference.
2. Secondly, Krita apply an inverse "composite over" to every pixel. Due to that step, if we put a layer filled with a base color below the filtered image, we will get original image!

What is the advantage compare to put your pencil artwork on a 'mulitply' layer blending mode ?  
You can easily 'lock' the alpha of the layer, then color only your lines now. It's a step I usually did in Gimp ( see on my [pencil to digital painting](http://www.davidrevoy.com/article129/pencil-to-digital-painting) tutorial ) and I'm happy to see the feature now in Krita too.

Reference :  
[Wikipedia Color Difference](http://en.wikipedia.org/wiki/Color_difference)  
[Dmitry original blog post](http://dimula73.blogspot.ru/2013/03/updated-krita-colortoalpha-filter.html)

image & text copied from Dmitry blog  
pencil artwork CC-By Deevad
