---
layout: page
title: Coffee collection
permalink: /coffee/
---

Here's a list of some coffee things in some order, I guess...

Figuring out how to actually use Jekyll's collection feature.

{% for coffee in site.coffee %}

{{ coffee.number }}: [{{ coffee.name }}]({{ coffee.url }}) purchased {{ %unless coffee.used }}new {{ %endunless }} for ${{ coffee.price }}
  
{% endfor %}
