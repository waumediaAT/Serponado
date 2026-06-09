---
entityId: "local-pack"
name: "Local Pack"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Map Pack"
  - "3-Pack"
  - "Local 3-Pack"
  - "Google Local Box"
  - "Local SERP"
sameAs:
  - "https://developers.google.com/search/docs/appearance/local-business"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: TRIGGERED_BY
    target: "local"
    description: "Local intent queries are the primary trigger"
  - predicate: POWERED_BY
    target: "google-business-profile"
    description: "Local Pack listings are sourced from Google Business Profile data"
  - predicate: HAS_SUBTYPE
    target: "local-finder"
    description: "Local Finder is the expanded view of the Local Pack"
  - predicate: RELATED_TO
    target: "local-knowledge-panel"
    description: "Clicking a listing leads to the Local Knowledge Panel"
  - predicate: COMPETES_WITH
    target: "local-service-ads"
    description: "LSAs appear above Local Pack, reducing its prominence for some categories"
attributes:
  position: "Below ads (if present), above organic results for local queries"
  trigger_intents:
    - local
    - transactional
  result_count: 3
  ctr_impact: high
  schema_required: "LocalBusiness (for structured data support)"
  owned_by: "Google"
  introduced: "2007 (7-pack), consolidated to 3-pack August 2015"
  display: "Google Maps embed + 3 business listings with name, rating, address, hours"
  ranking_factors:
    - relevance
    - distance
    - prominence
  mobile_display: true
  desktop_display: true
  expandable: true
  expand_to: "local-finder"
evidence:
  - source: "https://developers.google.com/search/docs/appearance/local-business"
    title: "Local Business Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
  - source: "https://support.google.com/business/answer/7091"
    title: "How your business ranks on Google"
    publisher: "Google Business Profile Help"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
    quote: "Relevance, distance, and prominence are the three main factors."
lastReviewed: "2026-06-09"
---

# Local Pack

## Definition

The Local Pack (also called the Map Pack or 3-Pack) is a SERP feature displaying an embedded Google Maps section with exactly three local business listings in response to location-based queries. It appears above standard organic results and provides business name, rating, address, hours, and click-to-call functionality directly on the SERP.

## Description

The Local Pack is Google's primary interface for local commerce search. When a user's query has local intent — either explicitly ("plumber in Berlin") or implicitly ("coffee shop," "emergency locksmith") — Google triggers the Local Pack above organic results, pulling data from Google Business Profiles (GBP) of relevant nearby businesses.

The three listings shown are selected through Google's local algorithm, which weighs three primary factors: **Relevance** (how well the business category and content matches the query), **Distance** (proximity from the searcher's location or the specified location), and **Prominence** (the business's online and offline reputation — reviews, website authority, citations, press coverage). These three factors are confirmed in Google's official documentation and interact in non-linear ways: a highly prominent business farther away may outrank a closer but less-established competitor.

Each listing in the pack shows: business name, star rating and review count, category label, address, and a "website" and "directions" link. On mobile, "call" appears as a one-tap action. The embedded mini-map visually orients the listings geographically.

Clicking "More places" expands the pack into the **Local Finder** — a full-page view with more than 3 results, filtering options, and a larger map. Clicking a specific listing opens the **Local Knowledge Panel** — the full entity page for that business.

The Local Pack was introduced in 2007 as a 7-result format, progressively reduced and redesigned, consolidated to the current 3-result format in August 2015. This consolidation dramatically reduced the number of businesses visible without clicking through to the Local Finder, intensifying competition for the 3 visible slots.

## Key Attributes

**Position:** Immediately below any ads (Local Service Ads and text ads), above standard organic results. For queries with strong local intent, the Local Pack often appears above the fold.

**Trigger Conditions:** Location-modified queries, "near me" queries, category queries with implicit local intent (restaurant, dentist, gym, hotel), business name queries in a local context.

**Display Elements:** Google Maps mini-embed showing business pins, followed by three business cards showing: name, star rating, review count, category, address, and open/closed status with hours.

**Search Engine Ownership:** Google. The equivalent on Bing is the "Local Pack" powered by Bing Places for Business.

**Device Availability:** Both desktop and mobile. On mobile, the Local Pack is often the first non-ad element users see, with individual listings very prominently displayed.

**Schema Requirement:** `LocalBusiness` schema (or a subtype like `Restaurant`, `MedicalBusiness`, etc.) on the business website supports the Google Business Profile but is not required for Local Pack appearance — GBP data is the primary source.

## Optimization Relevance

Local Pack optimization is primarily Google Business Profile (GBP) optimization. Complete and accurate GBP data — correct category, business hours, address, phone, website, photos — is foundational. Review quantity and quality are the most influential dynamic factor: businesses with more and higher-rated reviews consistently outperform peers in prominence scoring.

Citation consistency (NAP — Name, Address, Phone) across business directories (Yelp, TripAdvisor, industry directories) supports prominence signals. Website content with location-specific pages (`LocalBusiness` schema, embedded Google Maps, location-specific text) reinforces relevance for geo-modified queries.

Distance cannot be optimized by the business, but service area configuration in GBP affects which queries trigger Local Pack appearance for service-area businesses without a physical storefront.

## Relations

- **Google Business Profile** (`POWERED_BY`): GBP is the data source for Local Pack listings — without a GBP, a business cannot appear.
- **Local Finder** (`HAS_SUBTYPE`): The Local Finder is the expanded view accessed via "More places."
- **Local Service Ads** (`COMPETES_WITH`): LSAs appear above the Local Pack for eligible service categories, pushing the pack lower on the page.
- **Local Intent** (`TRIGGERED_BY`): The Local Pack is the primary SERP response to local intent signals.

## Status & Evolution

**Current Status:** Active — core local search feature.

The Local Pack is one of Google's most stable features, having existed since 2007. The 2015 consolidation from 7 to 3 results was the last major structural change. Subsequent updates have focused on additional attributes (COVID hours, vaccination booking, safety attributes) and visual redesigns. AI integration in local search (AI Overviews for local queries) has been limited as of 2026; the Local Pack remains the dominant surface for local commercial queries.

## Evidence & Sources

- [Local Business Structured Data](https://developers.google.com/search/docs/appearance/local-business) — Google Search Central, retrieved 2026-06-09
- [How your business ranks on Google](https://support.google.com/business/answer/7091) — Google Business Profile Help, retrieved 2026-06-09
