---
entityId: "visibility-index"
name: "Visibility Index"
type: Metric
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "SEO Visibility"
  - "SISTRIX Visibility Index"
  - "Organic Visibility Score"
  - "Search Visibility"
sameAs:
  - "https://www.sistrix.com/faq/what-is-the-sistrix-visibility-index/"
parent: "serp-metric"
namespace: "metrics"
relations:
  - predicate: RELATED_TO
    target: "share-of-voice"
    description: "Share of Voice is the competitive version of Visibility Index"
  - predicate: RELATED_TO
    target: "average-position"
    description: "Visibility Index is position-weighted — lower positions contribute less"
  - predicate: MEASURES
    target: "organic-result"
    description: "Visibility Index aggregates position data into a single domain-level score"
attributes:
  formula: "Weighted sum of (position-based CTR × keyword search volume) across tracked keyword universe"
  source_tool:
    - "SISTRIX (Visibility Index)"
    - "Semrush (Authority Score / Visibility)"
    - "Ahrefs (Organic Traffic estimate)"
    - "SE Ranking (Visibility Score)"
  unit: "Indexed score (SISTRIX: 0 to unbounded; others: 0–100)"
  direction: higher-is-better
  benchmark: "Varies by industry and domain size — relative comparison is most useful"
  primary_use: "Macro-level tracking of organic search performance over time"
  algorithmic_change_sensitivity: "High — visibility drops after core updates are one of the primary signals of algorithmic impact"
evidence:
  - source: "https://www.sistrix.com/faq/what-is-the-sistrix-visibility-index/"
    title: "What is the SISTRIX Visibility Index?"
    publisher: "SISTRIX"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://moz.com/learn/seo/search-visibility"
    title: "Search Visibility"
    publisher: "Moz"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Visibility Index

## Definition

The Visibility Index is a composite SEO metric that aggregates organic search ranking data across a large keyword set into a single, comparable score representing a domain's overall visibility in search results. It weights rankings by estimated keyword search volume and position-based CTR to produce a single number that tracks SERP presence over time.

## Description

Individual keyword rankings are too granular to give a holistic picture of a site's organic search health. A site might rank #1 for 50 keywords and #15 for 500 others — what does that mean for overall visibility? The Visibility Index answers this by computing a weighted aggregate score.

SISTRIX's Visibility Index is the most widely cited version in European SEO, calculated weekly from a large fixed keyword set (hundreds of thousands of keywords per country). A domain's score reflects the sum of expected CTR contributions from each ranking keyword, where each keyword's contribution is CTR(position) × search_volume. The resulting score tracks directional changes in organic performance — whether a domain is gaining or losing overall visibility.

Visibility Index scores are most valuable for:
- **Pre/post algorithm update analysis** — tracking which domains gained or lost visibility after a core update
- **Competitor benchmarking** — comparing visibility trajectories with competing domains
- **Long-term trend monitoring** — identifying multi-month growth or decline patterns that individual keyword fluctuations obscure

Different tools use different keyword universes and weighting methodologies, making cross-tool comparison unreliable. Consistency within a single tool over time is what matters.

## Key Attributes

**Primary Value:** Macro trend visibility — directional comparison over time and between domains.

**Tool Dependency:** Metric definitions vary by tool (SISTRIX, Semrush, Ahrefs use different approaches). Only compare within the same tool.

**Algorithm Update Signal:** Sharp drops in Visibility Index correlated with core update timing are the primary indicator of algorithmic impact.

## Status & Evolution

**Current Status:** Active — standard KPI for enterprise SEO reporting.

## Evidence & Sources

- [What is the SISTRIX Visibility Index?](https://www.sistrix.com/faq/what-is-the-sistrix-visibility-index/) — SISTRIX, retrieved 2026-06-09
- [Search Visibility](https://moz.com/learn/seo/search-visibility) — Moz, retrieved 2026-06-09
