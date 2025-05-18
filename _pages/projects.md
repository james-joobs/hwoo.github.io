---
layout: page
title: Projects
permalink: /projects/
---

# My Projects

{% for project in site.projects %}
<div class="project-card">
  <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
  <p>{{ project.description }}</p>
  {% if project.github_link %}
    <a href="{{ project.github_link }}" class="github-link">View on GitHub</a>
  {% endif %}
</div>
{% endfor %} 