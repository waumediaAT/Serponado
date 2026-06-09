---
entityId: "review-snippets"
name: "Review Snippets"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Star Ratings in Search"
  - "Rich Snippets Stars"
  - "Aggregate Rating Stars"
sameAs:
  - "https://developers.google.com/search/docs/appearance/structured-data/review-snippet"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: REQUIRES
    target: "structured-data"
    description: "AggregateRating schema is required for review snippets to display"
  - predicate: RELATED_TO
    target: "product-rich-results"
    description: "Product rich results often include review snippet stars"
attributes:
  position: "Inline with the organic result (beneath URL, above description)"
  trigger_intents: [commercial-investigation, transactional]
  ctr_impact: high
  schema_required: "AggregateRating on Product, Recipe, Movie, Book, Software, LocalBusiness, Course, Event"
  owned_by: "Google"
  introduced: "2009"
  display: "Star rating (1–5 scale), numeric score, review count"
  prohibited_uses: "Self-serving reviews on own site (Google spam policies)"
  supported_types:
    - Product
    - Recipe
    - Movie
    - Book
    - Software Application
    - Local Business
    - Course
    - Event
    - CreativeWork
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://developers.google.com/search/docs/appearance/structured-data/review-snippet"
    title: "Review Snippet Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://developers.google.com/search/docs/appearance/structured-data/review"
    title: "Review Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Review Snippets

## Definition

Review Snippets are star rating indicators — typically a 1–5 star visual display, a numeric score, and a review count — displayed beneath the URL in an organic search result. They are powered by `AggregateRating` structured data markup on the page and significantly increase visual prominence and click-through rates.

## Description

Review Snippets are one of the most CTR-impactful rich result types available, because star ratings create immediate visual contrast in a text-dominated SERP. Studies consistently show 15–30% CTR increases for results displaying star ratings versus identical positions without them.

Google supports `AggregateRating` (average of many reviews) and individual `Review` markup for a range of schema types. The most common implementations are on product pages (`Product` schema), recipe pages (`Recipe` schema), and software/application pages (`SoftwareApplication` schema).

Google has strict quality guidelines around review markup to prevent abuse: reviews must be from genuine users, not fabricated or written by the site owner about their own products/services. In 2021, Google tightened its policies on review schema abuse and began actively penalizing sites that misuse `AggregateRating` markup for self-promotional purposes.

## Key Attributes

**Display:** Yellow stars (typically 3.5–5 visible filled), numeric score, parenthetical review count. Example: "★★★★☆ 4.2 (1,847 reviews)"

**Schema Required:** `AggregateRating` with `ratingValue`, `bestRating`, `worstRating`, and `ratingCount` or `reviewCount`. Must be nested within a supported schema type.

**Prohibited:** Using `AggregateRating` on pages where reviews are written by the site for its own offerings. Reviews must come from third-party users.

## Optimization Relevance

Implement `AggregateRating` within the appropriate parent schema type. Ensure review counts are accurate and represent genuine user reviews. For e-commerce, connect review platform data to schema markup. Regularly update the aggregated values as new reviews arrive. Avoid the common mistake of hardcoding static review counts that grow stale.

## Status & Evolution

**Current Status:** Active. Spam policy tightened 2021; FAQ rich results restricted 2023 (unrelated but indicative of Google's direction on reducing misused rich results).

## Evidence & Sources

- [Review Snippet Structured Data](https://developers.google.com/search/docs/appearance/structured-data/review-snippet) — Google Search Central, retrieved 2026-06-09
- [Review Structured Data](https://developers.google.com/search/docs/appearance/structured-data/review) — Google Search Central, retrieved 2026-06-09
