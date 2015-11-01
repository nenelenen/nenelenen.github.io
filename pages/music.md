---
layout: page-fullwidth
sidebar: false
show_meta: false
title:
subheadline:
teaser:
permalink: "/music/"
breadcrumb: false
---
<div class="row">
  <div class="large-9 large-push-3 columns" markdown="1">
#Music

## Concerts
I miei concerti

{% include list-posts tag='concert' %}

<small markdown="1">[Up to the top](#toc)</small>
{: .text-right }

## S.T.One
Sistema di diffusione omnidirezionale ideato e costruito da Giuseppe Silvi

<ul>
    {% for post in site.categories.STOne %}
    <li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>

<small markdown="1">[Up to the top](#toc)</small>
{: .text-right }

## EMUFest
Festival Internazionale di Musica Elettronica

{% include list-posts tag='EMUFest' %}

<small markdown="1">[Up to the top](#toc)</small>
{: .text-right }
</div>

<div class="large-3 large-pull-9 columns" markdown="1">
<div class="panel radius" markdown="1">
{: ##toc }
*  TOC
{:toc}
</div>
<div class="border-dotted radius b30">
  <img src="{{ site.url }}/images/banners/stage.jpg" alt="stage">
</div>
</div>

</div>
