---
entityId: "transactional"
name: "Transactional Intent"
type: Search_Intent
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Do Query"
  - "Buy Intent"
  - "Purchase Intent"
  - "Action Intent"
sameAs:
  - "https://en.wikipedia.org/wiki/Web_search_query"
parent: "search-intent"
namespace: "intent"
relations:
  - predicate: TRIGGERS
    target: "shopping-ads"
    description: "Shopping Ads are the primary paid feature for transactional queries"
  - predicate: TRIGGERS
    target: "product-rich-results"
    description: "Product rich results appear for transactional queries with schema"
  - predicate: RELATED_TO
    target: "commercial-investigation"
    description: "Commercial investigation queries precede transactional queries in the purchase funnel"
attributes:
  query_patterns:
    - "buy [product]"
    - "order [product]"
    - "[product] price"
    - "[product] deal"
    - "[product] discount"
    - "download [software]"
    - "subscribe to [service]"
    - "[service] sign up"
    - "[product] near me"
    - "cheap [product]"
    - "[product] free shipping"
  serp_features_triggered:
    - shopping-ads
    - text-ads
    - product-rich-results
    - local-pack
    - merchant-listings
  content_types:
    - Product pages
    - Category pages
    - Checkout/conversion pages
    - Landing pages
    - Pricing pages
  zero_click_risk: low
  conversion_proximity: high
  funnel_stage: "Bottom of funnel / Decision"
  paid_search_competition: highest
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
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Transactional Intent

## Definition

Transactional intent (also called "Do" queries in Google's framework) describes queries where the user intends to complete an action — typically a purchase, download, subscription, booking, or registration — and is actively ready to convert.

## Description

Transactional queries represent the highest commercial value tier in search, corresponding to the bottom-of-funnel decision stage where users have already decided what they want and are ready to take action. The explicit action words ("buy," "order," "download," "book") and price/deal/availability modifiers are the clearest signals.

Google's SERP for transactional queries is the most commercially dense: Shopping Ads appear at the top (often spanning the full width on mobile), followed by text ads, and then organic results which may include Product Rich Results, Local Pack (for local availability), and Merchant Listings (free Shopping listings).

The high commercial value of transactional keywords is reflected in the highest CPCs in Google Ads auctions — competitive product categories routinely command $5–50+ per click. Organic positions for transactional keywords are correspondingly competitive, dominated by major e-commerce platforms (Amazon, eBay, large retailers) that have both domain authority and optimized product pages.

For organic SEO, transactional intent content means product pages optimized with `Product` schema (price, availability, ratings), clear purchase CTAs, fast-loading with good Core Web Vitals, mobile-optimized checkout experience, and trust signals (reviews, security badges, return policies visible).

## Key Attributes

**Commercial Value:** Highest of all intent types — directly linked to purchase conversion.

**SERP Layout:** Most ad-heavy — Shopping Ads typically dominate above the fold for product transactional queries.

**Content Match:** Product pages, category pages, pricing pages — NOT informational articles.

## Optimization Relevance

For e-commerce: `Product` schema with price, availability, and `AggregateRating`. Clear product titles matching query phrasing. Fast page speed (high conversion-value pages have highest performance ROI). Trust signals visible above the fold. For Google Shopping organic (Merchant Listings): complete and accurate Google Merchant Center product feed with competitive pricing and high ratings.

## Status & Evolution

**Current Status:** Active.

## Evidence & Sources

- [Search Quality Evaluator Guidelines](https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf) — Google, retrieved 2026-06-09
- [Search Intent in SEO: What It Is & How to Optimize for It](https://ahrefs.com/blog/search-intent/) — Ahrefs, retrieved 2026-06-09
