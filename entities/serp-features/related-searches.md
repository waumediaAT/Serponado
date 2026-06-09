---
entityId: "related-searches"
name: "Related Searches"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Searches Related To"
  - "Related Queries"
  - "Bottom SERP Searches"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: RELATED_TO
    target: "people-also-ask"
    description: "Both are query expansion features; PAA offers question-format, Related Searches offers keyword variants"
  - predicate: RELATED_TO
    target: "people-also-search-for"
    description: "Related Searches shows query variants; PASF shows back-click alternatives"
attributes:
  position: "Bottom of SERP (primary), occasionally mid-SERP"
  trigger_intents: [all]
  ctr_impact: low
  schema_required: null
  owned_by: "Google"
  introduced: "2008"
  count: "6–8 suggestions typically"
  display: "Grid or list of related query suggestions with small search icons"
  seo_value: "Keyword research, semantic cluster identification, topical gap analysis"
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://moz.com/learn/seo/related-searches"
    title: "Related Searches in Google"
    publisher: "Moz"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
  - source: "https://ahrefs.com/blog/related-searches/"
    title: "Google Related Searches: How to Use Them for SEO"
    publisher: "Ahrefs"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Related Searches

## Definition

Related Searches is a SERP feature displaying 6–8 algorithmically generated query suggestions at the bottom of the SERP (and sometimes mid-page), showing related terms and phrases that users commonly search for alongside or after the current query.

## Description

Related Searches appears at the bottom of nearly every Google SERP. It represents Google's mapping of the semantic neighborhood around a query — the adjacent topics, synonymous phrases, and related concepts that belong to the same information ecosystem.

The suggestions are derived from aggregate user search behavior: queries that users commonly search for in the same session, before or after the current query, or as alternative formulations of similar intent. Unlike People Also Ask (which shows question variants), Related Searches shows keyword and phrase variants — offering alternative formulations, narrower subtopics, broader categories, and related but distinct concepts.

For SEO practitioners, Related Searches is primarily a **keyword research and content planning tool**. Systematically documenting Related Searches for a target keyword cluster reveals the semantic coverage expected of a comprehensive resource on that topic. Content that addresses all the related searches associated with a primary topic is more likely to achieve topical authority status.

## Key Attributes

**Position:** Bottom of SERP — always present. Some queries also show a mid-page Related Searches section in addition to the bottom placement.

**Count:** Typically 6–8 suggestions displayed simultaneously.

**Research Value:** Direct insight into Google's semantic associations — what related topics should be covered in a comprehensive page addressing the primary query.

## Optimization Relevance

Related Searches cannot be directly optimized — they are generated algorithmically. Their SEO value is as a research tool: using Related Searches to expand content outlines, identify supporting pages for a topic cluster, and find natural semantic variations of target keywords.

## Status & Evolution

**Current Status:** Active. One of the oldest and most consistent SERP features — has been present since at least 2008.

## Evidence & Sources

- [Related Searches in Google](https://moz.com/learn/seo/related-searches) — Moz, retrieved 2026-06-09
- [Google Related Searches: How to Use Them for SEO](https://ahrefs.com/blog/related-searches/) — Ahrefs, retrieved 2026-06-09
