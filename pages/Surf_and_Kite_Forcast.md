---
layout: page
css: surf_scroll_style
title: "Surf and Kite Forecast"
description: ""
---
{% include JB/setup %}

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
<script>
$(document).ready(function() {
    var s = $("#sticker");
    var pos = s.position();                    
    $(window).scroll(function() {
        var windowpos = $(window).scrollTop();
        if (windowpos - 210 >= pos.top) {
            s.addClass("stick");
        	s.html("<img src='/images/surf_kite_forcast/windarrows.png'>" );
        } else {
            s.removeClass("stick"); 
        	s.html("" );
        }
    });
});

</script>
<link rel="stylesheet" href="my_styles.css">
<div id='sticker'>  </div>

##Spots:

[Hamresanden](#hamresanden)
<br>
[Høllen](#hllen)
<br>
[Sjøsanden](#sjsanden)
<br>
[Havika](#havika)


---



### <a name="hamresanden"> Hamresanden </a>



This spot is a short drive away from Kristiansand.
     
        



<script src="http://www.yr.no/place/Norway/Vest-Agder/Kristiansand/Hamresanden/external_box_three_days.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Kristiansand/Hamresanden/">yr.no: Forecast for Hamresanden</a></noscript>
<script src="http://www.yr.no/place/Norway/Vest-Agder/Kristiansand/Hamresanden/external_box_hour_by_hour.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Kristiansand/Hamresanden/">yr.no: Forecast for Hamresanden</a></noscript>


---

###<a name="hllen">Høllen, Søgne </a>

<script src="http://www.yr.no/place/Norway/Vest-Agder/Søgne/Høllen/external_box_three_days.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Søgne/Høllen/">yr.no: Forecast for Høllen</a></noscript>
<script src="http://www.yr.no/place/Norway/Vest-Agder/Søgne/Høllen/external_box_hour_by_hour.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Søgne/Høllen/">yr.no: Forecast for Høllen</a></noscript>

---


###<a name="sjsanden">Sjøsanden, Mandal </a>

<script src="http://www.yr.no/place/Norway/Vest-Agder/Mandal/Sjøsanden/external_box_three_days.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Mandal/Sjøsanden/">yr.no: Forecast for Sjøsanden</a></noscript>
<script src="http://www.yr.no/place/Norway/Vest-Agder/Mandal/Sjøsanden/external_box_hour_by_hour.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Mandal/Sjøsanden/">yr.no: Forecast for Sjøsanden</a></noscript>

---

###<a name="havika">Havika, Farsund</a>

<script src="http://www.yr.no/place/Norway/Vest-Agder/Farsund/Havika/external_box_three_days.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Farsund/Havika/">yr.no: Forecast for Havika</a></noscript>
<script src="http://www.yr.no/place/Norway/Vest-Agder/Farsund/Havika/external_box_hour_by_hour.js"></script><noscript><a href="http://www.yr.no/place/Norway/Vest-Agder/Farsund/Havika/">yr.no: Forecast for Havika</a></noscript>


---
