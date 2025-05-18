---
layout: page
title: Thoughts
permalink: /thoughts/
---

# My Thoughts

{% for post in site.categories.thoughts %}
<article class="post-card">
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
  <p>{{ post.excerpt }}</p>
</article>
{% endfor %} 