---
title: "Krita 4.0.0 Released!"
date: "2018-03-22"
categories: 
  - "news"
  - "officialrelease"
---

Today we're releasing Krita 4.0! A major release with major new features and improvements: improved vector tools, SVG support, a new text tool, Python scripting and much, much, much more!

{{< youtube a-CY4hmkg_I >}}

The new splash screen for Krita 4.0, created by Tyson Tan, shows Kiki among the plum blossoms. We had wanted to release Krita 4 last year already, but [trials and tribulations](/item/krita-foundation-update/) caused considerable delays. But, like the plum blossoms that often bloom most vibrantly when it's coldest, we have overcome, and Krita 4 is now ready!

[![](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)

### Highlights

We've again created a long, long page with all the details of everything that's new and improved in Krita 4.

[See the full release notes with all changes!](/krita-4-0-release-notes/)

We already mentioned SVG support, a new text tool and Python scripting, so here are some other highlights:

- Easy coloring of line-art with the new Colorize Mask Tool. [Read the manual for more detail](https://docs.krita.org/en/reference_manual/tools/colorize_mask.html)!

[![](/images/posts/2018/colorize-mask.png)](/images/posts/2018/colorize-mask.png)

- Masked brushes: add a mask to your brush tip for a more lively effect. This opens up some really cool possibilities!

[![](/images/posts/2018/waterpaint.gif)](/images/posts/2018/waterpaint.gif)

- New brush presets! We overhauled the entire brush set for Krita 4. Brush presets are now packaged as a bundle, too. And Krita 3's brush set is available as well, it's just disabled by default.

[![](/images/posts/2018/bundles.png)](/images/posts/2018/bundles.png)

### Known issues

Krita 4 is a huge step for the Krita project, as big as, if not bigger than the 3.0 release. There are some known issues and caveats:

- Krita 4 uses SVG for vector layers. This means that Krita 3 files with vector layers may not be loaded entirely correctly. Keep backups!
- Krita 4's new text tool is still limited compared to what we wanted to implement. We focused on creating a reliable base and making the text tool work reliably for just one, simple use-case: creating text for comic book balloons, and we'll continue working on improving and extending the text tool.
- We have a new binary build factory for Windows and Linux. Unfortunately, we don't have 32 bits Windows builds at this point in time.
- Because macOS has a very low limit on shared memory segments, G'Mic cannot work on macOS at the moment.
- The Reference Images Docker has been removed. It was too easy to crash it if invalid image files where present. In Krita 4.1 it will be replaced by a new reference images tool.

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.0.0-setup.exe](https://download.kde.org/stable/krita/4.0.0/krita-x64-4.0.0-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.0.zip](https://download.kde.org/stable/krita/4.0.0/krita-x64-4.0.0.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.0/krita-x64-4.0.0-dbg.zip)

At this moment, we do not have 32 bits Windows builds available.

Note that on Windows 7 and 8 you need to install the Universal C Runtime separately to enable Python scripting. See the [manual](https://docs.krita.org/en/user_manual/python_scripting/introduction_to_python_scripting.html).

#### Linux

- - 64 bits Linux: [krita-4.0.0-x86_64.appimage](https://download.kde.org/stable/krita/4.0.0/krita-4.0.0-x86_64.appimage)

At the moment, the appimage does not have working translations.

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

You can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.0.0 on Ubuntu and derivatives. We are working on an updated snap.

#### OSX

- macOS disk image: [krita-4.0.0.dmg](https://download.kde.org/stable/krita/4.0.0/krita-4.0.0.dmg)

Note: the gmic-qt and python plugins are not available on macOS.

### Source code

- Source code: [krita-4.0.0.tar.gz](https://download.kde.org/stable/krita/4.0.0/krita-4.0.0.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/stable/krita/4.0.0/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.0.0/).

### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

[![](/images/posts/2018/Krita4_Alegoric_final-1024x507.png)](/images/posts/2018/Krita4_Alegoric_final.png) Artwork by Ramon Miranda
