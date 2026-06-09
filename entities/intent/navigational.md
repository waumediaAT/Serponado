---
entityId: "navigational"
name: "Navigational Intent"
type: Search_Intent
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Go Query"
  - "Brand Query"
  - "Navigation Query"
  - "Direct Navigation"
sameAs:
  - "https://en.wikipedia.org/wiki/Web_search_query"
parent: "search-intent"
namespace: "intent"
relations:
  - predicate: TRIGGERS
    target: "sitelinks"
    description: "Sitelinks are the primary feature triggered by branded/navigational queries"
  - predicate: TRIGGERS
    target: "knowledge-panel"
    description: "Entity-recognized brands trigger Knowledge Panels on navigational queries"
attributes:
  query_patterns:
    - "[brand name]"
    - "[website name]"
    - "[brand] login"
    - "[brand] sign in"
    - "[brand] contact"
    - "[brand].com"
    - "[person] official site"
    - "[brand] account"
  serp_features_triggered:
    - sitelinks
    - knowledge-panel
    - sitelinks-searchbox
    - local-knowledge-panel
  content_types:
    - Brand homepage
    - Login pages
    - Contact pages
    - About pages
  zero_click_risk: low
  conversion_proximity: medium
  funnel_stage: "All funnel stages — existing customer or aware user"
  seo_implications: "Cannot be won by competitors — Google surfaces the brand destination"
evidence:
  - source: "https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf"
    title: "Search Quality Evaluator Guidelines"
    publisher: "Google"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://ahrefs.com/blog/search-intent/"
    title: "Search Intent in SEO: What It Is & How to Optimize for It"
    publisher: "Ahrefs"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Navigational Intent

## Definition

Navigational intent (also called "Go" queries) describes queries where the user wants to reach a specific website, page, or online destination they already know exists. The search engine is being used as a navigation shortcut rather than a discovery tool.

## Description

Navigational queries have the clearest and most definitive correct answer: the specific website the user intends to visit. When a user types "Gmail," "Amazon," or "New York Times," they are not seeking alternatives — they want to reach that specific destination. Google recognizes this intent and surfaces the intended brand's result prominently, typically with Sitelinks.

The SEO implication is that navigational queries are essentially unwinnable by non-target brands — Google's quality systems are specifically designed to ensure users who search for "[Brand]" reach "[Brand]." Branded navigational queries are also the most reliable indicator of brand awareness and intent: users who search brand names are typically existing customers, highly engaged prospects, or people looking to contact/engage the brand.

For brand owners, navigational queries are about protecting and enhancing the branded SERP rather than competing for it. This means claiming the Knowledge Panel, ensuring Sitelinks reflect the most valuable pages, maintaining a Sitelinks Searchbox via `WebSite` schema, and monitoring the branded SERP for reputation issues (negative reviews, competitor ads on brand keywords).

## Key Attributes

**User Mindset:** The destination is already decided — the user is in execution mode, not discovery mode.

**Competitive SEO Value:** Zero — Google will always surface the intended brand for its own branded queries.

**Brand SEO Value:** High — the branded SERP is a trust and conversion asset to be optimized.

## Status & Evolution

**Current Status:** Active.

## Evidence & Sources

- [Search Quality Evaluator Guidelines](https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf) — Google, retrieved 2026-06-09
- [Search Intent in SEO: What It Is & How to Optimize for It](https://ahrefs.com/blog/search-intent/) — Ahrefs, retrieved 2026-06-09
