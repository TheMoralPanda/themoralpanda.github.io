---
author_profile: true
comments: false
date: 2017-03-18 11:24:20+00:00
layout: single
title: Categories
---

{% include group-by-array collection=site.posts field='subcaty' %}
{% assign fullUrl = site.url | append: site.baseurl %}

<div class="categories_div" style="font-size:0.8em">
<ul>
  {% for catg in group_names %}
    {% assign posts = group_items[forloop.index0] %}

    <li>
      <h2>{{ catg }}</h2>
      <ul>
        {% for post in posts %}
        <li>
          <a href="{{ fullUrl | append: post.url }}">{{ post.title }}</a>
        </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
</div>