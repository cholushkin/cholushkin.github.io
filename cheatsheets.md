---
layout: default
title: Cheatsheets
permalink: /cheatsheets/
---

<h1>📚 Cheatsheets</h1>

<div class="card-grid">
  {% for item in site.data.cheatsheets %}
  <a class="card" href="{{ item.url }}">
    <div>
      <div class="card-thumb">
        {% if item.thumbnail %}<img src="{{ item.thumbnail }}" alt="{{ item.title }}">{% endif %}
      </div>
      <h3>{{ item.title }}</h3>
    </div>
    <div class="card-cta">Open →</div>
    <div class="card-tags">
      {% for c in item.categories %}#{{ c }} {% endfor %}
    </div>
  </a>
  {% endfor %}
</div>
