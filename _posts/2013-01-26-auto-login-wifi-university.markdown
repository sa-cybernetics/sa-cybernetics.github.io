---
layout: post
title: "Auto login WiFi – University, Hotels etc"
date: 2013-01-26 01:23
comments: true
categories: 
---

When using the University WiFi I found it annoying that I always had to login through a browser using my university username and password. Using the simple scripts below, this bothersome procedure can be done automatically each time the computer discovers a network.
<!-- more -->
I am using Wicd Network Manager, which has a nice feature where one can include scripts that you want to run when the computer connects and disconnects to a network ( see wicd documentation). Using this feature I made a short script to run different tasks when the computer discovered different Wifi's. I have a file called perform_on_post_connect.sh in the directory /etc/wicd/scripts/postconnect on my linux machine with the following code:



<script src="https://gist.github.com/simena86/c7341285d34637b9212b.js"></script>

I then wrote a python script called foo_autologin.py that performs the nessecary login procedure. If I am not mistaken, with Wicd one has to have this in a directory with only root access. The source for foo_autologin.py:

<script src="https://gist.github.com/simena86/3007e02416461d849330.js"></script>

When using the code above one has to use the headers and data used in the post method. The way I got the data from a login to the university was through using a Firefox Extension called Live HTTP Headers, as I found that chrome would not show HTTP traffic for HTTPS sites.

After monitoring a login using Live HTTP headers one can fill in the headers and data. Im sure there is a way of automating this task So feel free to share.
