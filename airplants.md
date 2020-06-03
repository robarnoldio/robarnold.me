---
layout: page
title: airplant (Tillandsia) collection
permalink: /airplants/
---
## Air plants currently in my collection

{% assign totalspend = 0 %}
{% for airplant in site.airplants %}

{% if airplant.categories contains "dead" %}~~{% endif %}{{ airplant.number }} - [{{ airplant.name }}]({{ airplant.url }}) purchased {{ airplant.date | date: "%b %Y" }} from {{ airplant.seller }}{% if airplant.categories contains "dead" %}~~{% endif %}

<!-------------------------------------
{% increment c %}
{% if airplant.categories contains "dead" %}{% increment d %}{% else %}{% increment l %}{% endif %}
{% assign totalspend = totalspend | plus: airplant.price %}
--------------------------------------->
{% endfor %}

## My current want list

* T. crocata giant
* T. duratii
* T. exserta
* T. intermedia
* T. ionantha Vanhyningii
* T. x Nidus

## Some crude stats

total: {{ c }}
living: {{ l }}
dead: {{ d }}
total: ${{ totalspend }}
average price: ${{ totalspend | divided_by: c }}

Last update: {{ "now" | date: "%b %d, %y" }}

Some debug stuff that I will subsequently delete: built {{ "now" | date: "%Y-%m-%d %H:%M" }}
