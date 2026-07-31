---
layout: page
title: News
permalink: /news/
---

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url | relative_url }})
{{ post.date | date: "%B %-d, %Y" }}
{% endfor %}