---
layout: default
title: "Home"
---

# Stefan Hoffelner — Research

Welcome. Below are my research papers.

<ul>
  {% for p in site.papers reversed %}
    <li>
      <a href="{{ p.url }}">{{ p.title }}</a>
      {% if p.authors %} — {{ p.authors }}{% endif %}
      {% if p.year %} ({{ p.year }}){% endif %}
    </li>
  {% endfor %}
</ul>

You can download PDFs from each paper page.
