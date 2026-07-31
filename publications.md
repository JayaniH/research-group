---
layout: page
title: publications
permalink: /publications/
---

{% assign publications = site.data.publications | sort: "year" | reverse %}
{% for publication in publications %}
{% if publication.doi != "" %}
{{ publication.authors }} ({{ publication.year }}). {{ publication.title }}. *{{ publication.venue }}*. [https://doi.org/{{ publication.doi }}](https://doi.org/{{ publication.doi }})
{% else %}
{{ publication.authors }} ({{ publication.year }}). {{ publication.title }}. *{{ publication.venue }}*
{% endif %}
{% endfor %}