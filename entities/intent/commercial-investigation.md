---
entityId: "commercial-investigation"
name: "Commercial Investigation Intent"
type: Search_Intent
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Commercial Intent"
  - "Research Intent"
  - "Comparison Intent"
  - "Pre-Purchase Research"
sameAs:
  - "https://en.wikipedia.org/wiki/Web_search_query"
parent: "search-intent"
namespace: "intent"
relations:
  - predicate: RELATED_TO
    target: "transactional"
    description: "Commercial investigation precedes transactional in the purchase funnel"
  - predicate: TRIGGERS
    target: "review-snippets"
    description: "Reviews and ratings are primary SERP features for comparison queries"
  - predicate: TRIGGERS
    target: "perspectives"
    description: "Forum/community perspectives often surface for comparison queries"
attributes:
  query_patterns:
    - "best [product/service]"
    - "[product A] vs [product B]"
    - "[product] review"
    - "top [product category]"
    - "[product] alternatives"
    - "[product] pros and cons"
    - "[product] worth it"
    - "is [product] good"
    - "[product] for [use case]"
    - "cheapest [product category]"
    - "[product] comparison"
  serp_features_triggered:
    - review-snippets
    - people-also-ask
    - perspectives
    - shopping-ads
    - text-ads
    - product-rich-results
  content_types:
    - Review articles
    - Comparison guides
    - "Best X for Y" listicles
    - Buyer's guides
    - Roundup posts
    - Vs. articles
  zero_click_risk: low
  conversion_proximity: medium-high
  funnel_stage: "Middle-to-bottom of funnel / Consideration"
  affiliate_seo_relevance: highest
evidence:
  - source: "https://ahrefs.com/blog/search-intent/"
    title: "Search Intent in SEO: What It Is & How to Optimize for It"
    publisher: "Ahrefs"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
  - source: "https://developers.google.com/search/docs/fundamentals/creating-helpful-content"
    title: "Creating Helpful, Reliable, People-First Content"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 0.8
lastReviewed: "2026-06-09"
---

# Commercial Investigation Intent

## Definition

Commercial investigation intent describes queries where the user is researching products, services, or options before making a purchase decision — comparing alternatives, reading reviews, evaluating features and pricing — without being ready to transact immediately.

## Description

Commercial investigation sits at the boundary between informational and transactional intent. The user has an identified purchase need but has not yet chosen a specific product or vendor. They are actively comparing options, seeking third-party validation through reviews, and evaluating fit for their use case.

This is the highest-value intent type for **affiliate SEO** and **content marketing** — "best," "vs," and "review" queries are the primary targets for affiliate review sites, because these are the queries asked by high purchase-intent users who have not yet decided where to buy.

The Helpful Content System has significant implications for commercial investigation content. Google's documentation specifically calls out "affiliate-heavy" content as a potential low-quality signal if it lacks genuine original experience and analysis. Post-Helpful Content, the differentiator between ranking and not ranking for "best [product]" queries is increasingly whether the content demonstrates actual hands-on experience with the reviewed products.

## Key Attributes

**Content Quality Bar:** High and rising — Google increasingly rewards content with genuine first-hand experience (aligns with E-E-A-T "Experience" dimension).

**Affiliate Relevance:** Highest commercial value for affiliate marketing strategies.

**Funnel Stage:** Consideration — these users are close to buying but still gathering evidence.

## Optimization Relevance

Content for commercial investigation queries must demonstrate genuine product knowledge (specific pros/cons based on use, measurements, comparisons). Include real-world test results, photos, video walkthroughs. Use comparison tables. `Product` and `AggregateRating` schema on compared products. First-person language ("I tested," "In my experience") increases E-E-A-T Experience signals.

## Status & Evolution

**Current Status:** Active — quality bar significantly raised by Helpful Content System (2022–2024).

## Evidence & Sources

- [Search Intent in SEO: What It Is & How to Optimize for It](https://ahrefs.com/blog/search-intent/) — Ahrefs, retrieved 2026-06-09
- [Creating Helpful, Reliable, People-First Content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) — Google Search Central, retrieved 2026-06-09
