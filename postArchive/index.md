---
author_profile: true
comments: false
date: 2017-03-18 11:24:20+00:00
layout: single
title: All Posts
---

<div id="allPosts" style="font-size:0.7em">
	{% assign fullUrl = site.url | append: site.baseurl %}
	<ul>
	{% for post in site.posts %}

	<li>
		<a href="{{ fullUrl | append: post.url }}">{{ post.title }}</a> 
		<span style="font-size:0.65em"> {{ post.date | date: "%d %b , %Y" }} </span>				
	</li>
	      
	{% endfor %}
	</ul>
</div>



	