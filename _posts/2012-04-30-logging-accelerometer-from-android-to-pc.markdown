---
layout: post
title: "Logging Accelerometer from Android to PC"
date: 2012-04-30 22:09
comments: true
categories: 
---



I am pretty new to Android and decided to play around with the sensors. I always find accelerometers fun to play with, and like to visualize the sensor reading through a real time plot. In the java-script for the android app below, the acceleration in the x axis is read and streamed through a TCP socket to the PC over wlan. A simple python server script reads the data from a socket and writes it to a perl script, logging the data in GnuPlot, and thus setting my personal record for mixing different languages.

<!-- more -->

{% img  http://sacybernetics.files.wordpress.com/2012/06/2012-06-03-23-07-43.png 300 380 %}

{% youtube OOufu8sdyKA %}


<script src="https://gist.github.com/simena86/b076b4ebb61d5268823b.js"></script>


The simple python server script below opens a TCP socket and receives the readings from the Android app over WLAN. Note that the python script reads the last entry in the receive buffer, which then makes up a LIFO que, and no timestamp is added to the reading. For a signal analysis one would add a time stamp and a FIFO que should be used instead. For debugging and pure fun, the method I used is still pretty sufficient.
`
The plotting is excecuted with piping the output from the python script to the perl script in the linux terminal:

{% highlight bash  %}
$ ./server.py | ./driveGnuPlot.pl 1 500 "Accelerometer Reading"
{% endhighlight  %}

Python server :

<script src="https://gist.github.com/simena86/6e2c0c6e8c35b0ac8e05.js"></script>

And lastly the python script pipes data to a Perl script written by Thanassis Tsiodras.

<script src="https://gist.github.com/simena86/8da192563c98405ed02f.js"></script>


