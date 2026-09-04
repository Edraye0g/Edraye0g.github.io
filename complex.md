---
layout: page
title: Complex Science
---

{% assign posts = site.categories.complex %}
{% for post in posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.date | date: "%b %d, %Y" }}</p>
  </article>
{% endfor %}

