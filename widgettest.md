---
layout: page
title: widget collection
permalink: /widgets/
---

Here's a list of some things in some order, I guess...

Figuring out how to actually use Jekyll's collection feature.

{% for widget in site.widgets %}

## #{{ widget.number }} [{{ widget.name }}]({{ widget.url }}) purchased for ${{ widget.price }}
  {% raw %}{{ widget.excerpt }}{% endraw %}
###  {{ widget.content | markdownify }}
{% endfor %}
