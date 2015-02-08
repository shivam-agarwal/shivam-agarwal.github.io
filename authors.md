---
layout: page
title: Authors
permalink: /authors/
---

<ul class="tags-box">
{% if site.posts != empty %}
author list: 
{% for cat in site.authors %}
{{ cat[0] }} .... {{ cat }} .... {{ cat[1].size }}
<a href="#{{ cat[0] }}" title="{{ cat[0] }}" rel="{{ cat[1].size }}">{{ cat[0] | join: "/"}}<span class="size"> {{ cat[1].size }}</span></a>
{% endfor %}
now category:
{% for cat in site.categories %}
<a href="#{{ cat[0] }}" title="{{ cat[0] }}" rel="{{ cat[1].size }}">{{ cat[0] | join: "/"}}<span class="size"> {{ cat[1].size }}</span></a>
{% endfor %}
</ul>

<ul class="tags-box">
{% for cat in site.categories %}
<li id="{{ cat[0] }}">{{ cat[0]}}</li>
{% for post in cat[1] %}
<time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time> &raquo;
<a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a><br />
{% endfor %}
{% endfor %}
{% else %}
<span>No posts</span>
{% endif %}
</ul>

