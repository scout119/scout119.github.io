---
layout: post
title: RGB-123 16x16 and Arduino Mega playing Tetris
date: '2013-09-07T13:44:00.000-04:00'
author: Valentin Ivanov
tags:
- Kickstarter
- LED
- Arduino
- Electronics
modified_time: '2013-09-07T13:54:15.991-04:00'
thumbnail: http://2.bp.blogspot.com/-7Wq_tCv0xBw/UitoOS7jV5I/AAAAAAAAAgg/GpkHz_Yz5Tw/s72-c/matrix.jpg
blogger_id: tag:blogger.com,1999:blog-5161433332962744423.post-1159449799765783067
blogger_orig_url: http://www.breakcontinue.com/2013/09/rgb-123-16x16-and-arduino-mega-playing.html
---
![img1](http://2.bp.blogspot.com/-7Wq_tCv0xBw/UitoOS7jV5I/AAAAAAAAAgg/GpkHz_Yz5Tw/s1600/matrix.jpg)

Couple of weeks ago I programmed a clone of the Tetris game for the [FEZ GameO](https://www.ghielectronics.com/catalog/product/448) console. Here it is running in my [GameO Emulator](https://www.ghielectronics.com/community/codeshare/entry/776):

![img2](http://4.bp.blogspot.com/-urU3azbJwec/UitYScw88mI/AAAAAAAAAfo/9SM-CCF37bM/s1600/1.jpg)

![img3](http://1.bp.blogspot.com/-JovH6VyssKs/UitYSTtpOSI/AAAAAAAAAfk/Wtt6xuC6LM0/s1600/4.jpg)

The game is a NETMF application written in C#. You can find it [here](https://www.ghielectronics.com/community/codeshare/entry/777).

A fellow maker and inventor Ryan O'Hara is running a Kickstarter campaign for his awesome [RGB-123 Led Matrices](http://www.kickstarter.com/projects/311408456/rgb-123-led-matrices) He was very kind to offer the 16x16 version of the board to help me see if I can get the game up and running on it. The RGB-123 is based on WS2812 RGB LEDs. [Adafruit Industries](http://www.adafruit.com/) has a great Arduino library - [NeoPixel for Arduino](https://github.com/adafruit/Adafruit_NeoPixel) - that can be used to drive WS2812 LED strips. RGB-123 16x16 is a LED strip that is arranged in square using a zig-zag like pattern, so the library is perfect for that. I have decided to use Arduino Mega as the controller to run the game, since Uno might be not enough due to smaller RAM. Couple of nights later I came up with this:

{% include youtubePlayer.html id="BBl3EjRrQ4Y" %}

I am using Wii Classic to control the game. If you use something else, you will need to change just one function (readButtons) and you should be good. More shots:

![img4](http://4.bp.blogspot.com/-CrD97fhpE7M/UitkfL3XigI/AAAAAAAAAgY/u36g4gzRxsk/s1600/5.jpg)

![img5](http://3.bp.blogspot.com/-GODDNAykeBI/UitkNfa3ZEI/AAAAAAAAAgI/xTnmcMQR20U/s1600/3.jpg)

![img6](http://3.bp.blogspot.com/-kSpV65Df_cA/UitkNT0389I/AAAAAAAAAgQ/ODBeC3ZrYLo/s1600/2.jpg)

![img7](http://1.bp.blogspot.com/-GODDNAykeBI/UitkNfa3ZEI/AAAAAAAAAf8/a815naAF78k/s1600/3.jpg)

[Download the source code](https://github.com/scout119/RGB123).

The RGB-123 is a fun board to play with. You can also chain them and have really big matrices (as long as you have enough power.) So, if you really like it and would like to have one, go to the Kickstarter and [support Ryan's campaign](http://www.kickstarter.com/projects/311408456/rgb-123-led-matrices).

What is next? I am going to do another game - Snake for RGB123, so stay tuned!