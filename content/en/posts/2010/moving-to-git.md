---
title: "Moving to Git!"
date: "2010-12-06"
---

Or... Where did my Krita go?

For about five years, until 2005, Krita was developed in KDE's CVS repository. In 2005, it moved to subversion. And now, in 2010, Krita will move to KDE's git infrastructure. This is a much bigger change than from CVS to SVN, and people will have to learn some new habits. We might even change some of our ways of working.

And at the same time, the name of the parent project changes from KOffice to [Calligra](http://www.calligra-suite.org). This is in recognization of the fact that the "KOffice" technology Krita is based on has a wider purpose than just enabling office applications. See [the Calligra announcement for more information!](http://dot.kde.org/2010/12/06/kde-announces-calligra-suite).

In any case, if you were one of the brave people following Krita development, you'll have to adapt a bit. Where you previously checked out the Krita source code from subversion and kept up to date with "svn up", you'll have to do the following:

Download the latest repository tarball**\***:

$ wget -c http://anongit1.kde.org/calligra/calligra-latest.tar.gz

Unpack it:

$ tar -xzf calligra-latest.tar.gz

Initialize the repository:

$ cd calligra; ./initrepo.sh

And from now on, with a simple**\***

git pull

You can keep up to date! All the building steps are still exactly the same.

**\* NOTE:** Problems have been seen when doing git pull, if the second step (unpacking the .tar.gz) is done on an NTFS partition. This may also apply to Fat 16 and Fat 32 partitions. Typically these are not partitions created by Linux, but by Windows or on removable drives.

If the experience of other KDE projects that have moved to git is anything to go by, this move will make Krita development go even faster!
