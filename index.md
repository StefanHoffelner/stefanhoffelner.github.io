---
title: Home
permalink: /
---

# Stefan Hoffelner

Set theory, forcing, descriptive set theory, and inner model theory.

I am a project leader and senior postdoc in the Set Theory group at TU Wien. My research concerns definability and forcing, with a focus on separation, reduction and uniformization principles for projective sets of reals, definable well-orders, forcing axioms, and canonical inner models with Woodin cardinals.

[Publications]({{ '/publications/' | relative_url }}) · [Research]({{ '/research/' | relative_url }}) · [CV]({{ '/cv/' | relative_url }})

## Contact

**TU Wien**  
Research Unit Set Theory  
Institute of Discrete Mathematics and Geometry  
Email: <stefan.hoffelner@tuwien.ac.at>  
ORCID: [0000-0003-0434-6554](https://orcid.org/0000-0003-0434-6554)

## Recent and selected papers

{% assign selected = site.papers | where: "selected", true | sort: "sort_key" | reverse %}
{% for paper in selected limit:6 %}
### [{{ paper.title }}]({{ paper.url | relative_url }})

{{ paper.authors }}{% if paper.venue %}, {{ paper.venue }}{% endif %}{% if paper.year %}, {{ paper.year }}{% endif %}.

{% if paper.pdf %}[PDF]({{ paper.pdf | relative_url }}){% endif %}{% if paper.arxiv %} · [arXiv]({{ paper.arxiv }}){% endif %}{% if paper.doi %} · [DOI]({{ paper.doi }}){% endif %}
{% endfor %}

See the full [publications list]({{ '/publications/' | relative_url }}).
