---
layout: page
title: airplant (Tillandsia) collection
permalink: /airplants/
---
## Air plants currently in my collection

{% for airplant in site.airplants %}

{% if airplant.categories contains "dead" %}~~{% endif %}{{ airplant.number }} - [{{ airplant.name }}]({{ airplant.url }}) purchased {{ airplant.date | date: "%b %Y" }} from {{ airplant.seller }}{% if airplant.categories contains "dead" %}~~{% endif %}

{% increment count %}
{% if airplant.categories contains "dead" %}{% increment deadcount %}{% else %}{% increment livecount %}{% endif %}

{% endfor %}

## My current want list

* T. crocata giant
* T. duratii
* T. exserta
* T. intermedia
* T. ionantha Vanhyningii
* T. x Nidus

## Some crude stats

total: {{ count }}
living: {{ livecount }}
dead: {{ deadcount }}

Last update: {{ "now" | date: "%b %d, %y" }}

Some debug stuff that I will subsequently delete: built {{ "now" | date: "%Y-%m-%d %H:%M" }}
