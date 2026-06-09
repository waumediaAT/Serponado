---
entityId: "perspectives"
name: "Perspectives / Forum Results"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Perspectives"
  - "Forum Results"
  - "Reddit Results"
  - "Discussion Results"
  - "Perspectives Filter"
sameAs:
  - "https://blog.google/products/search/google-search-perspectives/"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: TRIGGERED_BY
    target: "commercial-investigation"
    description: "Recommendation and review queries frequently trigger Perspectives"
  - predicate: RELATED_TO
    target: "e-e-a-t"
    description: "Perspectives was introduced in response to E-E-A-T's Experience dimension emphasis"
  - predicate: RELATED_TO
    target: "helpful-content"
    description: "Helpful Content System emphasized first-hand experience, which Perspectives surfaces"
attributes:
  position: "Variable — often mid-SERP for experience/recommendation queries"
  trigger_intents: [commercial-investigation, informational]
  ctr_impact: medium
  schema_required: null
  owned_by: "Google"
  introduced: "2023"
  source_types:
    - Reddit
    - Quora
    - Stack Exchange
    - TikTok
    - YouTube
    - Personal blogs
    - Online forums
    - Social media platforms
  display: "Carousel of forum/discussion thread excerpts with source, author, engagement metrics"
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://blog.google/products/search/google-search-perspectives/"
    title: "Google Search will now show more perspectives from real people"
    publisher: "Google Blog"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://searchengineland.com/google-perspectives-search-feature-394756"
    title: "Google Perspectives: Everything You Need to Know"
    publisher: "Search Engine Land"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Perspectives / Forum Results

## Definition

Perspectives (also called Forum Results) is a SERP feature introduced in 2023 that surfaces first-person experience content from forums, social media, and community platforms — Reddit, Quora, Stack Exchange, TikTok, personal blogs — for queries seeking real-world advice, recommendations, and authentic human experience.

## Description

Perspectives represents Google's response to a documented user behavior: for product recommendations, lifestyle advice, and experience-based queries, users had been appending "reddit" or "forum" to their Google queries to bypass algorithmically optimized content and reach authentic community discussions.

The feature was introduced alongside the broader "Perspectives" filter tab in Google Search, which allows users to explicitly filter results to show only first-person content. In the standard SERP, Perspectives content appears as a mid-page carousel showing discussion thread excerpts with source attribution, author handle, post date, and engagement metrics.

Reddit's elevated presence in Google SERPs became notable in 2023–2024, driven partly by Perspectives and partly by a broader algorithmic reweighting of community content following the Helpful Content Update's emphasis on first-hand experience as an E-E-A-T signal. Google's 2024 licensing deal with Reddit for AI training data coincided with Reddit's high SERP visibility (though the causal relationship is disputed).

For content creators, Perspectives represents an opportunity: participating genuinely in relevant forums and communities, with authentic answers on relevant platforms, can earn SERP visibility through the Perspectives surface without traditional SEO optimization.

## Key Attributes

**Source Types:** Forum threads, social posts, blog posts with first-person perspective, video content.

**E-E-A-T Connection:** Directly tied to the "Experience" dimension — content from people with first-hand experience answering from their own perspective.

**Optimization:** Cannot be "gamed" in the traditional sense — requires genuine community participation and authentic content.

## Status & Evolution

**Current Status:** Active and expanding.

Perspectives expanded from beta in 2023 to wider deployment. The integration of Reddit as a primary source (often appearing in the main SERP as well as Perspectives) was a notable development. Ongoing expansion of source types and increased prominence are expected as Google emphasizes authentic human experience.

## Evidence & Sources

- [Google Search will now show more perspectives from real people](https://blog.google/products/search/google-search-perspectives/) — Google Blog, retrieved 2026-06-09
- [Google Perspectives: Everything You Need to Know](https://searchengineland.com/google-perspectives-search-feature-394756) — Search Engine Land, retrieved 2026-06-09
