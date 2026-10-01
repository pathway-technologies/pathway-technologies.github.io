---
layout: page
title: Services
permalink: /services/
description: Engineering services for regulated environments
banner-image: /assets/images/AdobeStock_281187282.jpeg
---

<p class="ptl-service-intro">
  Focused support for engineering teams operating in regulated and
  safety-critical environments.
</p>

<p class="ptl-subtle-note">
  Infrastructure is intentionally selected to minimise data exposure,
  with a preference for European-hosted services where practical.
</p>

<div class="ptl-service-list">
  {% assign services = site.data.services | sort: "order" %}

  {% for service in services %}
    <section class="ptl-service-item">
      <h2>{{ service.title }}</h2>
      <p>{{ service.description }}</p>

      {% if service.id == "devops" %}
        <p>Focused on traceability, reproducibility, and auditability within CI/CD pipelines.</p>
      {% elsif service.id == "training-consultancy" %}
        <p>Bridging the gap between standards and practical engineering workflows.</p>
      {% endif %}

      <a href="{{ service.url | relative_url }}" class="ptl-button"
         aria-label="View details for {{ service.title }}">
        View details
      </a>
    </section>
  {% endfor %}
</div>
