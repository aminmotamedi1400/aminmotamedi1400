---
layout: default
title: Participants
---


<div class="container"> 
  <h2>Teaching Staff</h2>
  {% for person in site.data.participants %}
    {% if person.role == "Teacher" or person.role == "Head TA" or person.role == "TA" %}
      <div class="card staff-card">
        <img src="{{ '/assets/images/' | append: person.photo | relative_url }}" alt="Photo of {{ person.name }}">
        <div>
          <h3>{{ person.name }}</h3>
          <p class="meta">{{ person.role }}</p>
          <p>{{ person.bio }}</p>
          {% if person.assigned_exercises %}
            <div class="assigned-exercises">
              <strong>Assigned Exercise:</strong>
              <ul>
                {% for exercise_title in person.assigned_exercises %}
                  {% assign found_exercise = site.exercises | where: "title", exercise_title | first %}

                  {% if found_exercise %}
                    <li><a href="{{ found_exercise.url | relative_url }}">{{ found_exercise.title }}</a></li>
                  {% else %}
                    <li>{{ exercise_title }} (Exercise page not found)</li>
                  {% endif %}
                {% endfor %}
              </ul>
            </div>
          {% endif %}
        </div>
      </div>
    {% endif %}
  {% endfor %}

  <br>

  <h2 id="students">Students</h2>
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
</div>