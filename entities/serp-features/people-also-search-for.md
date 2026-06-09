---
entityId: "people-also-search-for"
name: "People Also Search For"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "PASF"
  - "Others Also Searched For"
  - "Related Searches on Back-click"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: RELATED_TO
    target: "related-searches"
    description: "Both surface related queries; PASF triggers specifically on back-click behavior"
  - predicate: RELATED_TO
    target: "people-also-ask"
    description: "Both are discovery features within the SERP ecosystem"
attributes:
  position: "Appears beneath a result after a user back-clicks from it"
  trigger_intents: [all]
  ctr_impact: low
  schema_required: null
  owned_by: "Google"
  introduced: "2018"
  trigger_mechanism: "User clicks a result, immediately returns to SERP (back-click / pogo-stick)"
  display: "Grid of related site/query suggestions shown beneath the result that was just visited"
  seo_implication: "Appearing in PASF for a competitor indicates user dissatisfaction with that result"
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://searchengineland.com/google-also-searched-for-feature-explained-311840"
    title: "Google Also Searched For Feature Explained"
    publisher: "Search Engine Land"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
  - source: "https://www.seroundtable.com/google-people-also-search-for-25849.html"
    title: "Google People Also Search For"
    publisher: "SE Roundtable"
    retrieved: "2026-06-09"
    relevanceScore: 0.8
lastReviewed: "2026-06-09"
---

# People Also Search For

## Definition

People Also Search For (PASF) is a SERP feature that appears beneath an organic result after a user clicks that result and then immediately returns to the SERP (a "back-click" or "pogo-stick" behavior). It displays alternative queries and related sites that other users with similar searches also visited, helping users refine or redirect their search after not finding what they needed.

## Description

PASF is triggered by user dissatisfaction signals. When Google detects that a user clicked an organic result but returned to the SERP quickly — suggesting the result did not satisfy the query — it displays the PASF box beneath that result on the user's return. This serves as a recovery mechanism, offering alternative paths to satisfy the query.

The PASF suggestions are derived from aggregate query-session data: what other users searched for in the same session when visiting similar results. This makes PASF a unique window into competitive landscape analysis — if your competitors frequently appear in PASF boxes for target keywords, it signals that users who visited those pages were not satisfied and continued searching.

For publishers, appearing in PASF is a double-edged signal: it indicates your competitors are not satisfying users, giving you an opportunity to capture traffic. But if your own pages appear in competitor PASF boxes, it suggests a traffic opportunity. PASF is primarily a research and competitive intelligence signal rather than an optimization target.

## Key Attributes

**Trigger Mechanism:** User back-click (pogo-stick behavior) from an organic result.

**Competitive Implication:** If Site A appears in PASF after users visit Site B, it means users who were dissatisfied with Site B found Site A more relevant. This is a strong signal that Site A and Site B compete for similar queries.

## Status & Evolution

**Current Status:** Active. Limited direct optimization relevance; primarily useful as a competitive research signal.

## Evidence & Sources

- [Google Also Searched For Feature Explained](https://searchengineland.com/google-also-searched-for-feature-explained-311840) — Search Engine Land, retrieved 2026-06-09
- [Google People Also Search For](https://www.seroundtable.com/google-people-also-search-for-25849.html) — SE Roundtable, retrieved 2026-06-09
