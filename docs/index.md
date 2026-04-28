---
layout: default
title: Pages index
---

# Articles

<ul>
{% assign pages_list = site.pages | where_exp: "p", "p.path contains '.md'" | sort: "title" %}
{% for page in pages_list %}
  {% if page.path != "index.md" and page.title %}
  <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>
