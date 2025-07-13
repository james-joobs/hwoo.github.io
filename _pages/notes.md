---
layout: page
title: Notes
permalink: /notes/
---

# Quick Notes & Learning

*Fast thoughts, ideas, and learning snippets*

{% assign notes = site.notes | sort: 'date' | reverse %}
{% for note in notes %}
## [{{ note.title }}]({{ note.url | relative_url }})
*{{ note.date | date: "%B %d, %Y" }}*

{% if note.tags %}
{% for tag in note.tags %}
`{{ tag }}` 
{% endfor %}
{% endif %}

{{ note.excerpt }}

---
{% endfor %} 