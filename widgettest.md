---
layout: page
title: testing widget collection yo
permalink: /widgets/
---

Opinions expressed on this site are not those of my employer, or probably of
anyone's employer. 

{% for widget in site.widgets %}
  <h2>{{ widget.name }} purchased for teh paltry sum of {{ widget.price }}</h2>
  <p>{{ widget.content | markdownify }}</p>
{% endfor %}
