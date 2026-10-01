---
layout: default
title: Home
permalink: /

banner-image: /assets/images/AdobeStock_169936222.jpeg
banner-image-style: cover
banner-title-style: caption
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
  <div class="ptl-home-services">
    <section class="ptl-home-service">
      <h2>DevOps for Regulated Systems</h2>
      <p>Design and implement deterministic CI/CD pipelines aligned with safety standards and audit requirements.</p>
      <a href="/services/devops/">Learn more <span aria-hidden="true">&rarr;</span></a>
    </section>

    <section class="ptl-home-service">
      <h2>Training &amp; Consultancy</h2>
      <p>Practical guidance and structured training in ISO 26262, safety workflows, and engineering process design.</p>
      <a href="/services/training-consultancy/">Learn more <span aria-hidden="true">&rarr;</span></a>
    </section>

    <section class="ptl-home-service">
      <h2>Document &amp; Compliance Workflows</h2>
      <p>Transform engineering documentation into structured, traceable, and audit-ready artefacts.</p>
      <a href="/services/">Explore services <span aria-hidden="true">&rarr;</span></a>
    </section>
  </div>

  <!-- Latest Blog Post -->
  {% assign post = site.posts.first %}
  {% include ptl-post-feature.html post=post label="Latest article" %}

  <!-- Positioning / About -->
  <section class="ptl-home-about">
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
  </section>

</div>
