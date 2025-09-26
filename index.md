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
<p style="text-align: right;"><a href="{{ '/news.html' | relative_url }}">View all news &rarr;</a></p>


## Recent Exercises
{% for ex in site.data.exercises limit:2 %}
<div class="card">
  <h3>{{ ex.title }}</h3>
  <p class="meta">Due: {{ ex.date | date: "%B %d, %Y" }}</p>
  <p>{{ ex.description }}</p>
  <a href="{{ ex.file | relative_url }}" class="button">Download File</a>
</div>
{% endfor %}
<p style="text-align: right;"><a href="{{ '/all-exercises.html' | relative_url }}">View all exercises &rarr;</a></p>