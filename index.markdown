---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Welcome
---

# Welcome to My Space

안녕하세요! 개발자 Hwoo의 공간입니다.

## Latest Posts

{% for post in site.posts limit:5 %}
<article class="post-card">
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <p class="post-meta">{{ post.date | date: "%B %d, %Y" }} • {{ post.category }}</p>
  <p>{{ post.excerpt }}</p>
</article>
{% endfor %}

## Featured Projects

{% for project in site.projects limit:3 %}
<div class="project-card">
  <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
  <p>{{ project.description }}</p>
</div>
{% endfor %}
