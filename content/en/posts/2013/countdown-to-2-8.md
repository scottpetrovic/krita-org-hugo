---
title: "Countdown to 2.8"
date: "2013-12-15"
---

The Krita Team is working really hard on what promises to become a really exciting release of Krita: 2.8. We're not adding any new features anymore, just fixing bugs and then fixing more bugs! Here's a short list of what we've done over the past week. These fixes are available for Windows users in updated 2.8 beta 1 builds:

[http://heap.kogmbh.net/downloads/krita_x86_2.7.9.1.msi](http://heap.kogmbh.net/downloads/krita_x86_2.7.9.1.msi)  
[http://heap.kogmbh.net/downloads/krita_x64_2.7.9.1.msi](http://heap.kogmbh.net/downloads/krita_x64_2.7.9.1.msi)  
[http://heap.kogmbh.net/downloads/kritagemini_x86_2.7.9.1.msi](http://heap.kogmbh.net/downloads/kritagemini_x86_2.7.9.1.msi)  
[http://heap.kogmbh.net/downloads/kritagemini_x64_2.7.9.1.msi](http://heap.kogmbh.net/downloads/kritagemini_x64_2.7.9.1.msi)

And for \*buntu users, in the Krita Lime repository.

Here's this week's crop of fixes:

- BUG: 328579: Add close button to quick access palette dialog
- BUG:328389: Fix delivering tablet events to wigdets other than the canvas
- BUG:328615: Fix an assert in KisToolPolylineBase (by Antony Saraev -- welcome!)
- Fix a lockup when pressing Shift while doing a stroke
- BUG:328621: Initialize the active composite op to default
- Fix a crash when using Select->Opaque and Color Range over fully transparent layer
- Show messagebox instead of backtrace when the shaders cannot be compiled
- BUG:328564: Fix autobrush size calculation
- BUG:324987: Make it possible to paint something with brushes smaller than 1.0
- BUG:328332: Add a menu entry to open a file manager on the resources folder
- BUG: 328456: Save and load color-dodge correctly. With fallback for old and broken ora files.
- BUG:328618: Accept the event in KoPathTool when we really need it
- BUG: 325481: Warn the user when enabling wraparound mode if opengl is off
- BUG:327977: don't show popups outside the screen
- BUG:312111: Only show suitable filters in the filter layer/mask dialog
- BUG: 328648: Do not show the High Quality filtering mode if it's not available
- BUG:326759: Use default rgb8 for setting the initial bg/fg color
- BUG:318024: Remember the detached status of the brush editor
- BUG:315553: Open the quick access ring under the cursor
- BUG:328630; Fix crash when cropping a Shape Layer
- BUG:328390: Fix undo for the Grid Brush
- BUG:328358: Fix too fast mouse clicks (triple clicks) issue (yoo many and too fast clicks on a canvas lead to a lock-up and switching to Default Tool)
- BUG:328649: Fix initialization order of OpenGL canvas (might fix opengl on AMD?)
- BUG:327162: Fix the border effect when working in Trilinear/HiQuality mode
- A more precise color-picker cursor (Thanks to David Revoy)
