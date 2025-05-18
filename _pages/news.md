---
layout: page
title: News
permalink: /news/
---

# News & Updates

{% assign news_items = site.news | sort: 'date' | reverse %}
{% for item in news_items %}
## [{{ item.title }}]({{ item.url | relative_url }})
{{ item.date | date: "%B %d, %Y" }}

{{ item.excerpt }}

---
{% endfor %} 