---
entityId: "local"
name: "Local Intent"
type: Search_Intent
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Local Search Intent"
  - "Geographic Intent"
  - "Near Me Intent"
  - "Location-Based Intent"
sameAs:
  - "https://developers.google.com/search/docs/appearance/local-business"
parent: "search-intent"
namespace: "intent"
relations:
  - predicate: TRIGGERS
    target: "local-pack"
    description: "Local intent is the primary trigger for the Local Pack"
  - predicate: TRIGGERS
    target: "local-service-ads"
    description: "Local Service Ads appear above the Local Pack for eligible categories"
  - predicate: RELATED_TO
    target: "transactional"
    description: "Local intent often co-occurs with transactional intent for service bookings"
attributes:
  query_patterns:
    - "[service/product] near me"
    - "[service] in [city/neighborhood]"
    - "[business type] [location]"
    - "open now [business type]"
    - "[business name]" (with user location context)
    - "emergency [service]"
    - "[service] [zip code]"
  serp_features_triggered:
    - local-pack
    - local-finder
    - local-knowledge-panel
    - local-service-ads
    - google-business-profile
  content_types:
    - Google Business Profile
    - Local landing pages
    - Location pages
    - NAP citations
  zero_click_risk: medium
  conversion_proximity: high
  funnel_stage: "Bottom of funnel — high intent, local context"
  mobile_prevalence: very_high
evidence:
  - source: "https://developers.google.com/search/docs/appearance/local-business"
    title: "Local Business Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://support.google.com/business/answer/7091"
    title: "How your business ranks on Google"
    publisher: "Google Business Profile Help"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
lastReviewed: "2026-06-09"
---

# Local Intent

## Definition

Local intent describes queries where the user is seeking products, services, businesses, or information within a specific geographic area — either explicitly ("plumber Berlin") or implicitly through near-me context signals ("coffee shop," "emergency dentist").

## Description

Local intent is a modifying layer that can apply to informational, transactional, or navigational queries — the geographic dimension transforms the SERP response from organic-first to Local Pack-first. Google uses multiple signals to detect local intent: explicit location words, "near me" phrasing, device GPS location, IP-based location, and query category classification (categories like restaurants, medical services, home services have high baseline local intent).

Google estimates that approximately 46% of all searches have local intent. The prevalence is even higher on mobile, where immediate, physical-proximity needs are most common.

The Local Pack is the SERP's primary response to local intent, providing three business listings with geographically relevant results. Google's local ranking algorithm (Relevance, Distance, Prominence) ensures the most appropriate, proximate, and reputable businesses appear.

For local businesses, capturing local intent is the highest-ROI SEO activity: local pack clicks convert at high rates because the user's geographic readiness to visit or purchase is high.

## Key Attributes

**Mobile Prevalence:** Very high — local intent is disproportionately expressed on mobile devices by users with immediate physical needs.

**Implicit vs. Explicit:** Many queries have implicit local intent (Google infers location relevance) without containing location words. "Pizza delivery" doesn't need "near me" for Google to show local results.

**Conversion Rate:** High — users with local intent who find a relevant business commonly visit or call.

## Status & Evolution

**Current Status:** Active.

## Evidence & Sources

- [Local Business Structured Data](https://developers.google.com/search/docs/appearance/local-business) — Google Search Central, retrieved 2026-06-09
- [How your business ranks on Google](https://support.google.com/business/answer/7091) — Google Business Profile Help, retrieved 2026-06-09
