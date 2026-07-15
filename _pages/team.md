---
title: "Team"
permalink: /team/
layout: single
---
{% assign members = site.team | sort: "order" %}
{% for member in members %}
<div class="team-member">
  <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" width="150">
  <h3>{{ member.name }}</h3>
  <p><em>{{ member.position }}</em></p>
  <div>{{ member.content | markdownify }}</div>
</div>
{% endfor %}
