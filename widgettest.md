---
layout: page
title: widget collection
permalink: /widgets/
---

Here's a list of some thins in some order, I guess...

{% for widget in site.widgets %}

## #{{ widget.number}} [{{ widget.name }}]({{ widget.url }}) purchased for ${{ widget.price }}
  
  {{ widget.content | markdownify }}
{% endfor %}
