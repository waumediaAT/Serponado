---
entityId: "informational"
name: "Informational Intent"
type: Search_Intent
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Know Query"
  - "Know Simple Query"
  - "Research Intent"
  - "Informational Query"
sameAs:
  - "https://en.wikipedia.org/wiki/Web_search_query"
parent: "search-intent"
namespace: "intent"
relations:
  - predicate: TRIGGERS
    target: "featured-snippet"
    description: "Featured Snippets are the primary SERP feature for informational queries"
  - predicate: TRIGGERS
    target: "people-also-ask"
    description: "PAA is ubiquitous on informational queries"
  - predicate: TRIGGERS
    target: "knowledge-panel"
    description: "Entity-based informational queries often generate Knowledge Panels"
  - predicate: TRIGGERS
    target: "ai-overview"
    description: "AI Overviews predominantly target informational queries"
attributes:
  query_patterns:
    - "how to [action]"
    - "what is [term]"
    - "why does [phenomenon]"
    - "who is [person]"
    - "when did [event]"
    - "how does [process] work"
    - "define [term]"
    - "[term] meaning"
    - "[term] explained"
    - "history of [topic]"
  serp_features_triggered:
    - featured-snippet
    - people-also-ask
    - knowledge-panel
    - ai-overview
    - image-pack
    - video-carousel
    - knowledge-card
  content_types:
    - Articles
    - Guides
    - Tutorials
    - Explainers
    - FAQs
    - Encyclopedia entries
    - Wiki-style pages
  zero_click_risk: high
  conversion_proximity: low
  funnel_stage: "Top of funnel / Awareness"
evidence:
  - source: "https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf"
    title: "Search Quality Evaluator Guidelines"
    publisher: "Google"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://moz.com/blog/search-intent-seo"
    title: "Search Intent: The Overlooked SEO Factor"
    publisher: "Moz"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Informational Intent

## Definition

Informational intent describes queries where the user's primary goal is to learn something — to acquire knowledge, understand a concept, answer a question, or research a topic — without an immediate intent to navigate to a specific site or complete a transaction.

## Description

Informational intent is the most common query type by volume, encompassing everything from simple factual lookups ("capital of France") to complex research topics ("long-term effects of sleep deprivation on cognitive function"). The unifying characteristic is that the user wants information, not a specific website or a product.

Google's Search Quality Evaluator Guidelines classify informational queries as "Know" queries (seeking information) and "Know Simple" queries (seeking a single, definitive fact). This distinction matters for SERP construction: "Know Simple" queries (what's the boiling point of water?) trigger Knowledge Cards and Featured Snippets with high confidence; "Know" queries (understanding the causes of WWI) trigger richer, more multi-source SERP layouts.

Informational SERPs are the richest in terms of feature density: Featured Snippets, People Also Ask boxes, Knowledge Panels, Image Packs, Video Carousels, and AI Overviews all predominantly appear for informational queries. This feature density reflects Google's attempt to satisfy the query directly on the SERP — which creates the highest zero-click rate of any intent type.

For content strategy, informational intent represents the **awareness and consideration stages** of the marketing funnel. Content targeting informational queries builds brand authority and topical expertise, drives organic traffic, and seeds top-of-funnel audiences for downstream commercial conversion.

## Key Attributes

**SERP Feature Density:** Highest of all intent types.

**Zero-Click Risk:** High — AI Overviews, Featured Snippets, Knowledge Cards can answer the query without a click.

**Conversion Proximity:** Low — users at the information-gathering stage are not typically ready to purchase.

**Content Match:** Long-form explanatory content, FAQ structures, tutorials, how-to guides.

## Optimization Relevance

Content targeting informational intent should directly answer the target question (enabling Featured Snippet and PAA capture), use question-phrase headings, provide comprehensive coverage of related subtopics (topical authority), and include supporting media (images, diagrams, video) for visual queries. Structured data (FAQ, HowTo, Article) increases rich result eligibility.

## Status & Evolution

**Current Status:** Active — oldest and most stable intent classification.

## Evidence & Sources

- [Search Quality Evaluator Guidelines](https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf) — Google, retrieved 2026-06-09
- [Search Intent: The Overlooked SEO Factor](https://moz.com/blog/search-intent-seo) — Moz, retrieved 2026-06-09
