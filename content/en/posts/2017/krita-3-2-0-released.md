---
title: "Krita 3.2.0 Released"
date: "2017-08-17"
---

Later than planned, here's Krita 3.2.0! With the new G'Mic-qt plugin integration, the smart patch tool, finger painting on touch screens, new brush presets and a lot of bug fixes.

[Read the full release notes for more information!](/release-notes-for-krita-3-2/). Here's [GDQuest's](http://gdquest.com/) video introducing 3.2.0:

{{< youtube f9K48jXml4s >}}

Note: the gmic-qt plugin is not available on OSX. Krita now ships with a pre-built [gmic-qt plugin](https://github.com/c-koi/gmic-qt) on Windows and the Linux AppImage. If you have tested the beta or release candidate builds, you might need to [reset your configuration](https://docs.krita.org/KritaFAQ#Resetting_Krita_configuration).

### Changes since the last release candidate:

- Don't reset the LUT docker when moving the Krita window between moitors
- Correctly initialize the exposure display filter in the LUT docker
- Add the missing pan tool a ction
- Improve the "Normal" blending mode performance by 30% (first patch for Krita by Daria Scherbatyuk!)
- Fix a crash when creating a second view on an image
- Fix a possible crash when creating a second window
- Improve finding the gmic-qt plugin: Krita now first looks whether there is one available in the same place as the Krita executable
- Fix scroll wheel behaviour if Krita is built with Qt 5.7.1. or later
- Fix panning in gmic-qt when applying gmic-qt to a non-RGBA image
- Scale channel values correctly when using a non-RGBA image with gmic-qt
- Fix the default setting for allowing multiple krita instances
    
    ### Download
    
    #### Windows
    
    Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.
    
    - 32 bits Windows: [krita-3.2.0-x86-setup.exe](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86-setup.exe)
    - Portable 32 bits Windows: [krita-3.2.0-x86.zip](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86.zip)
    - [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86-dbg.zip)
    
    - 64 bits Windows: [krita-3.2.0-x64-setup.exe](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64-setup.exe)
    - Portable 64 bits Windows: [krita-3.2.0-x64.zip](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64.zip)
    - [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64-dbg.zip)
    
    - Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)
    
    #### Linux
    
    - 64 bits Linux: [krita-3.2.0-x86_64.appimage](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86_64.appimage)
    
    (If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)
    
    When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.2.0 on Ubuntu and derivatives.
    
    #### OSX
    
    - OSX disk image: [krita-3.2.0.dmg](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0.dmg)
    
    Note: the gmic-qt and pdf plugins is not available on OSX.
    
    ### Source code
    
    - Source code: [krita-3.2.0.tar.gz](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0.tar.gz)
    
    #### md5sums
    
    For all downloads:
    
    - [md5sums.txt](https://download.kde.org/stable/krita/3.2.0/md5sums.txt)
    
    #### Key
    
    The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.2.0/).
    
    #### Support Krita
    
    Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.
