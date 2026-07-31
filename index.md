---
layout: home
title: Home
---

# Welcome

Welcome to the research group homepage

## Latest News

{% assign recent_news = site.data.news | sort: "date" | reverse | slice: 0, 3 %}
{% for item in recent_news %}
*{{ item.date | date_to_long_string }}*

{{ item.summary }}

{% endfor %}

[See all news →](/news/)