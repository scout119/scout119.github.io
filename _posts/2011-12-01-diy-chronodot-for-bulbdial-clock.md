---
layout: post
title: DIY Chronodot for Bulbdial Clock
date: '2011-12-01T01:43:00.000-05:00'
author: Valentin Ivanov
tags:
- Bulbdial
- LED
- Chronodot
- Arduino
thumbnail: http://1.bp.blogspot.com/-uY1CiJZiIHk/Txc9PT_2stI/AAAAAAAAATI/p6jbeUnjIGw/s72-c/3367455284_733ccbdb3a_b.jpg
---
A friend from work gave me a really nice present this Christmas - [Bulbdial Clock Kit](https://www.evilmadscientist.com/article.php/bulbdialkit) made by [Evil Mad Scientist Laboratories](https://www.evilmadscientist.com/). This clock is excellent addition to my collection of Ice Tube Clock and Monochron Clock. I have really enjoyed building it. It looks so cool with all its RGB LEDs. There is an optional component that you can add - a real time clock (RTC) with battery back up. It is called Chronodot RTC. All it does is ensure that clock is still ticking when main power source is removed, that way you don't have to reset the clock every time power cord is unplugged. A nice feature to have on any externally powered clock. You can buy one, but where is fun in that?! So I have decided to build my own. By the way this is what Chronodot looks like:

![img1](https://1.bp.blogspot.com/-uY1CiJZiIHk/Txc9PT_2stI/AAAAAAAAATI/p6jbeUnjIGw/s1600/3367455284_733ccbdb3a_b.jpg)

I like the round shape of the Chronodot board. Luckily RadioShack sells [Round PCB Kit](https://www.radioshack.com/product/index.jsp?productId=3173937). It is a set of 5 round boards of different sizes. The middle one is the perfect fit for our goal.

![img2](https://4.bp.blogspot.com/-QqDgUnejiaM/Tv1d2nubw_I/AAAAAAAAAS4/daLyaWzjacU/s1600/radioshack.jpg)

Hmm... What else do we need?

| Part   | Description |
| ------ | ----------- |
| ![p1](https://4.bp.blogspot.com/-gGgWxubNDzk/Tx9BTJtSiMI/AAAAAAAAATk/BP0Wfab9ZHQ/s1600/ds1307_t.jpg) | Real time clock - DS1307 |
| ![p2](https://3.bp.blogspot.com/-kOhAOFp_67k/Tx9Bmmdo48I/AAAAAAAAATs/yh2dL4lC83o/s1600/crystalcyl_t.jpg) | 32.768 KHz, 12.5 pF watch crystal |
| ![p3](https://3.bp.blogspot.com/-v6QvC11B5Xs/Tx9DHdlvLaI/AAAAAAAAAT0/MHnL8Q2XY9g/s1600/cr1220thm_t.jpg) | 12mm coin cell holder |
| ![p4](https://4.bp.blogspot.com/-tU74e82SKko/Tx9D8n2i2iI/AAAAAAAAAUE/qJS6zJYAuEY/s1600/CR2032_t.jpg) | 12mm 3V lithium coin cell - CR1220 |
| ![p5](https://2.bp.blogspot.com/-H5AIni52XiY/Tx9Om1UZsyI/AAAAAAAAAUM/4iZsmjrhweM/s1600/headerm36_t.jpg) | Straight male header.Two sections 4 pins each |
| All parts photos by Adafruit Industries [Adafruit.com](https://www.adafruit.com/) |

We will also need some wire. I am using Kynar wire 30AWG. The pcb board is one sided board so we will solder all components on one side and will use wire jumpers to connect corresponding pins. Lets start by taking a look at the pin out of the DS1307.

![im3](https://1.bp.blogspot.com/-7kSFKF4HxFM/TyePQXir-PI/AAAAAAAAAUc/SuXRfkgql5E/s1600/DS1307.jpg)

We will use RTC for time keeping only (it also can be used for square wave generation), so we will not be using SQW/OUT pin.

Here is the schematic of required connections:

![im4](https://3.bp.blogspot.com/-qczPGAgpd_A/TyjNAK7r51I/AAAAAAAAAUk/PW2umZ-yXYo/s1600/cd_schematic.jpg)

and board view:

![im5](https://4.bp.blogspot.com/-mfHpn8C_9UU/TyjNYZihI4I/AAAAAAAAAUs/PSAgFert8tg/s1600/cd_board.jpg)

I will not get into details on soldering - there are a lot of tutorials about soldering on the Web. This is what it looks like with everything soldered on the board.

![im6](https://2.bp.blogspot.com/-so6fECzq5qA/TyjPBnv3NvI/AAAAAAAAAU0/yPQKAUjmVso/s1600/IMG_20111227_192037.jpg)

And finally painted and installed on the clock:

![im7](https://1.bp.blogspot.com/-NuWPw3t1hww/TyjPqjI2wpI/AAAAAAAAAU8/oqYtN3aNpHs/s1600/IMG_20111230_020711.jpg)

This is it! Thank you for stopping by.