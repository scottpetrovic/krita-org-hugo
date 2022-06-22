---
title: "Google Summer of Code 2015"
date: "2015-04-28"
---

The list of students accepted to the [2015 edition of Google's Summer of code](http://www.google-melange.com/gsoc/projects/list/google/gsoc2015) has just been published. This year, we've got two students working on Krita: Jouni and Wolthera. Wolthera has been a Krita developer for quite some time, working on color selectors perspective assistants and more, while Jouni has contributed with bug fixes for 2.9.

Wolthera is working on an experimental brush engine: a [tangent normal map brush engine](http://www.google-melange.com/gsoc/project/details/google/gsoc2015/wolthera/5668600916475904). A surface normal is a type of vector used to determine how light bounces off a surface. 3d graphics have has a way to encode these in normal-maps. To the human eye, this encoding looks like a colour. This brush engine takes the tilt sensors of a tablet stylus, and treats it like a surface normal, having it output the correct color. This would be a worthwhile asset to Krita because of the interest in hand-painted textures. There's already quite a bit of progress in [her branch](https://projects.kde.org/projects/calligra/repository/show?rev=krita-testing-wolthera)! Check out the [forum thread](https://forum.kde.org/viewtopic.php?f=288&t=126128&p=333828#p333828), too.

[![tangent](/images/posts/2015/tangent-1024x683.png)](https://krita.org/wp-content/uploads/2015/04/tangent.png)

Jouni will build on the lessons learned from last year's animation project and [integrate animation into Krita's core](http://www.google-melange.com/gsoc/project/details/google/gsoc2015/joupent/5649050225344512). All three of our previous animation plugins were hampered by being designed as a plugin. This time, animation is going right into the deepest layers of Krita. Krita's native file format will start supporting animations as well. Jouni had already started on animation support before Summer of Code was announced, in fact, and he has got a proof of concept up and running already.

[![animation](/images/posts/2015/animation-1024x640.png)](https://krita.org/wp-content/uploads/2015/04/animation.png)

In fact, two weeks ago, we had our first sprint in Deventer, sponsored by the Krita Foundation, with a hopeful Jouni and Wolthera and prospective mentors Dmitry and Boudewijn, to thresh out the designs for both features and do some pair programming.

[![2015-sprint](/images/posts/2015/2015-sprint-1024x768.jpg)](https://krita.org/wp-content/uploads/2015/04/2015-sprint.jpg)

Congrats to Jouni and Wolthera and let's look forward to an awesome Summer of Code!
