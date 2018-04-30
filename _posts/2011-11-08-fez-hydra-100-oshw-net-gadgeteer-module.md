---
layout: post
title: FEZ Hydra 100% OSHW .NET Gadgeteer main board
date: '2011-11-08T22:21:00.003-05:00'
author: Valentin Ivanov
tags:
- FEZ Hydra
- GHI Electronics
- Electronics
- Gadgeteer
modified_time: '2012-01-26T09:22:19.810-05:00'
thumbnail: http://4.bp.blogspot.com/-7TXVaMi_Gp4/TrnpGn4F70I/AAAAAAAAAPc/ccLF13JrJq4/s72-c/fez_hydra_socket_map.png
blogger_id: tag:blogger.com,1999:blog-5161433332962744423.post-9114617920648643415
blogger_orig_url: http://www.breakcontinue.com/2011/11/fez-hydra-100-oshw-net-gadgeteer-module.html
permalink: /2011/11/fez-hydra-100-oshw-net-gadgeteer-module.html
---

I wrote about FEZ Hydra in my last post and now we have all the [details](http://www.ghielectronics.com/catalog/product/328). It is 100% open source including hardware design as well as the port of .NET Microframework that can be compiled using GCC toolchain. According to Gus Issa, this board was designed with three main goals:

1. Open source
2. Low cost
3. More Power

Lets take a closer look and compare it to FEZ Spider.

![hydra](http://4.bp.blogspot.com/-7TXVaMi_Gp4/TrnpGn4F70I/AAAAAAAAAPc/ccLF13JrJq4/s1600/fez_hydra_socket_map.png)

![spider](http://1.bp.blogspot.com/-r8rfwd3FpLk/TrnpFKFQekI/AAAAAAAAAPU/iQomN9-g2MU/s1600/fez_spider_socket_map.png)

The first noticeable difference is in size **3.42" x 2.44"** vs **2.25" x 2.05"**. There is also a very nice OSHW logo in the center of the board and absence of configuration switches. The FEZ Hydra has 14 .NET Gadgeteer compatible sockets same as the FEZ spider, although there is a difference in the type sockets and number of the sockets. FEZ Hydra is missing H (USB Host), C (CAN Bus), E (Ethernet) sockets. (_Even though there is no E socket, the board can still be connected to internet using [SPI based Ethernet module](http://www.ghielectronics.com/catalog/product/333)_). I suspect that not having H, C and E is part of the low cost and open source measures. The board is definitely cheaper ($79.95) compared to FEZ Spider ($119.95) and no doubt has more power - 240Mhz ARM9 Processor (running at 200Mhz) compared to 72MHz ARM7 on Spider. These are the top main differences between the two boards. Overall FEZ Hydra is a very great offer.

I am one of the few lucky ones who will get the board, hopefully this week, and I will be back with more information on FEZ Hydra