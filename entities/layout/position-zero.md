---
entityId: "position-zero"
name: "Position Zero"
type: Layout_Element
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "P0"
  - "Featured Position"
  - "Above Position One"
  - "Answer Box Position"
sameAs:
  - "https://moz.com/learn/seo/featured-snippets"
parent: "serp-layout"
namespace: "layout"
relations:
  - predicate: CONTAINS
    target: "featured-snippet"
    description: "Featured Snippets occupy Position Zero"
  - predicate: RELATED_TO
    target: "ai-overview"
    description: "AI Overviews appear above Position Zero, effectively creating a new supra-position"
attributes:
  position: "Above all organic results, below search bar and any ads"
  occupied_by:
    - featured-snippet
  predecessor_in_value: "AI Overviews now appear above Position Zero"
  click_implications: "Complex — can increase CTR (more prominent) or decrease it (zero-click)"
  introduced: "~2014 with Featured Snippets"
evidence:
  - source: "https://moz.com/learn/seo/featured-snippets"
    title: "Featured Snippets"
    publisher: "Moz"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
  - source: "https://backlinko.com/featured-snippets-guide"
    title: "Featured Snippets: The Definitive Guide"
    publisher: "Backlinko"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Position Zero

## Definition

Position Zero refers to the Featured Snippet placement at the top of the SERP, above the standard organic results. The term captures the idea that this placement precedes Position 1 and therefore exists "before" the traditional ranking system begins.

## Description

Position Zero emerged as a concept when Google began extracting Featured Snippets and placing them above all organic results around 2014. For practitioners, "Position Zero" provided a way to describe a SERP placement that was neither a traditional organic position nor an ad.

A page occupying Position Zero simultaneously holds an organic ranking (typically positions 1–10) — the Featured Snippet extraction comes from a ranked page, but the snippet itself is displayed above that page's normal organic position. Until 2020, this meant the same page could appear twice: once as the Featured Snippet and again as its organic position. Google's 2020 de-duplication change removed this double-appearance.

With the rise of AI Overviews (2024), a new layer has been added above Position Zero. AI Overviews appear above Featured Snippets, creating a de facto "Position -1" for AI-generated answers. When an AI Overview is present, the Featured Snippet may be suppressed or pushed below it.

## Key Attributes

**Location:** Top of organic results area — below the search bar and any paid ads, above all standard organic listings.

**Current Occupant:** Featured Snippet (when no AI Overview is present). AI Overview (when triggered, appearing above the Featured Snippet position).

**Strategic Value:** Highest organic visibility on the page. Click behavior varies — commanding position for brand visibility regardless of CTR.

## Status & Evolution

**Current Status:** Active concept — but increasingly superseded by AI Overviews appearing "above" Position Zero.

## Evidence & Sources

- [Featured Snippets](https://moz.com/learn/seo/featured-snippets) — Moz, retrieved 2026-06-09
- [Featured Snippets: The Definitive Guide](https://backlinko.com/featured-snippets-guide) — Backlinko, retrieved 2026-06-09
