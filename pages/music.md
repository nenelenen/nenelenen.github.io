---
layout: page
show_meta: false
title: "Music"
subheadline: "my musical world"
teaser: "My principal musical projects"
permalink: "/music/"
breadcrumb: true
---
## S.T.One project

<ul>
    {% for post in site.categories.STOne %}
    <li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
