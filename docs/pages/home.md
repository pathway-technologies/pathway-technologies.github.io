---
layout: default
title: Home
permalink: /

banner-image: /assets/images/AdobeStock_169936222.jpeg
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
  <hr>

  <div class="w3-margin-top w3-cell-row">
    {% assign post = site.posts.first %}

    <div class="w3-container w3-cell w3-mobile">
      <img src="{{ post.banner-image }}" style="width:100%;">
    </div>

    <div class="w3-container w3-cell w3-mobile">
      <h2 class="w3-center">
        <a href="{{ post.url }}">{{ post.title }}</a>
      </h2>

      <p>
        By {{ post.author }} on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      {% assign preprocessed_content=post.content | replace: '</h', '.</h' %}
      {% assign cleaned_content=preprocessed_content | strip_html | truncatewords:50 %}

      <p>{{ cleaned_content }}</p>

      <p>
        <a href="{{ post.url }}">Read full article →</a>
      </p>
    </div>

  </div>

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
