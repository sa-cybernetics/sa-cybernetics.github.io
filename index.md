---
layout: page
title: Blog Posts
tagline: 
---
{% include JB/setup %}


<style>
	table{
		border:0px solid black;
	}
	.alignright { 
		text-align: right;
	    width: 23%;	
		font-family: "Andale Mono", AndaleMono, monospace;
		color: #009933

	}
	a:hover {
		text-decoration: none;
	}

</style>

<ul class="posts">
<table style="width:100%">
  {% for post in site.posts %} 
  <tr>
  	<td class="alignright" >
	<a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}   </a>  
	<br>
    {{ post.date | date_to_string }} 
	</td>
	<td align>
	{{ post.content | more: "excerpt" }} </li>
	</td>
  </tr>
  {% endfor %}
</table>
</ul>



