---
layout: default
title: Sandbox
permalink: /sandbox/
---

<h1>Sandbox</h1>

<ul>
{% for post in site.posts %}
  {% if post.categories contains "Sandbox" %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>