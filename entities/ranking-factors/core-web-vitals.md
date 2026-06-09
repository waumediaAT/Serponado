---
entityId: "core-web-vitals"
name: "Core Web Vitals"
type: Ranking_Factor
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "CWV"
  - "Web Vitals"
  - "Page Experience Signals"
sameAs:
  - "https://web.dev/vitals/"
  - "https://developers.google.com/search/docs/appearance/core-web-vitals"
parent: "ranking-factor"
namespace: "ranking-factors"
relations:
  - predicate: CONTAINS
    target: "lcp"
    description: "LCP is the loading performance metric"
  - predicate: CONTAINS
    target: "inp"
    description: "INP is the interactivity metric (replaced FID March 2024)"
  - predicate: CONTAINS
    target: "cls"
    description: "CLS is the visual stability metric"
  - predicate: AFFECTS
    target: "organic-result"
    description: "CWV pass/fail status is a page experience ranking signal"
  - predicate: RELATED_TO
    target: "mobile-first-indexing"
    description: "CWV is measured from Chrome User Experience data, primarily mobile"
attributes:
  factor_type: technical
  weight: medium
  confirmed_by:
    - "Google Page Experience Update announcement (2021)"
    - "Google Search Central Core Web Vitals documentation"
  ranking_status: "Confirmed ranking factor since June 2021 (Page Experience Update)"
  metrics:
    - id: lcp
      name: "Largest Contentful Paint"
      target: "< 2.5 seconds"
      measures: "Loading performance"
    - id: inp
      name: "Interaction to Next Paint"
      target: "< 200 milliseconds"
      measures: "Interactivity"
      replaced: fid
      replaced_date: "March 2024"
    - id: cls
      name: "Cumulative Layout Shift"
      target: "< 0.1"
      measures: "Visual stability"
  data_source: "Chrome User Experience Report (CrUX) — real user field data"
  lab_data_tool: "PageSpeed Insights, Lighthouse"
  field_data_tool: "Chrome UX Report, Google Search Console CWV report"
  affects_feature:
    - organic-result
    - top-stories
evidence:
  - source: "https://web.dev/vitals/"
    title: "Web Vitals"
    publisher: "web.dev (Google)"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://developers.google.com/search/docs/appearance/core-web-vitals"
    title: "Core Web Vitals"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
lastReviewed: "2026-06-09"
---

# Core Web Vitals

## Definition

Core Web Vitals (CWV) are a set of three specific user experience metrics defined by Google that measure the loading performance, interactivity, and visual stability of a web page. They became an official Google ranking factor in June 2021 via the Page Experience Update and are measured from real-user Chrome browser data.

## Description

Core Web Vitals operationalize Google's commitment to rewarding fast, stable, and interactive web experiences. Unlike many ranking factors that are abstract or hard to measure directly, CWV are precise, objectively measurable metrics with defined "Good," "Needs Improvement," and "Poor" thresholds.

**LCP (Largest Contentful Paint)** measures loading performance — specifically, how long it takes for the largest visible content element on the page (usually a hero image, video thumbnail, or large text block) to finish loading and rendering. The threshold for "Good" is under 2.5 seconds. LCP optimization focuses on server response time, render-blocking resources, resource load efficiency, and element render time.

**INP (Interaction to Next Paint)** measures interactivity — the latency between user input (click, tap, keypress) and the browser's visual response across all interactions during the page's lifetime. It replaced FID (First Input Delay) in March 2024. FID only measured the first interaction; INP measures all interactions, providing a more comprehensive picture of responsiveness. The threshold for "Good" is under 200 milliseconds.

**CLS (Cumulative Layout Shift)** measures visual stability — how much visible content unexpectedly shifts during page load. CLS is scored as a unitless ratio; the "Good" threshold is under 0.1. Common causes include images without declared dimensions, late-loading ads injecting content above existing elements, and web fonts causing content reflow.

CWV scores are based on **field data** from the Chrome User Experience Report (CrUX) — actual measurements from real users' Chrome browsers over a 28-day rolling window. This is a crucial distinction: lab data from tools like Lighthouse reflects simulated performance; CrUX data reflects actual user experience. Google uses CrUX data for ranking signals.

## Key Attributes

**Measurement Source:** Chrome User Experience Report (CrUX) — 28-day rolling real-user data. Requires sufficient traffic to generate field data.

**Tools:** Google Search Console CWV Report (field data), PageSpeed Insights (both lab and field), Chrome DevTools Lighthouse (lab only), web.dev/measure (lab).

**Pass/Fail:** Each metric has a binary Good/Needs Improvement/Poor classification. Page Experience ranking signal requires passing all three metrics (Good status) at the page level.

## Optimization Relevance

LCP optimization: preload the LCP resource, use a CDN, optimize the LCP image (WebP/AVIF, appropriate sizing, no lazy-load on LCP element), eliminate render-blocking CSS/JS above the fold, minimize server response time (TTFB).

INP optimization: identify long JavaScript tasks with Chrome DevTools, minimize main thread blocking, use `scheduler.yield()` for long tasks, defer non-critical JS, optimize event handlers.

CLS optimization: always declare `width` and `height` on `<img>` and `<video>` elements, use CSS `aspect-ratio`, avoid inserting content above existing content, use CSS transforms instead of properties that trigger layout for animations, preload web fonts.

## Status & Evolution

**Current Status:** Active — confirmed ranking factor. March 2024 update: INP replaced FID as the interactivity metric.

## Evidence & Sources

- [Web Vitals](https://web.dev/vitals/) — web.dev (Google), retrieved 2026-06-09
- [Core Web Vitals](https://developers.google.com/search/docs/appearance/core-web-vitals) — Google Search Central, retrieved 2026-06-09
