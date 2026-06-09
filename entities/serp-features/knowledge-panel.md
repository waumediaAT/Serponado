---
entityId: "knowledge-panel"
name: "Knowledge Panel"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "KP"
  - "Entity Panel"
  - "Google Knowledge Box"
sameAs:
  - "https://en.wikipedia.org/wiki/Knowledge_panel"
  - "https://developers.google.com/search/docs/appearance/structured-data/knowledge-graph"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: POWERED_BY
    target: "knowledge-graph"
    description: "Knowledge Panels are generated from Knowledge Graph entity data"
  - predicate: COMPETES_WITH
    target: "featured-snippet"
    description: "Both appear in top-of-SERP position for entity queries"
  - predicate: TRIGGERED_BY
    target: "navigational"
    description: "Brand and entity queries trigger Knowledge Panels"
  - predicate: RELATED_TO
    target: "knowledge-card"
    description: "Knowledge Card is a simpler, fact-only variant"
  - predicate: REQUIRES
    target: "entity-establishment"
    description: "An entity must be in the Knowledge Graph to get a Knowledge Panel"
attributes:
  position: "Right rail (desktop), top of SERP (mobile)"
  trigger_intents:
    - navigational
    - informational
    - brand
  ctr_impact: medium
  schema_required: "Organization, Person, LocalBusiness, or other entity type"
  owned_by: "Google"
  introduced: "2012"
  claimable: true
  claim_method: "Google Search Console verification"
  sections:
    - Summary description
    - Images
    - Key facts (founding date, CEO, headquarters, etc.)
    - Social profiles
    - Related entities
    - Reviews (for businesses)
    - Posts (for businesses)
  data_sources:
    - Wikipedia
    - Wikidata
    - Official website structured data
    - Google Business Profile
    - Licensed data providers
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://developers.google.com/search/docs/appearance/knowledge-graph"
    title: "Knowledge Graph in Google Search"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://en.wikipedia.org/wiki/Knowledge_panel"
    title: "Knowledge panel — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Knowledge Panel

## Definition

A Knowledge Panel is a large, structured information box that Google displays on the right side of desktop SERPs (or at the top of mobile SERPs) for recognized entities — people, organizations, places, products, and concepts that exist in Google's Knowledge Graph. It provides a comprehensive summary of the entity sourced from multiple authoritative data providers.

## Description

Knowledge Panels are the SERP's most visible expression of Google's entity-based understanding of the world. When a user searches for a recognized entity — a brand, a public figure, a landmark, a movie — Google generates a rich information card drawing from its Knowledge Graph, which synthesizes data from Wikipedia, Wikidata, official websites, structured data markup, and licensed data providers.

The panel provides key facts specific to the entity type. For organizations, this typically includes founding date, headquarters, leadership, number of employees, stock ticker, social profiles, and a short description. For people, it shows birthdate, nationality, notable works, relationships, and associated organizations. For local businesses, it integrates Google Business Profile data — hours, address, phone number, photos, and reviews.

Desktop display places the Knowledge Panel in the right column, occupying 300–400px of width beside the organic results list. On mobile, the panel collapses to a top-of-page card with a tap-to-expand pattern. The visual prominence of Knowledge Panels is exceptional — they signal to users that Google recognizes and has structured knowledge about the queried entity, strongly reinforcing brand credibility.

Entity owners (individuals, organizations) can claim their Knowledge Panel through Google Search Console. Claiming enables suggesting edits to factual information, adding official social profiles, and flagging inaccuracies. Ownership does not give full editorial control — Google retains final say on what data is displayed.

The Knowledge Panel was introduced alongside the Knowledge Graph in May 2012 and has expanded significantly since. In 2021, Google integrated AI-generated summaries from the Knowledge Graph into the panel description for some entities. As of 2024–2026, AI Overviews and the Knowledge Panel coexist, with the panel maintaining its position for navigational and entity-specific queries.

## Key Attributes

**Position:** Right rail on desktop (beside organic results). Top of SERP on mobile (above organic results, below the search bar). The right-rail position is unique to Knowledge Panels and Google Shopping — standard organic results never appear there.

**Trigger Conditions:** Branded and navigational queries where Google has high confidence in the entity identity. Queries matching a recognized Knowledge Graph entity (a company name, person's full name, place name, product line).

**Display Elements:** Entity name and type label, description paragraph, image/photo, key fact pairs (varies by entity type), social profile links, related entities carousel, and entity-type-specific elements (business hours, stock price, filmography, discography, etc.).

**Search Engine Ownership:** Google (Knowledge Panel). Bing has an analogous "Knowledge Widget" powered by its own entity graph.

**Device Availability:** Desktop (right rail) and mobile (top of SERP). Knowledge Panels are significantly more prominent on mobile where they fill the entire screen.

**Schema Requirement:** Structured data on the entity's official website (`Organization`, `Person`, `LocalBusiness`, etc.) helps Google associate and verify Knowledge Graph data, but is not strictly required — panels can generate from Wikipedia/Wikidata data alone.

## Optimization Relevance

Earning a Knowledge Panel requires establishing an entity in Google's Knowledge Graph. The primary pathway is a Wikipedia article meeting Wikipedia's notability standards, supported by a Wikidata entry with structured properties. For organizations and public figures without Wikipedia coverage, extensive press coverage, social profile verification, and consistent structured data (`Organization` schema with `sameAs` links to Wikidata/Wikipedia) are the alternative path.

Once a Knowledge Panel exists, claiming it via Google Search Console allows the entity owner to suggest corrections and add official social profile links. While Google controls final data display, a claimed panel tends to be more accurate and up-to-date.

For local businesses, Google Business Profile data is the primary source for the Local Knowledge Panel. Completing the GBP profile comprehensively, verifying ownership, and maintaining fresh posts/photos directly affects the panel's content.

## Relations

- **Knowledge Graph** (`POWERED_BY`): The Knowledge Graph is the underlying data store that Knowledge Panels visualize.
- **Knowledge Card** (`RELATED_TO`): Knowledge Card is a simplified fact-answer variant that appears for simple factual queries without generating a full panel.
- **Entity Establishment** (`REQUIRES`): An entity must be recognized in the Knowledge Graph before a panel will generate.
- **Featured Snippet** (`COMPETES_WITH`): For question queries about entities, Google may show either a Featured Snippet or a Knowledge Panel, depending on whether the answer lives in the Knowledge Graph or in indexed page content.

## Status & Evolution

**Current Status:** Active — core SERP feature with no deprecation signals.

Knowledge Panels have expanded in scope and richness since their 2012 launch. Key milestones include integration with Google Business Profile data (2014), the addition of the "claim your panel" feature (2017), integration of user-submitted photos and reviews, and the 2021 expansion of AI-generated summaries. As AI Overviews expand, Knowledge Panels remain distinct because they serve entity recognition rather than query answering — they coexist with AI Overviews rather than competing with them directly.

## Evidence & Sources

- [Knowledge Graph in Google Search](https://developers.google.com/search/docs/appearance/knowledge-graph) — Google Search Central, retrieved 2026-06-09
- [Knowledge panel](https://en.wikipedia.org/wiki/Knowledge_panel) — Wikipedia, retrieved 2026-06-09
