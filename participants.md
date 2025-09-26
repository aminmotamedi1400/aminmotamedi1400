---
layout: default
title: Participants
---

## Teacher
{% for person in site.data.participants %}
  {% if person.role == "Teacher" %}
    <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="{{ person.name }}" width="100">
    <h3>{{ person.name }}</h3>
    <p><i>{{ person.bio }}</i></p>
  {% endif %}
{% endfor %}

<hr>

## Head TA & TAs
{% for person in site.data.participants %}
  {% if person.role == "Head TA" or person.role == "TA" %}
    <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="{{ person.name }}" width="100">
    <h3>{{ person.name }} ({{ person.role }})</h3>
    <p><i>{{ person.bio }}</i></p>
  {% endif %}
{% endfor %}

<hr>

## Students
<div style="display: flex; flex-wrap: wrap; gap: 20px;">
{% for person in site.data.participants %}
  {% if person.role == "Student" %}
    <div style="text-align: center;">
      <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="{{ person.name }}" width="100" style="border-radius: 50%;">
      <p>{{ person.name }}</p>
    </div>
  {% endif %}
{% endfor %}
</div>
