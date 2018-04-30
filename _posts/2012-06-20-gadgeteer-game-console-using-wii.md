---
layout: post
title: Gadgeteer game console using Wii classic controller
date: '2012-06-20T22:49:00.000-04:00'
author: Valentin Ivanov
tags:
- NETMF
- GHI Electronics
- Electronics
- Gadgeteer
modified_time: '2013-05-14T11:34:52.776-04:00'
thumbnail: http://3.bp.blogspot.com/-jJ1GUjUS4FU/T-KDBZ7nRII/AAAAAAAAAYM/YKs90a13wHI/s72-c/IMG_4287.JPG
blogger_id: tag:blogger.com,1999:blog-5161433332962744423.post-1983980462702264392
blogger_orig_url: http://www.breakcontinue.com/2012/06/gadgeteer-game-console-using-wii.html
permalink: /2012/06/gadgeteer-game-console-using-wii.html
---

A while ago I made a [module (Chucky)](http://www.breakcontinue.com/2011/10/chucky-module-for-microsoft-gadgeteer.html) that allows to connect a Wii classic controller to a Gadgeteer mainboard. Finally got some time to build a mounting rig that attaches to a Wii controller and allows you to put all necessary modules. The goal was to make it easy to assemble/disassemble and no extra modifications for the Wii controller. Here is what I have ended up with:

![im1](http://3.bp.blogspot.com/-jJ1GUjUS4FU/T-KDBZ7nRII/AAAAAAAAAYM/YKs90a13wHI/s1600/IMG_4287.JPG)

I've used 1/8 and 1/4 thick plywood and a 1/8 in diameter bronze rod. Two small pieces of rod glued to the only 1/4 thick "base" piece that goes into the screw holes at the back of the Wii controller. The rest of the 1/8 thick pieces are interlocked with each other and the base. (I have put a small piece of electric tape on one of the "pegs" that holds the base much better)

![im2](http://3.bp.blogspot.com/-03O5RIBLhpk/T-KDB29NTyI/AAAAAAAAAYU/CRXGJWOJ6Y4/s1600/IMG_4291.JPG)

Here are more pictures of the whole thing put together.

![im3](http://3.bp.blogspot.com/-q8TnTCCrjOA/T-KFAHFSU3I/AAAAAAAAAYc/-TJQ58K81Gw/s1600/IMG_4275.JPG)

![im4](http://3.bp.blogspot.com/-IxCNyEBoz90/T-KFFKd8VwI/AAAAAAAAAYk/Ar2M4ypBt2s/s1600/IMG_4273.JPG)

I have used plastic standoffs and various screws to attach all the modules:

![im5](http://3.bp.blogspot.com/-kbUGaJKwKQM/T-KFSokAleI/AAAAAAAAAYs/gWzj6w1idFU/s1600/IMG_4277.JPG)

That is the FEZ Spider attached at the back of the main mounting plate.

![im6](http://3.bp.blogspot.com/-LvcCUHtHKFw/T-KFZAelwOI/AAAAAAAAAY0/TvO6tenpSTw/s1600/IMG_4278.JPG)

A fellow Fezzer **taylorza** ported the [Mini Pacman game for Fez Spider](http://www.tinyclr.com/forum/topic?id=6907). He has used joystick and button modules. To make my module work, I had to add a custom input provider that wraps the Chucky driver. It was very easy to do. The full source code of the game can be downloaded from [Codeplex](http://chrismcstuff.codeplex.com/). Chucky Gadgeteer driver code and example is on [Codeshare](http://www.tinyclr.com/codeshare/entry/439), same goes for the [Chuky custom input provider code](http://www.tinyclr.com/codeshare/entry/440).

Here it is running on my "console":

![im7](http://1.bp.blogspot.com/-dyFYbr7y0Qs/T-KHzsjV7NI/AAAAAAAAAZA/FV9MN6NDoiI/s1600/IMG_4281.JPG)

I have started porting Space Invaders for Gadgeteer, so keep in touch for the update.