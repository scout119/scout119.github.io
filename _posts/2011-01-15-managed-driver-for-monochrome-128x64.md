---
layout: post
title: Managed driver for Monochrome 128x64 OLED graphic display
date: '2011-01-15T19:42:00.000-05:00'
author: Valentin Ivanov
tags: 
modified_time: '2012-01-20T17:41:37.813-05:00'
thumbnail: http://4.bp.blogspot.com/-gbWBuh43KLA/ToUCLi41A6I/AAAAAAAAAJk/9iJUy2hlN3o/s72-c/SSD1306.jpg
blogger_id: tag:blogger.com,1999:blog-5161433332962744423.post-7598050169105157644
blogger_orig_url: http://www.breakcontinue.com/2011/01/managed-driver-for-monochrome-128x64.html
permalink: /2011/01/managed-driver-for-monochrome-128x64.html
---

I got my hands on the new Monochrome OLED graphic display from [Adafruit](http://www.adafruit.com/index.php?main_page=product_info&amp;cPath=37&amp;products_id=326). I absolutely love it. This is a great addition to my gadgets.

My main dev board is [FEZ Panda](http://www.tinyclr.com/hardware/16/fez-panda/) from GHI Electronics. It is a .Net Micro Framework device with a great set of features. I looked for a managed driver for the display and couldn't find any, so I have ported the [arduino library](https://github.com/adafruit/Adafruit_SSD1306) that is provided by Adafruit.

It didn't work from the first try. I have arduino board as well, so I have tried the orginal library with no success. I almoust got to the point of returning the display, but decided to take a closer look and found that there were two bridges on some pins at the back of the display board.

I have "fixed" the bridges with a hobby knife and my driver worked right away!

![image](http://4.bp.blogspot.com/-gbWBuh43KLA/ToUCLi41A6I/AAAAAAAAAJk/9iJUy2hlN3o/s1600/SSD1306.jpg)

You can find the full source code [here](http://code.tinyclr.com/project/229/monochrome-128x64-oled-graphic-display-driver/).