---
layout: default
title: Sandbox
permalink: /sandbox/
---

<h1>🧪 Sandbox</h1>

<div class="card-grid">
  {% for item in site.data.sandbox %}
  <a class="card" href="{{ item.url }}" target="_blank" rel="noopener">
    <div>
      <div class="card-thumb">
        {% if item.thumbnail %}<img src="{{ item.thumbnail }}" alt="{{ item.title }}">{% endif %}
      </div>
      <h3>{{ item.title }}</h3>
      <div class="card-description">{{ item.description }}</div>
    </div>
    <div class="card-tags">
      {% for t in item.tags %}#{{ t }} {% endfor %}
    </div>
  </a>
  {% endfor %}
</div>
