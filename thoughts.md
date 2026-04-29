---
layout: default
title: Thoughts
permalink: /thoughts/
---

# Thoughts

<ul>
{% for post in site.categories.thoughts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    ({{ post.date | date: "%Y-%m-%d" }})
  </li>
{% endfor %}
</ul>