---
layout: default
title: Services
permalink: /services/
description: Engineering services for regulated environments
banner-image: /assets/images/AdobeStock_281187282.jpeg
---

<section class="w3-container w3-padding-32">
  <h1>Services</h1>

  <p class="w3-large">
    Focused support for engineering teams operating in regulated
    and safety-critical environments.
  </p>
</section>

<section class="w3-container w3-padding-32">
  <div class="w3-row-padding">

    {% assign services = site.data.services | sort: "order" %}

    {%- for service in services -%}

    <div class="w3-half w3-margin-bottom">
      <div class="w3-card w3-padding">

        <h3>{{ service.title }}</h3>

        <p>{{ service.description }}</p>

        <!-- OPTIONAL: manual variation slot -->
        {%- if service.id == "devops" -%}
        <p>
          Focused on traceability, reproducibility, and auditability
          within CI/CD pipelines.
        </p>
        {% endif %}

        {%- if service.id == "training-consultancy" -%}
        <p>
          Bridging the gap between standards and practical engineering workflows.
        </p>
        {% endif %}

        <div class="w3-margin-top">
          <a
            href="{{ service.url | relative_url }}"
            class="w3-button w3-small w3-border"
            aria-label="View details for {{ service.title }}"
          >
            View details
          </a>
        </div>

      </div>
    </div>

    {% endfor %}

  </div>
</section>
