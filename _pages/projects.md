---
title: "Projects"
permalink: /projects/
layout: single
---
{% assign projects = site.projects | sort: "order" %}
{% for project in projects %}
<div class="project-entry">
  <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" width="300">
  <h3>{{ project.title }}</h3>
  <p><em>Status: {{ project.status }}</em></p>
  {% if project.tags %}
  <p>
    {% for tag in project.tags %}<span class="tag">{{ tag }}</span> {% endfor %}
  </p>
  {% endif %}
  <div>{{ project.content | markdownify }}</div>
</div>
{% endfor %}
