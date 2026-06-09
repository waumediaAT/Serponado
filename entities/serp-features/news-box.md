---
entityId: "news-box"
name: "News Box / Top Stories"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Top Stories"
  - "Google News Box"
  - "News Carousel"
  - "In The News"
sameAs:
  - "https://developers.google.com/search/docs/appearance/structured-data/article"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: TRIGGERED_BY
    target: "seasonal"
    description: "News intent and time-sensitive queries are primary triggers"
  - predicate: REQUIRES
    target: "structured-data"
    description: "NewsArticle or Article schema strongly improves eligibility"
  - predicate: RELATED_TO
    target: "content-freshness"
    description: "Recency is the dominant ranking factor for Top Stories"
attributes:
  position: "Top of SERP — often above organic results for news queries"
  trigger_intents: [news, seasonal, informational]
  ctr_impact: high
  schema_required: "NewsArticle or Article"
  owned_by: "Google"
  introduced: "2002 (Google News), main SERP integration ~2012"
  amp_required_formerly: true
  amp_required_now: false
  display: "Carousel of 3–5 news articles with headline, source, image, and time elapsed"
  freshness_weight: "Extremely high — recency is dominant signal"
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://developers.google.com/search/docs/appearance/structured-data/article"
    title: "Article Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://developers.google.com/search/docs/crawling-indexing/news/news-features"
    title: "Google News Features"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
lastReviewed: "2026-06-09"
---

# News Box / Top Stories

## Definition

The News Box (also called Top Stories) is a SERP feature displaying a carousel of recent news articles at the top of the SERP for timely, news-relevant queries. It aggregates content from Google News-indexed publishers and shows headlines, source names, images, and publication timestamps.

## Description

The Top Stories carousel is Google's integration of its news index into the main SERP. When a query has news-relevant signals — breaking events, recent announcements, named individuals or organizations with recent coverage, trending topics — Google triggers the Top Stories box above or near the top of organic results.

The key differentiating factor for Top Stories is **freshness**. Unlike standard organic results where freshness is one signal among many, Top Stories ranking is dominated by recency — articles published within the last few hours to days significantly outperform older content for the same topic. Content from yesterday competes poorly with content from this morning.

AMP (Accelerated Mobile Pages) was previously required for mobile Top Stories inclusion. Google removed this requirement in June 2021 when the Page Experience update launched, meaning any fast-loading mobile page can now appear in Top Stories. `NewsArticle` or `Article` structured data remains strongly recommended for eligibility and accurate display.

Publishers must be indexed by Google News (either through automatic discovery or by submitting a news sitemap) to consistently appear in Top Stories.

## Key Attributes

**Schema Requirement:** `NewsArticle` with `headline`, `image`, `datePublished`, `dateModified`, `author`, and `publisher`. `Article` also accepted.

**Freshness Signal:** Dominant. Articles should be published promptly, accurately dated with `datePublished` and `dateModified`, and have timestamps visible in the HTML.

**AMP:** No longer required (since June 2021). Still beneficial for performance.

## Optimization Relevance

Core requirements: fast mobile page speed (replacing AMP requirement), `NewsArticle` schema, Google News indexing (news sitemap), clear bylines and publisher information, accurate publication timestamps. Editorial quality and factual accuracy affect long-term publisher standing in Google's news ranking.

## Status & Evolution

**Current Status:** Active. AMP requirement removed 2021 was the most significant recent change.

## Evidence & Sources

- [Article Structured Data](https://developers.google.com/search/docs/appearance/structured-data/article) — Google Search Central, retrieved 2026-06-09
- [Google News Features](https://developers.google.com/search/docs/crawling-indexing/news/news-features) — Google Search Central, retrieved 2026-06-09
