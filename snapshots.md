---
layout: default
title: Snapshots
permalink: /snapshots/
---

<h1>🖼️ Snapshots</h1>

<ul>
{% for post in site.posts %}
  {% if post.categories contains "Snapshots" %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>