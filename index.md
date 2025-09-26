---
layout: default
title: Dashboard
---

## Latest News
{% for item in site.data.news limit:2 %}
<div class="card">
  <h3>{{ item.title }}</h3>
  <p class="meta">Posted on: {{ item.date | date: "%B %d, %Y" }}</p>
  <p>{{ item.content }}</p>
</div>
{% endfor %}

<p style="text-align: right;">
  <a href="{{ '/news.html' | relative_url }}">View all news &rarr;</a>
</p>

## Recent Exercises
{% assign today = 'now' | date: "%Y-%m-%d" %}
{% assign upcoming_exercises = site.exercises | sort: "date" %}

{% for ex in upcoming_exercises limit:2 %}
{% assign ex_date = ex.date | date: "%Y-%m-%d" %}
{% if ex_date > today %}
<div class="card">
  <h3>{{ ex.title }}</h3>
  <p class="meta">Due: {{ ex.date | date: "%B %d, %Y" }}</p>
  <p>{{ ex.description }}</p>
  {% if ex.file %}
    <a href="{{ ex.file | relative_url }}" class="button">Download File</a>
  {% endif %}
</div>
{% endif %}
{% endfor %}

<p style="text-align: right;">
  <a href="{{ '/all-exercises.html' | relative_url }}">View all exercises &rarr;</a>
</p>