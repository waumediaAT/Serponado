---
entityId: "ctr"
name: "Click-Through Rate"
type: Metric
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "CTR"
  - "Organic CTR"
  - "Search CTR"
  - "SERP CTR"
sameAs:
  - "https://support.google.com/searchconsole/answer/9683419"
parent: "serp-metric"
namespace: "metrics"
relations:
  - predicate: MEASURES
    target: "organic-result"
    description: "CTR measures the click performance of a URL in search results"
  - predicate: RELATED_TO
    target: "impressions"
    description: "CTR is derived from clicks divided by impressions"
  - predicate: RELATED_TO
    target: "average-position"
    description: "Position is the strongest predictor of CTR"
  - predicate: AFFECTS
    target: "organic-result"
    description: "CTR may influence ranking via NavBoost engagement signals"
attributes:
  formula: "CTR = (Clicks ÷ Impressions) × 100%"
  source_tool:
    - "Google Search Console (Performance report)"
  unit: "Percentage (%)"
  direction: contextual
  benchmark:
    position_1: "~28–39%"
    position_2: "~15–18%"
    position_3: "~10–12%"
    position_4: "~7–9%"
    position_5: "~5–6%"
    positions_6_to_10: "~2–4%"
    featured_snippet: "highly variable (can be >P1 or <P1)"
  ranking_factor_status: "Disputed — Google denies; leaked documents (2024) suggest NavBoost uses click signals"
  zero_click_impact: "AI Overviews and Featured Snippets reduce CTR for some query types"
evidence:
  - source: "https://support.google.com/searchconsole/answer/9683419"
    title: "Search Console — Clicks and Click-Through Rate"
    publisher: "Google"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://backlinko.com/google-ctr-stats"
    title: "Google Organic CTR Statistics"
    publisher: "Backlinko"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Click-Through Rate (CTR)

## Definition

Click-Through Rate (CTR) is the percentage of impressions that result in a click. In the SERP context, it measures what proportion of users who saw a search result listing actually clicked on it. It is calculated as clicks divided by impressions, expressed as a percentage.

## Description

CTR is one of the most directly actionable metrics in SEO because it can often be improved without changing rankings. Two pages at the same position with significantly different CTRs represent a material traffic gap that is addressable through title tag and meta description optimization.

Position is the dominant predictor of CTR. The relationship is strongly non-linear: Position 1 captures roughly 28–39% of clicks for most queries, Position 2 captures 15–18%, and CTR drops sharply from there. This "position tax" makes the difference between Position 1 and Position 2 the most commercially significant ranking distinction in SEO.

SERP features modify the CTR curve significantly. Featured Snippets at Position 0 can capture CTRs above Position 1 for some queries but below it for others — particularly "zero-click" queries where the snippet answers the question completely. AI Overviews are expected to reduce CTR for all organic positions on covered queries, as the generated answer may satisfy users before they reach organic results.

The relationship between CTR and ranking is contested. Google publicly denies that CTR is a direct ranking signal. However, a 2024 leak of Google's internal API documentation suggested a system called "NavBoost" that incorporates click and engagement data. The academic and industry consensus is that some form of click signal influences rankings, at least in quality evaluation if not in continuous real-time ranking.

CTR is reported at the query, page, and device level in Google Search Console's Performance report.

## Key Attributes

**Formula:** CTR = (Clicks ÷ Impressions) × 100%

**Optimization Levers:** Title tag (most impactful), meta description (secondary), URL structure, rich results (star ratings dramatically improve CTR), Featured Snippet format.

**Zero-Click Trends:** CTR across the SERP has been declining for high-volume informational queries since the expansion of Featured Snippets (2014), AI Overviews (2024), and Knowledge Cards — Google satisfying queries without clicks.

## Status & Evolution

**Current Status:** Active primary performance metric.

## Evidence & Sources

- [Search Console — Clicks and Click-Through Rate](https://support.google.com/searchconsole/answer/9683419) — Google, retrieved 2026-06-09
- [Google Organic CTR Statistics](https://backlinko.com/google-ctr-stats) — Backlinko, retrieved 2026-06-09
