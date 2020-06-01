---
layout: page
title: airplant (Tillandsia) collection
permalink: /airplants/
---
## Air plants currently in my collection

{% for airplant in site.airplants %}

{% if airplant.categories contains "dead" %}~~{% endif %}{{ airplant.number }}. [{{ airplant.name }}]({{ airplant.url }}) purchased {{ airplant.date | date: "%b %Y" }}{% if airplant.categories contains "dead" %}~~{% endif %}

{% endfor %}

## My current want list

* T. crocata giant
* T. duratii
* T. exserta
* T. intermedia
* T. ionantha Vanhyningii
* T. x Nidus

Last update: {{ "now" | date: "%b %d, %y" }}
Some debug stuff that I will subsequently delete: built {{ "now" | date: "%Y-%m-%d %H:%M" }}
