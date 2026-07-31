---
layout: page
title: News
permalink: /news/
---

{% assign items = site.data.news | sort: "date" | reverse %}
{% for item in items %}
#### {{ item.headline }}
*{{ item.date | date_to_long_string }}*  
{{ item.content }}
---
{% endfor %}