---
title: Home
permalink: /
---

<section class="hero">
  <div class="hero-text">
    <h1>Stefan Hoffelner</h1>
    <p class="lead">Set theory, forcing, descriptive set theory, and inner model theory.</p>
    <p>I am a project leader and senior postdoc in the Set Theory group at TU Wien. My research concerns definability and forcing, with a focus on separation, reduction and uniformization principles for projective sets of reals, definable well-orders, forcing axioms, and canonical inner models with Woodin cardinals.</p>
    <p class="button-row">
      <a class="button" href="{{ '/publications/' | relative_url }}">Publications</a>
      <a class="button" href="{{ '/research/' | relative_url }}">Research</a>
      <a class="button" href="{{ '/cv/' | relative_url }}">CV</a>
    </p>
  </div>
  <div class="hero-photo">
    <img src="{{ '/assets/Profilbild-Stefan.jpg' | relative_url }}" alt="Stefan Hoffelner">
  </div>
</section>

## Contact

**TU Wien**  
Research Unit Set Theory  
Institute of Discrete Mathematics and Geometry  
Email: <a href="mailto:stefan.hoffelner@tuwien.ac.at">stefan.hoffelner@tuwien.ac.at</a>  
ORCID: [0000-0003-0434-6554](https://orcid.org/0000-0003-0434-6554)

## Recent and selected papers

{% assign selected = site.papers | where: "selected", true | sort: "sort_key" | reverse %}
{% for paper in selected limit:6 %}
<div class="paper-item">
  <h3><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h3>
  <p class="paper-line">{{ paper.authors }}{% if paper.venue %}, {{ paper.venue }}{% endif %}{% if paper.year %}, {{ paper.year }}{% endif %}.</p>
  <p class="link-list">
    {% if paper.pdf %}<a href="{{ paper.pdf | relative_url }}">PDF</a>{% endif %}
    {% if paper.arxiv %}<a href="{{ paper.arxiv }}">arXiv</a>{% endif %}
    {% if paper.doi %}<a href="https://doi.org/{{ paper.doi }}">DOI</a>{% endif %}
  </p>
</div>
{% endfor %}

See the full [publications list]({{ '/publications/' | relative_url }}).
