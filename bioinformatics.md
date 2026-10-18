---
layout: page
title: "Bioinformatics"
permalink: /bioinformatics/
---

{% assign posts = site.categories.bioinformatics %}
{% if posts.size > 0 %}
  {% for post in posts %}
    <article class="post-preview-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%b %d, %Y" }}</p>
    </article>
  {% endfor %}
{% else %}
  <p>Reviews in Bioinformatics are in progress. Stay tuned!</p>
{% endif %}
