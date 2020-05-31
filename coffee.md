---
layout: page
title: Coffee collection
permalink: /coffee/
---

Here's a list of some coffee things in some order, I guess...

Figuring out how to actually use Jekyll's collection feature.

{% for coffee in site.coffees %}

 #{{ coffee.number }} [{{ coffee.name }}]({{ coffee.url }}) purchased {{ %if coffee.new }}new {{ %endif }} for ${{ coffee.price }}
  
  {{ coffee.content | markdownify | truncate: 40 }}
{% endfor %}
