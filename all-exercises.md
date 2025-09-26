---
layout: default
title: All Course Exercises
---

<div class="container">
  <h2>All Course Exercises</h2>
  <hr>

  {% for ex in site.exercises %}
  <div class="card exercise-list-card">
    <h3><a href="{{ ex.url | relative_url }}">{{ ex.title }}</a></h3>
    <p class="meta">Due: {{ ex.date | date: "%B %d, %Y" }}</p>
    <p>{{ ex.description }}</p>
    {% if ex.file %}
      <a href="{{ ex.file | relative_url }}" target="_blank" class="button">Download File <i class="fas fa-download"></i></a>
    {% endif %}
  </div>
  {% endfor %}
</div>