---
layout: page
title: "Unhinged Thoughts"
---

{% assign posts = site.categories.unhinged %}
{% for post in posts %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.date | date: "%b %d, %Y" }}</p>
  </article>
{% endfor %}
