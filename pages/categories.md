---
permalink: /categories/
layout: page
title: "Category Index"
---

{% capture site_categories %}{% for category in site.categories %}{{ category | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign categories_list = site_categories | split:',' | sort %}

<ul class="no-bullet">
  {% for item in (0..site.categories.size) %}{% unless forloop.last %}
    {% capture this_word %}{{ categories_list[item] | strip_newlines }}{% endcapture %}
    <li> <span class="icon-archive pr20"> <a href="#{{ this_word }}"> {{ this_word }} <span>{{ site.tags[this_word].size }}</span></a></span></li>
  {% endunless %}{% endfor %}
</ul>

{% for item in (0..site.categories.size) %}{% unless forloop.last %}
  {% capture this_word %}{{ categories_list[item] | strip_newlines }}{% endcapture %}
  <h2 id="{{ this_word }}" class="icon-archive pr20"> {{ this_word }}</h2>
  <ul class="post-list">
  {% for post in site.categories[this_word] %}{% if post.title != null %}
    <li><a href="{{ site.url }}{{ post.url }}">{{ post.title }} - <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span></a></li>
  {% endif %}{% endfor %}
  </ul>
{% endunless %}{% endfor %}
