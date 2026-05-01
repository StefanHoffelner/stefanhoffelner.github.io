---
layout: default
title: "Home"
---

# Stefan Hoffelner — Research
<p><a href="/cv/"><strong>View my Curriculum Vitae (CV)</strong></a></p>
<img src="/assets/Profilbild-Stefan.jpg" alt="Stefan Hoffelner" width="220" style="float: right; margin-left: 20px; border-radius: 5%; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
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
