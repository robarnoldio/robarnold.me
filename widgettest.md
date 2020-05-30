---
layout: page
title: widget collection
permalink: /widgets/
---

Opinions expressed on this site are not those of my employer, or probably of
anyone's employer.

{% for widget in site.widgets %}

## [{{ widget.name }}]({{widget.url}}) purchased for teh paltry sum of {{ widget.price }}
  
  {{ widget.content | markdownify }}
{% endfor %}
