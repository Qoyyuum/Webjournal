---
layout: post
title:  "Where have I been?"
date:   2018-05-28 09:32:00 +1000
categories: blog
---

Back in Github again as I go through fiddling around with my machine. I've finally managed to set up Fedora 27 recently as part of a dual boot on my Windows 10 laptop. It wasn't easy, I tell ya, despite all the support I got, the solution was alot easier than I thought.

# Fedora Display Drivers
The problem with my installation was that it only work with certain display drivers for some odd reason. Setting this up kind of gives me a little lesson on how machines interface with the display. And this happened even before installing Fedora. The first clue was that I managed to install Fedora only through the "Troubleshooting" option on boot to my USB stick.

After the installation, the image was... functional but at a lowest possible resolution (i.e. 800x600). My `xrandr -q` did nothing as it only displayed
```
xrandr: Failed to get size of gamma for output default
Screen 0: minimum 800 x 600, current 800 x 600, maximum 800 x 600
default connected primary 800x600+0+0 0mm x 0mm
   800x600       75.00*
```

Immediately, its just a problem with my display driver. But can I live with the low resolution? I did try. Unfortunately, its not workable for me (especially if I'm working in the web). So fixing the display diver became a priority.

After trying out multiple solutions out there, I tried the most simple solution of all and this requires no third-party repositories or installation of a nvidia driver from anywhere else but the official repo.

```
$ dnf search *\nvidia\*
google-chrome                                                                                                                                                                       18 kB/s | 3.7 kB     00:00    
Last metadata expiration check: 0:00:00 ago on Mon 28 May 2018 09:40:31 AM AEST.
======================================================================================== Name & Summary Matched: *nvidia* =========================================================================================
nvidia-query-resource-opengl-lib.x86_64 : Library for nvidia-query-resource-opengl
pcp-pmda-nvidia-gpu.x86_64 : Performance Co-Pilot (PCP) metrics for the Nvidia GPU
nvidia-texture-tools-devel.i686 : Development libraries/headers for nvidia-texture-tools
nvidia-texture-tools-devel.x86_64 : Development libraries/headers for nvidia-texture-tools
nvidia-query-resource-opengl.x86_64 : Querying OpenGL resource usage of applications using the NVIDIA OpenGL driver
============================================================================================= Name Matched: *nvidia* ==============================================================================================
nvidia-texture-tools.i686 : Collection of image processing and texture manipulation tools
nvidia-texture-tools.x86_64 : Collection of image processing and texture manipulation tools
============================================================================================ Summary Matched: *nvidia* ============================================================================================
nv-codec-headers.noarch : FFmpeg version of Nvidia Codec SDK headers
envytools.x86_64 : Tools for people envious of nvidia's blob driver
xorg-x11-drv-nouveau.x86_64 : Xorg X11 nouveau video driver for NVIDIA graphics chipsets
```
After that I just did `sudo dnf install xorg-x11-drv-nouveau` and it all worked after a reboot.

# Now to enjoy all the goodness of Linux
This includes `Docker`, the wonders of `VIM`, and to a lot of my host hopping tunnel for server traffic to my localhost machine, `sshuttle` has now become much more convenient as opposed to my Win10 image.

Not exactly hating Win10 but recently, and before I dualbooted, I was fond of using WSL (Windows Subsystem for Linux) but unfortunately, Microsoft decided to break it in one of its Windows Updates. Sure, I could rollback but why bother.