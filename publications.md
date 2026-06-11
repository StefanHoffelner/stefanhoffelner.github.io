---
title: Publications
permalink: /publications/
---

# Publications and preprints

{% assign published = site.papers | where: "status", "published" | sort: "sort_key" | reverse %}
{% assign preprints = site.papers | where: "status", "preprint" | sort: "sort_key" | reverse %}
{% assign theses = site.papers | where: "status", "thesis" | sort: "sort_key" | reverse %}

## Published and accepted papers

{% for paper in published %}
<div class="paper-item">
  <h2><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h2>
  <p class="paper-line">
    {{ paper.authors }}{% if paper.venue %}, {{ paper.venue }}{% endif %}{% if paper.year %}, {{ paper.year }}{% endif %}.
  </p>
  <p class="link-list">
    {% if paper.pdf %}<a href="{{ paper.pdf | relative_url }}">PDF</a>{% endif %}
    {% if paper.arxiv %}<a href="{{ paper.arxiv }}">arXiv</a>{% endif %}
    {% if paper.doi %}<a href="{{ paper.doi }}">DOI</a>{% endif %}
  </p>
</div>
{% endfor %}

## Preprints and manuscripts

{% for paper in preprints %}
<div class="paper-item">
  <h2><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h2>
  <p class="paper-line">
    {{ paper.authors }}{% if paper.venue %}, {{ paper.venue }}{% endif %}{% if paper.year %}, {{ paper.year }}{% endif %}.
  </p>
  <p class="link-list">
    {% if paper.pdf %}<a href="{{ paper.pdf | relative_url }}">PDF</a>{% endif %}
    {% if paper.arxiv %}<a href="{{ paper.arxiv }}">arXiv</a>{% endif %}
    {% if paper.doi %}<a href="{{ paper.doi }}">DOI</a>{% endif %}
  </p>
</div>
{% endfor %}

## Thesis

{% for paper in theses %}
<div class="paper-item">
  <h2><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h2>
  <p class="paper-line">
    {{ paper.authors }}{% if paper.venue %}, {{ paper.venue }}{% endif %}{% if paper.year %}, {{ paper.year }}{% endif %}.
  </p>
  <p class="link-list">
    {% if paper.pdf %}<a href="{{ paper.pdf | relative_url }}">PDF</a>{% endif %}
    {% if paper.arxiv %}<a href="{{ paper.arxiv }}">arXiv</a>{% endif %}
    {% if paper.doi %}<a href="{{ paper.doi }}">DOI</a>{% endif %}
  </p>
</div>
{% endfor %}
