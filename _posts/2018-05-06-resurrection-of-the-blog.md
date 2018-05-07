---
layout: post
title: Resurrection of the blog
date: '2018-05-06T15:23:57-04:00'
author: Valentin Ivanov
tags:
image: /img/github-pages.png
published: false
---
I have neglected my blog for quite a while. The Blogger platform that I have used before is good, but it is not exciting to go there and make new blog entries. I wanted a better, easier, natural way to edit and maintain the blog. By natural I mean something that fits my workflow. I am dealing with code every day and use various developer tools and programming languages. There is a source control system behind each project. Visual Studio Online, Github, Gitlab - you name it.

## On choosing a theme

There are [plenty of themes](https://github.com/jekyll/jekyll/wiki/Themes) available for Jekyll sites.

Make sure to test the theme you have selected with various screen sizes. I would rather have a theme that works on all sizes from the start. I have used Developer tools (F12) in Google Chrome to do that. You can "emulate" various devices (screen sizes) in the Developer tools view. Here is what the [Midnight Theme](https://madebygraham.com/midnight/) will look like on Pixel 2 XL:

![Dev Tools](/img/2018/05/devtools.png)

Make sure to do proper attribution to the themes' author(s). Always check and follow the license requirements.

## On testing locally

The only inconvinience with having your post done in Markdown is that you have to push it to Github to see what it will look like live. It also made your new post visible to everybody even if it is a work in progress. You have to have Jekyll run locally if you want to avoid publishing draft posts. If you a Ruby developer I suspect it would be a trivial task. For non-Ruby folks the easiest way is to use Docker. Nice people from Jekyll project made an image available.