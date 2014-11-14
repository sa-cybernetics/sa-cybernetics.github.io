---
layout: post
title: "Automatically Download Subtitle when Finished Downloading Movie"
description: ""
category: 
tags: [Movies, Linux, Bash]
---
{% include JB/setup %}

When downloading movies from the internet using a torrent client, I found it useful to make a script to automatically download 
subtitles to the movie (I always forgot the right filebot command and was too lazy downloading from a browser).

<!-- more -->

 The default Ubuntu BitTorrent
Client *Transmission* (and most other torrent clients I assume) lets you run scripts at different stages of the 
download, including *download finnished*.
So I simply let transmission call the script below when a movie is finnished downloading. If you're using a different client, then you might have
to change the script arguments $TR_TORRENT_NAME and $TR_TORRENT_DIR with command line arguments giving the directory and name of the torrent, 
used for that client.
In order to make it work, you need to have [filebot](http://www.filebot.net/ "filebot") installed. 

<script src="https://gist.github.com/simena86/483656f8eaee51a44f54.js"></script>

