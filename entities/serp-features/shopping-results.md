---
entityId: "shopping-results"
name: "Shopping Results (Merchant Listings)"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Free Shopping Listings"
  - "Merchant Listings"
  - "Organic Shopping"
  - "Free Product Listings"
  - "Google Shopping Organic"
sameAs:
  - "https://support.google.com/merchants/answer/9838672"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: RELATED_TO
    target: "shopping-ads"
    description: "Shopping Ads are the paid counterpart to free merchant listings"
  - predicate: REQUIRES
    target: "structured-data"
    description: "Product schema and Google Merchant Center feed required"
  - predicate: TRIGGERED_BY
    target: "transactional"
    description: "Product and commercial queries trigger shopping results"
attributes:
  position: "Shopping tab (primary); sometimes main SERP"
  trigger_intents: [transactional, commercial-investigation]
  ctr_impact: high
  schema_required: "Product schema + Google Merchant Center feed"
  owned_by: "Google"
  introduced: "2020"
  display: "Product image, title, price, merchant name, ratings, shipping"
  requirement: "Google Merchant Center account with approved product feed"
  free: true
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://support.google.com/merchants/answer/9838672"
    title: "Free Product Listings on Google"
    publisher: "Google Merchant Center Help"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://support.google.com/merchants/answer/9538352"
    title: "About free listings on Google"
    publisher: "Google Merchant Center Help"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
lastReviewed: "2026-06-09"
---

# Shopping Results (Merchant Listings)

## Definition

Shopping Results (Free Merchant Listings) are organic product listings appearing in Google's Shopping tab and sometimes the main SERP, showing product images, titles, prices, merchant names, and ratings. Introduced in 2020 when Google opened Shopping to free listings, they allow e-commerce merchants to appear in Google Shopping without paid advertising.

## Description

Prior to April 2020, Google Shopping was entirely pay-to-play — all listings required a Google Shopping (now Performance Max) advertising campaign. When Google opened Shopping to free listings in April 2020, it transformed Shopping into a hybrid of paid and organic results, similar to the main SERP.

Free merchant listings are powered by **Google Merchant Center** product feeds — structured product data submitted by merchants containing title, description, price, availability, image URL, product URL, and category. The quality and completeness of the feed directly affects listing visibility, as Google uses feed data to match products to user queries.

Free listings appear primarily in the Google Shopping tab and secondarily in the main SERP for product queries. In the Shopping tab, they are intermixed with paid Shopping Ads — the distinction is subtle (paid listings show "Sponsored" labels).

Feed optimization (title structure, category accuracy, high-quality images, accurate pricing, fast inventory updates) is the primary lever for free listing performance. `Product` schema markup on product pages supports the connection between the Merchant Center feed and the website.

## Key Attributes

**Requirement:** Google Merchant Center account with approved product feed. No advertising budget required.

**Position:** Shopping tab (primary), main SERP Shopping carousel (secondary, mixed with paid ads).

**Feed Quality Signals:** Title relevance to target queries, complete attribute coverage, accurate pricing and availability, high-resolution images, positive seller ratings.

## Status & Evolution

**Current Status:** Active — introduced April 2020 as Google's response to Amazon's free listings.

## Evidence & Sources

- [Free Product Listings on Google](https://support.google.com/merchants/answer/9838672) — Google Merchant Center Help, retrieved 2026-06-09
- [About free listings on Google](https://support.google.com/merchants/answer/9538352) — Google Merchant Center Help, retrieved 2026-06-09
