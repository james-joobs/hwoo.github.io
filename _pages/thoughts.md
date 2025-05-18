---
layout: page
title: Thoughts
permalink: /thoughts/
---

# Thoughts

{% assign thoughts = site.thoughts | sort: 'date' | reverse %}
{% for thought in thoughts %}
## [{{ thought.title }}]({{ thought.url | relative_url }})
{{ thought.date | date: "%B %d, %Y" }}

{{ thought.excerpt }}

---
{% endfor %} 