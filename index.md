---
layout: default
title: Home
---

## Latest News
{% for item in site.data.news limit:2 %}
### {{ item.title }}
*Posted on: {{ item.date | date: "%B %d, %Y" }}*
<p>{{ item.content }}</p>
{% endfor %}
<a href="{{ '/news.html' | relative_url }}">View all news...</a>

<hr>

## Recent Exercises
{% for ex in site.data.exercises limit:2 %}
### {{ ex.title }}
*Due: {{ ex.date | date: "%B %d, %Y" }}*
<p>{{ ex.description }}</p>
<p><a href="{{ ex.file | relative_url }}">Download File</a></p>
{% endfor %}
<a href="{{ '/exercises.html' | relative_url }}">View all exercises...</a>
