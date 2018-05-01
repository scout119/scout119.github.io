---
layout: post
title: Rick Dangerous Port for NETMF
date: '2013-01-19T22:13:00.004-05:00'
author: Valentin Ivanov
tags:
- NETMF
- C#
- Electronics
- Gadgeteer
modified_time: '2013-01-23T22:13:33.627-05:00'
thumbnail: http://3.bp.blogspot.com/-eOpl6GVJBok/UQCfRkbNUHI/AAAAAAAAAaE/c42NTRjK8CQ/s72-c/splash.bmp
blogger_id: tag:blogger.com,1999:blog-5161433332962744423.post-2994142319986383496
blogger_orig_url: http://www.breakcontinue.com/2013/01/rick-dangerous-port-for-netmf.html
permalink: /2013/01/rick-dangerous-port-for-netmf.html
---
I wanted to have a good game for my [Gadgeteer Game Console](http://www.breakcontinue.com/2012/06/gadgeteer-game-console-using-wii.html). [Rick Dangerous](http://en.wikipedia.org/wiki/Rick_Dangerous) is an old classic game that I played long time ago and really liked.

![img1](http://3.bp.blogspot.com/-eOpl6GVJBok/UQCfRkbNUHI/AAAAAAAAAaE/c42NTRjK8CQ/s1600/splash.bmp)

Fortunately there is a clone of the game in C - **xrick** from [BigOrno.net](http://bigorno.net/xrick). Quote from BigOrno:

{: .box-note}
_Way before Lara Croft, back in the 1980's and early 1990's, Rick Dangerous was the Indiana Jones of computer games, running away from rolling rocks, avoiding traps, from South America to a futuristic missile base via Egypt and the Schwarzendumpf castle._  
_**xrick** is a clone of Rick Dangerous, known to run on Linux, Windows, BeOs, Amiga, QNX, all sorts of gaming consoles... download and install the game, learn how to play, and enjoy!_

It took some time, but here it is, running on Gadgeteer (FEZ Spider).
{% include youtubePlayer.html id=SU97StIcV80 %}

I have ported all C code from xrick to C#. The main difference between my code and xrick is how data is organized and stored. xrick uses a 8x8 pixels tiles as as smallest unit. There are 3 pages of 256 tiles each.

![img2](http://1.bp.blogspot.com/-wg7EwyANstk/UQChxMxmEWI/AAAAAAAAAaU/i4nlch5Emsg/s1600/rick1tiles.png)

Maps are build from blocks - block is a 4x4 tiles square (32x32 pixels). Blocks are rendered during map construction using tile data from a tile page for that map. So there is a lot of calculations happening before a map is constructed. The tile and page data is used to access environment flags for each 8x8 pixels area.

I have changed this from tiles to blocks. I have rearranged blocks, so they all grouped together for each map. I have replaced tile list for each block with the list of environment flags directly. This is how map related tiles are grouped into blocks:

![img3](http://1.bp.blogspot.com/-Oo3swz0E99I/UQCjb9KEzVI/AAAAAAAAAak/2Oy51hrcNso/s1600/blockmap.bmp)

Tiles for map introduction screens were put together as well:

![img4](http://3.bp.blogspot.com/-dgEjUwrkL8w/UQCmBfu7ffI/AAAAAAAAAbk/IlJUjOvjuLc/s1600/intro.bmp)

The only tiles that I have left are for text and status information:

![img5](http://1.bp.blogspot.com/-S4zT0g6Uzfg/UQCjyWMNg1I/AAAAAAAAAas/X2fl3k0W67c/s1600/font.bmp)

More information later...