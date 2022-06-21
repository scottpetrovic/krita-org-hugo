---
title: "Download Krita!"
date: "2011-05-11"
---

# Version 2.3  

Krita 2.3 is still part of KOffice. Some Linux distributions still package that version

# Version 2.4

Krita 2.4 has not been released yet. Beta packages are available for many Linux distributions as well as for Windows.

## Windows

Please go to [www.kogmbh.com/download.html](http://www.kogmbh.com/download.html) to download the HIGHLY EXPERIMENTAL Windows installer.

## Linux

### Ubuntu

Beta packages are available through the following PPA:

 https://launchpad.net/~kubuntu-ppa/+archive/beta/+packages  

You can also use the Project Neon packages:

Ubuntu users can get a nightly build of **Calligra** with the [Project Neon](https://wiki.kubuntu.org/Kubuntu/ProjectNeon), you need to add ppa:neon/ppa to your sources.list and install project-neon-calligra package.

This script installs project neon and krita:

sudo add-apt-repository ppa:neon/ppa   && sudo apt-get update  && sudo apt-get install project-neon-base     project-neon-calligra     project-neon-calligra-dbg 

In order to run the installed packages you have to logout and choose "Project Neon" from the login screen. Neon always has the latest version, not necessarily the beta releases.

### Debian

The [qt-kde debian project](http://qt-kde.debian.net/) has packages available as well now,Follow these instructions:

Add the following to your /etc/apt/sources.list:

deb http://qt-kde.debian.net/debian experimental-snapshots main deb-src http://qt-kde.debian.net/debian experimental-snapshots main

In order to get repository key, install the pkg-kde-archive-keyring  
package:

aptitude install pkg-kde-archive-keyring

then you can install krita with :

apt-get install krita

### OpenSUSE

Packages are available from the [unstable playground repository](https://build.opensuse.org/project/show?project=KDE%3AUnstable%3APlayground).

### Fedora

There are no Fedora packages available at this moment.  

### Gentoo

The ebuild for [Calligra 2.4 beta 3](http://www.calligra-suite.org/news/announcements/calligra-2-4-beta-3/), i.e. is in the portage tree as: [app-office/calligra-2.3.83](http://packages.gentoo.org/package/app-office/calligra). You can use this to install Krita as well; there might be newer versions as Calligra releases more beta's.  

### Arch

Arch Linux provides Calligra packages in the kde-unstable repository

## FreeBSD

Packages are available in [area51](http://freebsd.kde.org/area51.php).
