---
layout: default
title: Home
permalink: /

banner-image: /assets/images/AdobeStock_169936222.jpeg
banner-image-style: cover
banner-title: Engineering for Safety-Critical Systems
---

<div class="w3-container w3-margin-top">

  <!-- Hero Section -->
  <div class="w3-center w3-padding-32">
    <h1>Helping engineering teams build compliant, audit-ready systems</h1>
    <p class="w3-large">
      Specialising in ISO 26262, DevOps for regulated environments,
      and deterministic document workflows.
    </p>


    <div class="w3-margin-top">
      <a href="/services/" class="ptl-button">View Services</a>
      <a href="/about/" class="ptl-button">About Pathway Technologies</a>
      
      <a href="/newsletter/" class="ptl-button">
        Subscribe to newsletter
      </a>
    </div>
  </div>

  <!-- Services Overview -->
  <div class="w3-row-padding w3-padding-32">

    <div class="w3-third w3-margin-bottom">
      <div class="w3-card w3-padding">
        <h3>DevOps for Regulated Systems</h3>
        <p>
          Design and implement deterministic CI/CD pipelines aligned with
          safety standards and audit requirements.
        </p>
        <a href="/services/devops/">Learn more →</a>
      </div>
    </div>

    <div class="w3-third w3-margin-bottom">
      <div class="w3-card w3-padding">
        <h3>Training & Consultancy</h3>
        <p>
          Practical guidance and structured training in ISO 26262,
          safety workflows, and engineering process design.
        </p>
        <a href="/services/training-consultancy/">Learn more →</a>
      </div>
    </div>

    <div class="w3-third w3-margin-bottom">
      <div class="w3-card w3-padding">
        <h3>Document & Compliance Workflows</h3>
        <p>
          Transform engineering documentation into structured,
          traceable, and audit-ready artefacts.
        </p>
        <a href="/services/">Explore →</a>
      </div>
    </div>

  </div>

  <!-- Latest Blog Post -->
  <section class="ptl-home-feature" aria-labelledby="home-feature-title">
    {% assign post = site.posts.first %}

    {% if post.banner-image %}
      <img class="ptl-home-feature-image" src="{{ post.banner-image | relative_url }}" alt="{{ post.banner-alt | default: post.title | escape }}">
    {% endif %}

    <div class="ptl-home-feature-summary">
      <p class="ptl-home-feature-label">Latest article</p>
      <h2 id="home-feature-title"><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
      {% if post.sub-title %}
        <p class="ptl-home-feature-subtitle">{{ post.sub-title | escape }}</p>
      {% endif %}
      <p class="ptl-home-feature-meta">By {{ post.author | default: site.author | default: site.title }} <span aria-hidden="true">/</span> {{ post.date | date: "%B %-d, %Y" }}</p>
      {% assign preprocessed_content=post.content | replace: '</h', '.</h' %}
      {% assign cleaned_content=preprocessed_content | strip_html | truncatewords:50 %}
      <p>{{ cleaned_content }}</p>
      <a class="ptl-home-feature-link" href="{{ post.url | relative_url }}">Read article <span aria-hidden="true">&rarr;</span></a>
    </div>

  </section>

  <!-- Positioning / About -->
  <hr>

  <div class="w3-container w3-padding-32">
    <h2>About Pathway Technologies</h2>

    <p>
      Pathway Technologies supports engineering organisations working in
      safety-critical and regulated environments. We focus on delivering
      practical, structured solutions that improve compliance, traceability,
      and long-term maintainability.
    </p>

    <p>
      Our approach combines deep engineering experience with a strong emphasis
      on deterministic workflows, enabling teams to move faster while meeting
      regulatory obligations with confidence.
    </p>

    <a href="/about/">Learn more →</a>
  </div>

</div>
