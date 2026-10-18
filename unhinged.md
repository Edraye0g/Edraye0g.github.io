---
layout: page
title: "Unhinged Thoughts"
permalink: /unhinged/
---

{% assign posts = site.categories.unhinged %}
{% for post in posts %}
  <article class="post-preview-card">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%b %d, %Y" }}</p>
  </article>
{% endfor %}
