---
layout: page
title: Team
permalink: /team/
---

{% assign group_order = "Principal Investigator, PhD Students, Collaborators, Alumni" | split: "," %}

{% for group_name in group_order %}
    {% assign members = site.data.team | where: "group", group_name %}
    {% if members.size > 0 %}
        ## {{group_name}}

        {% for person in members %}
        ### {{person.name}}

        {% endfor %}
    {% endif %}
{% endfor %}
