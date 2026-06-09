---
entityId: "text-ads"
name: "Text Ads (Responsive Search Ads)"
type: Paid_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "RSA"
  - "Responsive Search Ads"
  - "Google Text Ads"
  - "Google Ads Search"
  - "Expanded Text Ads"
  - "PPC Ads"
sameAs:
  - "https://support.google.com/google-ads/answer/7684791"
parent: "paid-feature"
namespace: "paid-features"
relations:
  - predicate: IS_TYPE_OF
    target: "paid-feature"
    description: "Text Ads are a type of paid SERP feature"
  - predicate: COMPETES_WITH
    target: "shopping-ads"
    description: "Both appear in paid positions above organic results for commercial queries"
  - predicate: RELATED_TO
    target: "transactional"
    description: "Text Ads are primarily triggered by transactional and commercial investigation queries"
attributes:
  position: "Top of SERP (up to 4 ads), Bottom of SERP (up to 3 ads)"
  trigger_intents:
    - transactional
    - commercial-investigation
    - navigational
  billing_model: "CPC — Cost Per Click"
  auction_mechanism: "Ad Rank = Quality Score × Bid"
  quality_score_components:
    - Expected CTR
    - Ad Relevance
    - Landing Page Experience
  format:
    headlines: "Up to 15 (3 shown at once)"
    descriptions: "Up to 4 (2 shown at once)"
    display_url: "2 path fields"
  assets:
    - Sitelinks
    - Callouts
    - Structured Snippets
    - Call
    - Location
    - Price
    - Promotion
    - Image
    - Lead Form
  owned_by: "Google Ads"
  introduced: "1999 (AdWords text ads), RSA format 2018"
  eta_sunset: "June 2022 (Expanded Text Ads retired, RSAs became standard)"
  label: "'Sponsored' or 'Ad' label visible"
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://support.google.com/google-ads/answer/7684791"
    title: "Responsive Search Ads"
    publisher: "Google Ads Help"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://support.google.com/google-ads/answer/6154577"
    title: "About Ad Rank"
    publisher: "Google Ads Help"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
lastReviewed: "2026-06-09"
---

# Text Ads (Responsive Search Ads)

## Definition

Text Ads (Responsive Search Ads / RSAs) are the standard Google Ads format for search — text-based advertisements appearing at the top and bottom of the SERP, labeled "Sponsored," dynamically assembled by Google from a pool of provided headlines and descriptions to maximize relevance and expected performance for each individual auction.

## Description

Text Ads are the foundation of Google's advertising business and the original form of paid search. The modern Responsive Search Ad format replaced Expanded Text Ads (ETAs) as the standard in 2022. Where ETAs had fixed headline/description combinations, RSAs provide up to 15 headlines and 4 descriptions that Google automatically combines and tests to find the highest-performing combinations for different users and queries.

Ad Rank determines ad position and cost. Ad Rank = Quality Score × Maximum CPC Bid. Quality Score (1–10) is Google's estimate of ad relevance, landing page quality, and expected CTR. Higher Quality Score means lower effective CPC and better positions — the incentive structure rewards relevance over raw bidding.

Ads appear with a "Sponsored" label (changed from "Ad" in early 2023 in some markets). The top of SERP can show up to 4 ads for competitive queries; the bottom can show up to 3. On mobile, ads are indistinguishable from organic results in layout, differing only by the "Sponsored" label.

Assets (formerly Extensions) augment text ads with additional information: Sitelink assets add 4–6 navigation links; Callout assets add short USP phrases; Structured Snippet assets list product/service categories; Location assets show the business address; Call assets add phone numbers for direct calling; Price assets display service/product pricing directly in the ad.

## Key Attributes

**Billing:** CPC (Cost Per Click) — charged only when a user clicks the ad.

**Ad Label:** "Sponsored" — displayed above the headline, identifying the result as paid.

**Auction:** Real-time auction for each search — position determined by Ad Rank (Quality Score × Bid), not bid alone.

## Optimization Relevance

RSA optimization focuses on: providing high-quality, diverse headline and description variants (covering different USPs, features, CTAs), maximizing Asset coverage (all asset types with complete information), landing page relevance to target keywords (affects Quality Score), and bid strategy selection aligned to campaign goals (Maximize Conversions, Target CPA, Target ROAS).

## Status & Evolution

**Current Status:** Active. RSA is the sole standard text ad format (ETA retired June 2022).

Performance Max campaigns (fully automated, multi-channel) have taken an increasing share of Google Ads budget, but RSA campaigns remain the primary choice for search-specific keyword targeting.

## Evidence & Sources

- [Responsive Search Ads](https://support.google.com/google-ads/answer/7684791) — Google Ads Help, retrieved 2026-06-09
- [About Ad Rank](https://support.google.com/google-ads/answer/6154577) — Google Ads Help, retrieved 2026-06-09
