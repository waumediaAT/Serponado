---
entityId: "panda"
name: "Google Panda"
type: Algorithm_Update
schemaType: DefinedTerm
version: 1.0.0
status: deprecated
aliases:
  - "Panda Update"
  - "Farmer Update"
  - "Content Quality Update"
sameAs:
  - "https://en.wikipedia.org/wiki/Google_Panda"
parent: "google-algorithm-update"
namespace: "algorithms"
relations:
  - predicate: REPLACED_BY
    target: "helpful-content"
    description: "Helpful Content System is Panda's spiritual successor for AI-era content quality"
  - predicate: AFFECTS
    target: "content-quality"
    description: "Panda operationalized content quality as a site-level signal"
  - predicate: RELATED_TO
    target: "e-e-a-t"
    description: "Panda's quality criteria anticipated the E-E-A-T framework"
attributes:
  launched: "2011-02-24"
  incorporated_into_core: "2016"
  type: quality
  target: "Low-quality, thin, duplicate, and content farm content"
  scope: "site"
  mechanism: "Site-wide quality score based on content quality ratio"
  named_after: "Navneet Panda, Google engineer who developed the key technical solution"
  initial_impact: "~12% of search queries affected at launch"
  versions_count: 28
evidence:
  - source: "https://en.wikipedia.org/wiki/Google_Panda"
    title: "Google Panda — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
  - source: "https://searchengineland.com/google-panda-update-hits-content-farms-66408"
    title: "Google Panda Update Hits Content Farms"
    publisher: "Search Engine Land"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Google Panda

## Definition

Google Panda was a major algorithm update launched February 24, 2011, targeting low-quality, thin, duplicate, and content-farm content. It introduced site-level content quality scoring — where a high proportion of low-quality pages on a domain could reduce rankings for all pages on that domain. Panda was incorporated into Google's core algorithm in 2016 and now runs continuously.

## Description

Before Panda, content farms — sites producing large volumes of low-quality articles optimized for search traffic rather than user value — dominated many SERPs. Sites like Demand Media's eHow and Answers.com produced thousands of articles based solely on keyword search volume, with minimal quality control. Panda targeted these patterns specifically.

Panda introduced the concept of a **site-wide quality signal**: Google's systems evaluated the overall proportion of useful versus low-quality content on a domain. A site where 40% of pages were thin or low-quality received a Panda penalty that affected the entire domain, including otherwise good pages. This created urgency for publishers to either improve or remove low-quality content.

Panda ran as a distinct periodic filter from 2011 until 2016, when it was incorporated into Google's core algorithm to run continuously. With 28+ named versions over its discrete lifecycle, Panda updates caused cyclical "Panda dance" patterns where some sites would recover with each new version while others were newly hit.

Panda is the philosophical ancestor of the Helpful Content System (2022), which applies similar site-level quality logic using modern ML classifiers rather than Panda's earlier signal-based approach.

## Status & Evolution

**Current Status:** Deprecated as a named update — functionality incorporated into core algorithm since 2016.

## Evidence & Sources

- [Google Panda — Wikipedia](https://en.wikipedia.org/wiki/Google_Panda) — Wikipedia, retrieved 2026-06-09
- [Google Panda Update Hits Content Farms](https://searchengineland.com/google-panda-update-hits-content-farms-66408) — Search Engine Land, retrieved 2026-06-09
