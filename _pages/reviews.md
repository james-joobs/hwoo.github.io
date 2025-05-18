---
layout: page
title: Reviews
permalink: /reviews/
---

# Reviews

{% assign reviews = site.reviews | sort: 'date' | reverse %}
{% for review in reviews %}
## [{{ review.title }}]({{ review.url | relative_url }})
{{ review.date | date: "%B %d, %Y" }}

{{ review.excerpt }}

---
{% endfor %} 