---
title: "Multi Toolkit Programming: Interoperatibility of different GUI toolkits for the X Window System"
date: "2018-03-02"
---

 

(Archived from [http://www.linux-kongress.org/1998/abstracts.html](http://www.linux-kongress.org/1998/abstracts.html))

## Multi Toolkit Programming: Interoperatibility of different GUI toolkits for the X Window System

### Freitag, 5.6. 12:15-13:00

Matthias Ettrich [ettrich@kde.org](mailto:ettrich@kde.org)Thanks to the KDE Desktop Environment Project there is finally some movement inside the freeware community regarding graphical user interfaces. The ergonomical standards for graphical applications grow and an increasing number of users is no longer satisfied with a chaotically patched desktop. I clearly realized that with another project of mine: The LyX document processor, a kind of wordprocessor based on the LaTeX typesetting system. Only six months after the foundation of the KDE Desktop Project I recieved more and more emails of long-term LyX users "complaining" that their wordprocessor did no longer fit into their new desktop, but was more and more difficult to use. I could not believe that at first, until I created a larger document with my own program after a break of several months. And really: After only one year of KDE-usage it was remarkably more difficult for me to get used to the different behaviour of apparently well-known controls again, especially scrollbars and pulldown menus. "The forces I set free...." came out against me, that must not be! Also things began to bother me which I considered entirely normal before: The configuration by editing a complex file named lyxrc with a texteditor, complex dialog popups instead of dynamic toolbars, missing session management, missing drag'n'drop and all those further KDE benefits. In addition, the toolkit used by LyX - named xforms - differed very much from Motif in respect of usage, and therefore also from the OS/2 workplace shell, Macintosh and MS-Windows. This was no real problem in the times of chaotic X-desktops - Athena is even more unusable - but these times are luckily over.

Everything cried for a port! And due to the urging of Kalle Dallheimer, who was in seek for a comfortable wordprocessor for his wife, we found ourselves sitting in front of two X-terminals. Equiped with a couple of cans of caffeinated chocolate (too much coffee is bad for the stomach), we set ourselves a limit of 24 hours for a port.

A first "grep" over the sources, which are not too small with 80.000 lines of C++, was not very encouraging: Over 50 complex dialogs and far more than 5000 calls of xforms-functions. It was obvious that the trivial method of porting --- replacing all xforms related code with KDE/Qt-code and recompile --- was neither possible within 24 hours nor very amusing. The pure thought about the need to debug several thousand lines of new GUI-code at once after a couple of days hard work, took the last bit of fun away. And fun should be the most important motivation to create free software.

The ideal solution to cope with such a huge task of porting is obvious: Simply set one foot after the other. That means replacing function call for function call, dialog for dialog without breaking the functionality of the whole. This model of porting is similar to a complete renovation of a house while you still live in it. In one word: The solution is multi toolkit programming.

In fact: only few lines of modified code made it possible to add new Qt-GUI-controls additionally to the current xforms stuff. LyX simply used both toolkits at the same time!

In my talk I will try to explain how and why something like this works:

- X Basics: Displays and drawables
- the classical X11 event loop
- variations and extensions in legacy toolkits
- slots, places for interoperability

One the one hand multi toolkit programming has several advantages for the porting of applications: (a) It is easier, (b) it can be done within a larger timeframe, (c) it can be distributed on many shoulders. All these are important points for free software development. On the other hand it becomes possible to borrow controls and functionaliy from other toolkits. And example might be a GTK-application which want to use the KApplication-class from the KDE Desktop Environment to get access to a comfortable data base, desktop configuration events, session management, iconloader and much more.

My investigation will cover the popular ( = many applications available) tookits like Qt, Tk, Motif, Athena and XForms. I might also have a look at a framework like wxWindows and --- with regard to a possible Gimp-to-KDE-port --- GTK.

The target audience of the talk are mainly programmers who already have some X11-experiences. But also all others may hopefully gain some useful knowledge about the X Window System and event driven programming in general.
