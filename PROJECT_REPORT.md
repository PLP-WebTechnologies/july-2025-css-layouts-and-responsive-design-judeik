# Pure Honey Shop — Assignment Report

**Project file name:** `index.html`, `style.css`  
**Report file name:** `PROJECT_REPORT.md`  
**Course:** CSS Layouts & Responsive Web Design  
**Student:** Ojobor Jude Ikechukwu  
**Date:** August 28, 2025

---

## Table of Contents

- [Pure Honey Shop — Assignment Report](#pure-honey-shop--assignment-report)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Objectives](#objectives)
  - [Deliverables](#deliverables)
  - [Design \& Layout Approach](#design--layout-approach)
    - [Visual and UX Goals](#visual-and-ux-goals)
    - [Grid usage](#grid-usage)
    - [Flexbox usage](#flexbox-usage)
  - [Responsive Strategy \& Breakpoints](#responsive-strategy--breakpoints)
  - [Accessibility \& Screen Reader Support](#accessibility--screen-reader-support)
  - [SEO \& Performance Considerations](#seo--performance-considerations)
  - [Features \& Content Summary](#features--content-summary)
  - [How to Run / Preview Locally](#how-to-run--preview-locally)

---

## Overview

**Pure Honey Shop** is a professional, creative, and accessible single-page e-commerce demo site built only with **HTML5** and **CSS** (no frameworks). It demonstrates advanced layout techniques using **CSS Grid** and **Flexbox**, includes responsive breakpoints down to **200px**, and follows accessibility and SEO best practices required by the assignment.

This project was created specifically to fulfil the "CSS Layouts & Responsive Web Design" assignment by demonstrating structure, flexibility, responsive behavior, and content organization.

---

## Objectives

- Use **Flexbox** for 1D layout problems and small component alignment.
- Use **CSS Grid** for complex 2D multi-column layouts.
- Apply **responsive design** using media queries and relative units.
- Produce a clean, well-documented, and accessible page that adapts from 200px (very small phones) up to desktop.
- Build an attractive, SEO-friendly page using **only two standard colors** (Honey Gold `#d4a017`, Dark Brown `#3b2f2f`) as required.
- Add professional content sections: Products, About, News, Advertisement, Gallery, Testimonials, FAQs, Contact (Form + Google Map).
- Provide clear comments in both HTML and CSS for maintainability and grading transparency.

---

## Deliverables

- `index.html` — semantic HTML5 file with ARIA roles and accessible markup.  
- `style.css` — fully-commented CSS demonstrating Grid, Flexbox, and media queries.  
- `PROJECT_REPORT.md` — (this file) documenting design decisions, testing, and rubric mapping.

> Note: A `README.md` already exists in the repository per your workflow — this file is intentionally named `PROJECT_REPORT.md` so it can be used as the official assignment report requested here.

---

## Design & Layout Approach

### Visual and UX Goals
- Clean, minimal, professional aesthetic that highlights product imagery and copy.
- Two-color scheme ensures visual consistency and meets assignment constraints while providing enough contrast for accessibility.
- Logical content flow: Header → Products → About/News/Ads → Gallery → Testimonials/FAQs → Contact → Footer.

### Grid usage
Grid is used for larger page structure and multi-column sections:

- **Main layout (desktop):** `grid-template-columns: 1fr 3fr;` — Sidebar (offers) + Main products area.
- **About / News / Advertisement:** 3-column grid `grid-template-columns: repeat(3, 1fr)` — collapses responsively.
- **Testimonials + FAQs:** 2-column grid `grid-template-columns: 1fr 1fr`.
- **Contact section:** 2-column grid with contact form and embedded Google Map.

These areas show 2D layout control and alignment across varying content types.

### Flexbox usage
Flexbox is used for:

- **Header navigation:** horizontal, wrapping navigation bar with centered alignment.
- **Product card container:** horizontal wrapping of cards for even spacing and consistent alignment.
- **Testimonial rows / small component alignment** where a one-dimensional layout is sufficient.

This demonstrates the correct tool choice for 1D (Flexbox) vs 2D (Grid) problems.

---

## Responsive Strategy & Breakpoints

Responsive design uses media queries and relative sizing to ensure graceful adaptations:

- **Base (desktop-first)**: flexible Grid and Flexbox layouts using `fr`, `minmax()`, and percent widths so elements scale naturally.
- **Breakpoints used**:
  - `@media (max-width: 992px)` — medium screens / small laptops / tablets: multi-column grids reduce columns (3→2).
  - `@media (max-width: 600px)` — mobile phones: grids collapse to single column; nav becomes vertical.
  - `@media (max-width: 200px)` — tiny devices: font scale-down and compact spacing; tested to ensure content remains readable.
- **Units**: Mostly `rem`, `%`, and `fr`/`minmax()` to prefer relative sizing over fixed pixels.

This covers the assignment requirement of adaptability across devices and demonstrates careful breakpoint planning.

---

## Accessibility & Screen Reader Support

The project includes several accessibility features:

- Semantic HTML5 structure: `<header>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`.
- ARIA roles and labels where helpful (e.g., `role="banner"`, `aria-label` on complex sections).
- All images include descriptive `alt` attributes for screen readers.
- Keyboard focus states: interactive elements are accessible and usable via keyboard (e.g., `tabindex="0"` on product cards for keyboard users).
- Sufficient color contrast: Honey Gold used for accents and backgrounds, Dark Brown for primary text to ensure WCAG AA contrast for content (contrast-tested during design).
- Form fields have associated `<label>` elements and `required` attributes.
- Collapsible FAQs use `<details>`/`<summary>` for native keyboard and screen-reader support.

**Accessibility testing checklist (performed):**
- Tab navigation through all interactive elements.
- Screen reader semantics verified by ensuring logical heading structure and alt text present.
- Use of `details` element for accessible disclosure widgets.

---

## SEO & Performance Considerations

SEO best practices applied:

- `<title>` and `<meta name="description">` tags are included with meaningful content.
- Semantic headings (`h1`, `h2`, `h3`) used in hierarchical order.
- Descriptive `alt` text for images improves image search and accessibility.
- Content includes relevant keywords (organic honey, raw honey, honeycomb, beekeeping) used naturally in headings and body copy.
- Clean URL and file naming (index.html, style.css) for clarity.
- Mobile-first indexing concerns handled by enabling responsive markup, fast rendering with minimal external requests (only images loaded from CDN/Unsplash in demo).
- Page speed tips (for deployment):
  - Optimize and compress images (use responsive `srcset` if deployed).
  - Add `preload` for key assets where beneficial.
  - Serve CSS compressed and minified in production.

These measures help the page be crawlable, indexable, and rank better in search engines.

---

## Features & Content Summary

- **Products** — 3 example product cards with image, title, description, "Add to Cart" button.
- **Sidebar** — special offers and quick conversions.
- **About / News / Advertisement** — 3-column informative area.
- **Gallery** — responsive grid of imagery (auto-fit).
- **Testimonials** — customer quotes styled for credibility.
- **FAQs** — collapsible native `details` for accessibility.
- **Contact** — two-column layout combining a contact form and an embedded Google Map.
- **Footer** — legal and author information.

All features are implemented using only HTML and CSS and include comments to help graders follow the implementation.

---

## How to Run / Preview Locally

1. Clone your repository (if not already):
   ```bash
   git clone <your-repo-url>
   cd <your-repo-folder>
  ```