---
inpage: true
layout: page
css: surf_scroll_style
title: "Surf and Kite Forecast"
description: ""
---
{% include JB/setup %}

<style>
	table{
		border:0px solid black;
	}

	.left { 
		text-align: left;
	    width: 13%;	
		font-family: "Andale Mono", AndaleMono, monospace;
		color: #009933

	}
	.right { 
		text-align: left;
		font-family: "Andale Mono", AndaleMono, monospace;
		color: #009933
	}
</style>

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
<script>
jQuery(function(){
         jQuery('#showall').click(function(){
               jQuery('.targetDiv').show();
        });
        jQuery('.showSingle').click(function(){
              jQuery('.targetDiv').hide();
              jQuery('#div'+$(this).attr('target')).show();
        });
});
</script>
<style>

#wrapper { width: 468*0.8px; height: 290*0.8px; padding: 0; overflow: hidden; }
#scaled-frame { width: 0.8*468px; height: 0.8*290px; border: 0px; }
#scaled-frame {
    zoom: 0.8;
    -moz-transform: scale(0.8);
    -moz-transform-origin: 0 0;
    -o-transform: scale(0.8);
    -o-transform-origin: 0 0;
    -webkit-transform: scale(0.8);
    -webkit-transform-origin: 0 0;
}

@media screen and (-webkit-min-device-pixel-ratio:0) {
 #scaled-frame  { zoom: 1;  }
}

</style>

<link rel="stylesheet" href="my_styles.css">
<div id='sticker'>  </div>

<div id="menu" style="height:1200px;width:120px;float:left;">
	<b> Spots </b>
	<br>
	<a  class="showSingle" target="1">Hamresanden</a>
	<br>
	<a  class="showSingle" target="2">Høllen</a>
	<br>
	<a  class="showSingle" target="3">Kviljo</a>
</div>

<div id="content" style="height:1200px;width:400px;float:left;">
	<div id="div1" class="targetDiv" style="display:none">
		<img src="http://www.yr.no/sted/Norge/Vest-Agder/Kristiansand/Hamresanden~2229/meteogram.png" width="700" height="200">
		<iframe id="scaled-frame" src="http://www.yr.no/place/Norway/Vest-Agder/Kristiansand/Hamresanden/external_box_three_days.html" 
		width="468" height="290" frameborder="0" style="margin: 10px 0 10px 0" scrolling="no"></iframe>
	</div>
	<div id="div2" class="targetDiv" style="display:none">
		<img src="http://www.yr.no/sted/Norge/Vest-Agder/S%c3%b8gne/H%c3%b8llen/meteogram.png" width="700" height="200">
		<iframe id="scaled-frame" src="http://www.yr.no/place/Norway/Vest-Agder/S%c3%b8gne/H%c3%b8llen/external_box_three_days.html" 
		width="468" height="290" frameborder="0" style="margin: 10px 0 10px 0" scrolling="no"></iframe>
	</div>
	<div id="div3" class="targetDiv" style="display:none">
		<img src="http://www.yr.no/sted/Norge/Vest-Agder/Farsund/Kviljosanden/meteogram.png" width="700" height="200">
		<iframe id="scaled-frame" src="http://www.yr.no/place/Norway/Vest-Agder/Farsund/Kviljobukta~2219861/external_box_three_days.html"
		width="468" height="290" frameborder="0" style="margin: 10px 0 10px 0" scrolling="no"></iframe>
	</div>


</div>

