---
layout: page
title: Projects
permalink: /projects/
---

# ML Projects

{% assign projects = site.projects | sort: 'date' | reverse %}
{% for project in projects %}
## [{{ project.title }}]({{ project.url | relative_url }})
*{{ project.date | date: "%B %Y" }}*

{% if project.tech %}
**Tech Stack:** {{ project.tech }}
{% endif %}

{{ project.excerpt }}

{% if project.github %}
[🔗 GitHub]({{ project.github }})
{% endif %}

---
{% endfor %} 