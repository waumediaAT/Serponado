---
entityId: "impressions"
name: "Impressions"
type: Metric
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Search Impressions"
  - "SERP Impressions"
  - "Organic Impressions"
sameAs:
  - "https://support.google.com/searchconsole/answer/9683419"
parent: "serp-metric"
namespace: "metrics"
relations:
  - predicate: RELATED_TO
    target: "ctr"
    description: "CTR is derived from Clicks ÷ Impressions"
  - predicate: RELATED_TO
    target: "average-position"
    description: "Average Position is calculated across all impression-generating queries"
  - predicate: MEASURES
    target: "organic-result"
    description: "Impressions count how many times a URL appeared in search results"
attributes:
  formula: "Count of SERP appearances where the URL could be seen by the user"
  source_tool:
    - "Google Search Console (Performance report)"
  unit: "Count (integer)"
  direction: higher-is-better
  gscs_counting_rule: "Position-dependent — impressions counted only when URL is shown in the visible results area (below-fold results may not count depending on scroll depth)"
  benchmark: null
  zero_click_relevance: "Impressions without clicks indicate zero-click SERP or low CTR — both relevant for optimization"
evidence:
  - source: "https://support.google.com/searchconsole/answer/9683419"
    title: "Search Console — Impressions"
    publisher: "Google"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://developers.google.com/search/blog/2022/07/search-console-performance-report"
    title: "Search Console Performance Report"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Impressions

## Definition

An impression is recorded each time a URL from a website appears in a search result page in response to a query, in a position where the user could potentially see it. Impressions are reported in Google Search Console and represent the raw visibility of a site in Google's search results.

## Description

Impressions are the top-of-funnel metric for organic search visibility. A page can generate millions of impressions with zero clicks — this occurs when a page ranks but users don't click (low CTR), or when SERP features (AI Overviews, Featured Snippets, Knowledge Panels) satisfy the query without a click.

Google Search Console's counting of impressions follows specific rules. For standard organic results, an impression is counted when the URL appears within the visible area of a SERP, regardless of whether the user scrolls to it. For features like carousels, impression counting has specific rules: a video carousel impression requires the video to actually appear in the user's view.

Impression volume is a valuable keyword opportunity signal. A page with high impressions but very low CTR (say, 0.5% at position 8) represents an optimization opportunity: either improving the page to rank higher, or improving the title/description to increase CTR at the current position.

Year-over-year impression trends are a leading indicator of organic visibility — rising impressions before rising traffic indicates a site gaining ranking breadth before depth.

## Key Attributes

**Relationship to CTR:** Impressions are the denominator in CTR — more impressions does not mean more traffic; the CTR rate determines click volume.

**Zero-Click Signal:** High impressions + low CTR for informational queries often indicates a SERP dominated by Featured Snippets or AI Overviews.

## Status & Evolution

**Current Status:** Active primary metric in Google Search Console.

## Evidence & Sources

- [Search Console — Impressions](https://support.google.com/searchconsole/answer/9683419) — Google, retrieved 2026-06-09
- [Search Console Performance Report](https://developers.google.com/search/blog/2022/07/search-console-performance-report) — Google Search Central, retrieved 2026-06-09
