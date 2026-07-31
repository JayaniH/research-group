---
layout: page
title: Projects
permalink: /projects/
---

{% for project in site.data.projects %}
### {{ project.title }}
*{{ project.status }}*

{{ project.summary }}

{% endfor %}