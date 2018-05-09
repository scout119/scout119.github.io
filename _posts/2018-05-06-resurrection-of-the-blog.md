---
layout: post
title: Resurrection of the blog
date: '2018-05-06T15:23:57-04:00'
author: Valentin Ivanov
tags:
image: /img/github-pages.png
published: false
---
I have neglected my blog for quite a while. The Blogger platform that I have used before is good, but it is not exciting to go there and make new blog entries. I wanted a better, easier, natural way to edit and maintain the blog. By natural I mean something that fits my workflow. I am dealing with code every day. I use various developer tools and source control systems. So two major items in my developer workflow are:

1. Write code and supporting documents using different languages (markdown is one of them).
2. Check-in produced artifacts into the source (change) control system.

Github is one of the popular source control systems and it offers great companion service - [Github Pages](https://pages.github.com/). It is just another repository if you want a user site. Or a brunch in existing repository if it is a project site. It can be a full prebuilt static website or a markdown files that will be converted to html by static site generator [Jekyll](https://jekyllrb.com/). Using the service and Jekyll creating a new blog post is as easy as:

1. Write new post in markdown
2. Check-in the post into Github pages repository/branch.

That is all! Jekyll will generate the new html file, update all dependencies and it will publish it to the live site.

## On choosing a theme

There are [plenty of themes](https://github.com/jekyll/jekyll/wiki/Themes) available for Jekyll sites.

Make sure to test the theme you have selected with various screen sizes. I would rather have a theme that works on all sizes from the start. I have used Developer tools (F12) in Google Chrome to do that. You can "emulate" various devices (screen sizes) in the Developer tools view. Here is what the [Midnight Theme](https://madebygraham.com/midnight/) will look like on Pixel 2 XL:

![Dev Tools](/img/2018/05/devtools.png)

Make sure to do proper attribution to the themes' author(s). Always check and follow the license requirements.

## On testing locally

The only inconvinience with having your post done in Markdown is that you have to push it to Github to see what it will look like live. It also made your new post visible to everybody even if it is a work in progress. You have to have Jekyll run locally if you want to avoid publishing draft posts. If you are a Ruby developer I suspect it would be a trivial task. For non-Ruby folks the easiest way is to use Docker. Nice people from Jekyll project made an image available. Couple of issues I ran into while trying to run the container:

  1. My theme had **Gemfile** and **Gemfile.lock** that were causing an issue with one of the gems in the Jekyll docker image. I solved it by removing my local copies.  
  2. A lot of links were broken. The problem was that **baseurl** in the _config.yml had slash in it. I found this [post](http://downtothewire.io/2015/08/15/configuring-jekyll-for-user-and-project-github-pages/) (another Github pages site by the way) that describes the correct way of configuring various URLs. Following the rules in that post fixed the issue.

Here is my **docker.compose.yml** and extra _config.docker.yml for running Jekyll locally

**docker.compose.yml**:

```yml
jekyll:
  image: jekyll/jekyll:pages
  environment:
    - JEKYLL_ENV=docker
  command: jekyll serve --force_polling --incremental --config _config.yml, _config.docker.yml
  ports:
    - 4000:4000
  volumes:
    - .:/srv/jekyll
```

**_config.docker.yml**

```yml
url: "http://localhost:4000"
```

Keep in mind that even though the **--force_polling** setting was set, to get live updates the new posts you have to touch main index.html and any other pages that should have links for that newly created post.