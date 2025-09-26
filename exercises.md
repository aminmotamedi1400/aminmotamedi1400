---
layout: default
title: Exercises
---

{% for ex in site.data.exercises %}
<div class="card">
  <h3>{{ ex.title }}</h3>
  <p class="meta">Due: {{ ex.date | date: "%B %d, %Y" }}</p>
  <p>{{ ex.description }}</p>
  <a href="{{ ex.file | relative_url }}" class="button">Download File</a>
</div>
{% endfor %}