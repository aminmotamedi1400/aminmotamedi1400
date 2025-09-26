---
layout: default
title: Course News & Announcements
---

{% for item in site.data.news %}
<div class="card">
  <h3>{{ item.title }}</h3>
  <p class="meta">Posted on: {{ item.date | date: "%B %d, %Y" }}</p>
  <p>{{ item.content }}</p>
</div>
{% endfor %}