---
title: Publications
permalink: /publications/
---

# Publications and preprints

{% assign papers = site.papers | sort: "sort_key" | reverse %}
{% for paper in papers %}
## [{{ paper.title }}]({{ paper.url | relative_url }})

{{ paper.authors }}{% if paper.venue %}, {{ paper.venue }}{% endif %}{% if paper.year %}, {{ paper.year }}{% endif %}.

{% if paper.status %}**Status:** {{ paper.status }}.  
{% endif %}{% if paper.pdf %}[PDF]({{ paper.pdf | relative_url }}){% endif %}{% if paper.arxiv %}{% if paper.pdf %} · {% endif %}[arXiv]({{ paper.arxiv }}){% endif %}{% if paper.doi %} · [DOI]({{ paper.doi }}){% endif %}

{% if paper.abstract %}{{ paper.abstract }}{% endif %}

{% endfor %}
