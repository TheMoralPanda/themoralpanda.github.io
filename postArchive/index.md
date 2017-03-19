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
	{% for post in site.posts | sort: "date" %}

	<li>
		<a href="{{ fullUrl | append: post.url }}">{{ post.title }}</a>
		{{ post.date }}
	</li>
	      
	{% endfor %}
	</ul>
</div>



	