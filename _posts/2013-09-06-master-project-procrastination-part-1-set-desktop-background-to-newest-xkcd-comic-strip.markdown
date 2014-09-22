---
layout: post
title: "Automatically Set Desktop Background to newest XKCD Comic Strip Using Python"
date: 2013-09-06 13:48
comments: true
categories: Linux
---

This semester I'm writing my master's project, which seems to be a time when procrastination thrives. When setting up Ubuntu on my school PC i had to decide what to use for desktop image. I therefore wrote a script to update the desktop background to the most recent [XKCD](http://www.xkcd.com) comic strip:

<!-- more -->

<script src="https://gist.github.com/simena86/f4b464575419e38f61f3.js"></script>

The script fetches the image of the comic and the mouseover text. The mouseover text is rendered as an image and finally stitched together with the comic image.
If your're using a Unix based OS you can schedule the script to run e.g. every  Monday, Wednesday and Friday using [crontab](http://www.adminschoice.com/crontab-quick-reference/). 

The source can be found in my [github](https://github.com/simena86/xkcdDesktop)


![Alt text](/images/xkcd.png)

