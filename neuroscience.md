
---
layout: page
title: Neuroscience
---

{% assign posts = site.categories.neuroscience %}
{% for post in posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.date | date: "%b %d, %Y" }}</p>
  </article>
{% endfor %}
