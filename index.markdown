---
layout: home
---

## Recent Posts

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url | relative_url }})
*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

---
{% endfor %}

## Quick Access

### 📝 [Latest Notes]({{ "/notes/" | relative_url }})
Quick thoughts and learning notes
{% assign recent_notes = site.notes | sort: 'date' | reverse %}
{% for note in recent_notes limit:3 %}
- [{{ note.title }}]({{ note.url | relative_url }}) - *{{ note.date | date: "%m/%d" }}*
{% endfor %}

### 🚀 [Recent Projects]({{ "/projects/" | relative_url }})
ML projects and experiments
{% assign recent_projects = site.projects | sort: 'date' | reverse %}
{% for project in recent_projects limit:3 %}
- [{{ project.title }}]({{ project.url | relative_url }}) - *{{ project.date | date: "%B %Y" }}*
{% endfor %}

