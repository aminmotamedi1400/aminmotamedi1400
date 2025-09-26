---
layout: default
title: Participants
---

## Teaching Staff
{% for person in site.data.participants %}
  {% if person.role == "Teacher" or person.role == "Head TA" or person.role == "TA" %}
    <div class="card staff-card">
      <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="Photo of {{ person.name }}">
      <div>
        <h3>{{ person.name }}</h3>
        <p class="meta">{{ person.role }}</p>
        <p>{{ person.bio }}</p>
      </div>
    </div>
  {% endif %}
{% endfor %}

<br>

## Students
<div class="student-grid">
{% for person in site.data.participants %}
  {% if person.role == "Student" %}
    <div class="student-card">
      <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="Photo of {{ person.name }}">
      <div class="name">{{ person.name }}</div>
    </div>
  {% endif %}
{% endfor %}
</div>