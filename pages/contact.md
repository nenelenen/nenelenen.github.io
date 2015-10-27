---
layout: page
title: ""
meta_title: "Contact me"
subheadline: ""
teaser: ""
permalink: "/contact/"
---


### ed@elenadalo.xyz
<hr>

<div id="subfootercont">
<section class="social-icons">
  <ul align="center" class="inline-list">
  {% for social_item in site.data.socialmedia %}
    <li><a href="{{ social_item.url }}" target="_blank" class="{{ social_item.class }}" title="{{ social_item.title }}"></a></li>
  {% endfor %}
  </ul>
</section>
</div>
