---
layout: page
title: Blog Posts
tagline: 
---
{% include JB/setup %}

<link href='http://fonts.googleapis.com/css?family=Open+Sans' rel='stylesheet' type='text/css'>


<style>
	table{
		border:0px solid black;
	}

	tr{
		border:0px solid black;
	}

	a:link.mylink{
		font-weight:600;
	}
	a:visited.mylink{
		font-weight:600;
	}
	.alignright { 
		text-align: right;
	    width: 23%;	
		font-family: "Open Sans" !important;
		color: #009933;
		border:0px solid black;

	}

	.alignleft { 
		text-align: left;
		font-family: "Open Sans";
		border:0px solid black;

	}

	a:hover {
		text-decoration: none;
	}
</style>

<table style="width:100%">
  {% for post in site.posts %} 
  <tr> 
  	<td class="alignright">
	<a class="mylink" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>  
	<br>
    {{ post.date | date_to_string }} 
	</td>
	<td class="alignleft">
	{{ post.content | more: "excerpt" }} 
	</td>
  </tr>
  {% endfor %}
</table>


