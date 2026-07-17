---
title: "Partners"
permalink: /partners/
layout: single
---
<div class="partner-grid">
  {% assign partners = site.partners | sort: "order" %}
  {% for partner in partners %}
  <div class="partner-tile">
    <a href="{{ partner.url }}" target="_blank" rel="noopener">
      <img src="{{ partner.logo | relative_url }}" alt="{{ partner.name }}" class="partner-logo">
    </a>
    <h4><a href="{{ partner.url }}" target="_blank" rel="noopener">{{ partner.name }}</a></h4>
    <p class="partner-description">{{ partner.description }}</p>
  </div>
  {% endfor %}
</div>
