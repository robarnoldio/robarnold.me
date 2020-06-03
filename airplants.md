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
{% if airplant.categories contains "noid" %}{% increment n %}{% endif %}
{% if airplant.categories contains "bloom" %}{% increment b %}{% endif %}
{% if airplant.categories contains "hybrid" %}{% increment h %}{% endif %}
{% if airplant.categories contains "pup" %}{% increment p %}{% endif %}
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

* total: {{ c }} {% assign cc = c %}
* living: {{ l }} {% assign ll = l %}
* dead: {{ d }}
* survival rate: {{ ll | divided_by: cc | times: 100.0 | round: 2 }}
* pupping: {{ p }}
* unidentified: {{ n }}
* bloomed: {{ b }}
* hybrid: {{ h }}
* total: ${{ totalspend | round: }}
* average price: ${{ totalspend | divided_by: c | round: 2 }}

Last update: {{ "now" | date: "%b %d, %y" }}
