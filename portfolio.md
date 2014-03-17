---
Time-stamp: <2013-07-28 23:52:14 ()>
layout: page
title: Portfolio
tagline: <img src="http://mrenaud.ca/images/pylon.png" height="30px" /> Under Construction
---
<!-- The site where I got the information about category-page from http://stackoverflow.com/questions/17118551/generating-a-list-of-pages-not-posts-in-a-given-category -->
This page contains a collection of a handful of my recent work.


{% for cat in site.category-list %}
<h3>{{ cat }}</h3>
<div class="post">
<h3 class="page-title">
{% for page in site.pages %}
{% if page.portfolio == true %}
{% for pc in page.categories %}
{% if pc == cat %}
<img src={{ page.image }} class="float" />{{ page.title }} </h3>  <span class="page-excerpt">{{ page.desc }}</span>
{% endif %} 
{% endfor %} 
{% endif %} 
{% endfor %} 
</div><hr>
{% endfor %}