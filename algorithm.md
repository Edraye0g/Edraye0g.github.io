---
layout: page
title: Algorithms
permalink: /algorithm/
---

{% assign posts = site.categories.algorithm %}
{% for post in posts %}
  <article class="post-preview-card">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%b %d, %Y" }}</p>
  </article>
{% endfor %}
