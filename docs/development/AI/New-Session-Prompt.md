# New Session Prompt

# Pathway Technologies Website

## Overview

Pathway Technologies is a consultancy focused on engineering for regulated and safety-critical environments.

The website serves four primary purposes:

1. Explain services and areas of expertise
2. Establish credibility and trust
3. Publish technical articles and thought leadership
4. Provide contact and newsletter subscription mechanisms

The site is intentionally minimalist and engineering-focused. It avoids marketing-heavy language, excessive graphics, and corporate boilerplate.

---

# Positioning

Pathway Technologies supports organisations operating in regulated environments where compliance, traceability, and auditability are important.

Typical areas include:

- Functional safety
- DevOps for regulated systems
- Engineering process improvement
- Technical training
- Structured documentation workflows

The site targets engineering managers, technical leaders, safety engineers, quality teams, and regulated industry organisations.

---

# Design Principles

The website emphasises:

- Clarity
- Simplicity
- Maintainability
- Accessibility
- Consistency

The preferred style is:

- Professional
- Technical
- Informative
- Trustworthy

Avoid:

- Marketing buzzwords
- Excessive animations
- Aggressive calls-to-action
- Generic corporate language

---

# Technology Stack

## Site Generator

Jekyll

## CSS Framework

W3.CSS

## Custom Layer

SCSS with custom `ptl-*` classes.

The custom layer should provide:

- Semantic styling
- Consistent colour system
- Consistent spacing system
- Reusable components

Avoid large numbers of direct W3CSS utility classes in content where a reusable semantic class is appropriate.

---

# Layout Architecture

## Primary Layout

```
base/default layout
├── navigation
├── optional banner
├── main content
└── footer
```

The page body uses a flex layout to support a sticky footer:


```
.ptl-page {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
.ptl-main {
  flex: 1;
}
```

---

# Design System

## Navigation Colours

```
.ptl-nav-bg-color
.ptl-nav-bg-active
.ptl-nav-bg-hover
```

These define navigation appearance through semantic classes.

---

## Buttons

Buttons should use semantic classes rather than direct W3CSS usage.

Preferred pattern:

```
.ptl-button
```

Optional variants:

```
.ptl-button-secondary
```

Use a consistent colour scheme across the entire site.

---

## Vertical Rhythm

The site uses a consistent spacing system.

Typical scale:

```
$ptl-space-xs
$ptl-space-sm
$ptl-space-md
$ptl-space-lg
```

Spacing is controlled centrally through SCSS.

---

# Content Architecture

## Main Sections

### Home

Introduces:

- Services
- Positioning
- Latest article
- Newsletter
- About summary

### Services

Service catalogue and navigation.

### About

Describes:

- Background
- Expertise
- Approach
- Focus areas
- Working principles

The About page establishes credibility rather than containing traditional corporate vision/mission statements.

### Contact

Primary contact channel is email.

The Contact page explains how engagements typically begin.

### Privacy

Public privacy policy.

### Newsletter

Newsletter signup page.

---

# Branding

The company logo should appear on the About page.

Guidelines:

- Visible but not dominant
- Responsive
- Mobile-friendly
- Supporting rather than driving content

Text remains the primary focus.

---

# Footer

The footer should always provide easy access to:

- Contact
- Privacy
- Newsletter
- LinkedIn

Future legal links may be added as required.

---

# Blog Philosophy

Articles should:

- Demonstrate expertise
- Educate readers
- Support engineering organisations

Content should emphasise:

- Practical engineering
- Compliance
- Traceability
- Safety
- Process improvement

Articles should avoid overt sales language.

---

# Privacy and Compliance Strategy

## General Approach

Pathway Technologies is a Hong Kong registered company.

The company voluntarily aligns its data-processing approach with GDPR principles where practical.

Reasons include:

- European customer base
- Regulated-industry focus
- Consistent privacy expectations

---

## Core Principles

- Data minimisation
- Transparency
- Purpose limitation
- Appropriate safeguards
- Explicit consent

---

## Infrastructure Philosophy

Infrastructure is selected to minimise data exposure.

European-hosted services are preferred where practical.

Data residency and supplier selection should consider customer privacy expectations.

---

# Email and Newsletter Strategy

## Objectives

Maintain a low-volume technical newsletter.

Newsletter content should provide:

- Technical insights
- Regulatory developments
- Process and compliance topics

Avoid aggressive marketing campaigns.

---

## Consent Model

Newsletter subscriptions must use:

- Explicit consent
- Double opt-in
- Privacy Policy linkage
- Unsubscribe mechanism

No purchased lists.

No scraped contacts.

No automatic enrolment from email enquiries.

---

## Email Service Providers

Preferred characteristics:

- GDPR-aligned operation
- Good deliverability
- Strong consent management
- European hosting where practical

Brevo is currently an available platform.

Mailjet remains a potential future platform.

Provider selection should not affect public-facing processes.

---

# Internal Governance

The company maintains internal documentation covering:

- Email and customer data handling
- Consent management
- Data retention
- Third-party processors

Internal policy may be more detailed than public disclosures but must remain consistent with the public Privacy Policy.

---

# Future Development Principles

Future changes should prioritise:

1. Maintainability
2. Compliance
3. Simplicity
4. Consistency
5. User trust

New features should integrate into existing architecture rather than introducing parallel systems.

# Machine-Readable JSON Summary

```json
{
  "project": {
    "name": "Pathway Technologies Website",
    "type": "Jekyll website",
    "framework": "W3.CSS",
    "custom_css_prefix": "ptl"
  },
  "positioning": {
    "focus": [
      "functional safety",
      "regulated engineering",
      "devops",
      "compliance",
      "training",
      "traceability"
    ],
    "tone": [
      "technical",
      "professional",
      "minimalist",
      "trustworthy"
    ]
  },
  "architecture": {
    "layout": [
      "navigation",
      "banner",
      "main",
      "footer"
    ],
    "sticky_footer": true,
    "design_system": true
  },
  "pages": [
    "home",
    "services",
    "about",
    "contact",
    "privacy",
    "newsletter",
    "blog"
  ],
  "privacy": {
    "entity": "Pathway Technologies Ltd.",
    "jurisdiction": "Hong Kong",
    "gdpr_aligned": true,
    "data_minimisation": true
  },
  "newsletter": {
    "enabled": true,
    "double_opt_in": true,
    "explicit_consent": true,
    "marketing_style": "low_volume_technical",
    "purchased_lists_allowed": false
  },
  "infrastructure": {
    "eu_preferred": true,
    "privacy_focused": true
  },
  "branding": {
    "logo_on_about_page": true,
    "content_first": true
  }
}
```
