---
entityId: "knowledge-graph"
name: "Google Knowledge Graph"
type: Entity_Type
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "KG"
  - "Google Knowledge Base"
  - "Google Entity Graph"
  - "Google Freebase"
sameAs:
  - "https://en.wikipedia.org/wiki/Google_Knowledge_Graph"
  - "https://blog.google/products/search/introducing-knowledge-graph-things-not/"
parent: "knowledge-entity"
namespace: "knowledge-entities"
relations:
  - predicate: POWERS
    target: "knowledge-panel"
    description: "Knowledge Graph data populates Knowledge Panels"
  - predicate: POWERS
    target: "knowledge-card"
    description: "Knowledge Cards answer simple factual queries via KG data"
  - predicate: POWERS
    target: "ai-overview"
    description: "Knowledge Graph entities ground AI Overview factual accuracy"
  - predicate: RELATED_TO
    target: "entity-establishment"
    description: "Entity establishment is the process of entering the Knowledge Graph"
  - predicate: RELATED_TO
    target: "entity-disambiguation"
    description: "The Knowledge Graph enables entity disambiguation via unique entity IDs"
attributes:
  launched: "2012-05"
  announced_by: "Amit Singhal, Google SVP Engineering"
  size: "Hundreds of billions of facts about billions of entities (estimated)"
  data_sources:
    - Wikipedia
    - Wikidata
    - Freebase (incorporated 2014)
    - CIA World Factbook
    - Licensed data providers
    - Official website structured data (Schema.org)
    - Google Business Profile
    - User feedback and edits
  entity_types:
    - Person
    - Organization
    - Place
    - Product
    - Event
    - CreativeWork
    - Concept
    - Species
    - Chemical compound
    - Astronomical object
  founding_insight: "Things, not strings — understanding entities, not keyword matches"
  api_access: "Google Knowledge Graph Search API (limited public access)"
evidence:
  - source: "https://en.wikipedia.org/wiki/Google_Knowledge_Graph"
    title: "Google Knowledge Graph — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
  - source: "https://blog.google/products/search/introducing-knowledge-graph-things-not/"
    title: "Introducing the Knowledge Graph: things, not strings"
    publisher: "Google Blog"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
    quote: "The Knowledge Graph enables you to search for things, people or places that Google knows about."
lastReviewed: "2026-06-09"
---

# Google Knowledge Graph

## Definition

The Google Knowledge Graph is a knowledge base of real-world entities and their relationships, maintained by Google to power entity-based search understanding. It enables Google to recognize people, places, organizations, products, and concepts as distinct entities — not just strings of text — and surface structured, factual information about them directly in search results.

## Description

The Knowledge Graph was Google's most consequential shift from keyword-based to entity-based search. Announced in May 2012 with the tagline "things, not strings," it represented the operationalization of semantic web concepts at global search scale.

Before the Knowledge Graph, Google processed queries as bags of keywords. "Einstein" in a search was just a string of characters. With the Knowledge Graph, "Einstein" became a specific entity — Albert Einstein (Knowledge Graph ID: /m/0jcx) — with structured properties: birthdate (March 14, 1879), nationality (German-American), profession (physicist), notable works (Theory of General Relativity, Photoelectric Effect), and relationships (married to Mileva Marić, then Elsa Löwenthal).

The Knowledge Graph's data sources are hierarchical. Primary sources include: Wikipedia articles (for descriptive text), Wikidata (for structured properties and cross-language entity identification), and licensed data from specialized providers. Secondary sources include structured data (Schema.org markup) from official websites, Google Business Profile data for local entities, and factual corrections submitted through Google's feedback mechanisms.

The Knowledge Graph powers multiple SERP features: Knowledge Panels display entity summaries; Knowledge Cards answer factual queries directly; AI Overviews use Knowledge Graph entities to ground generated answers factually; and query understanding systems use Knowledge Graph entity recognition to disambiguate ambiguous queries.

The Knowledge Graph Search API provides limited programmatic access to a subset of Knowledge Graph data, primarily for developers building entity-aware applications. It returns entity types, descriptions, and URLs but not the full entity property graph.

## Key Attributes

**Scale:** Estimated hundreds of billions of facts across billions of entities across dozens of entity types and hundreds of languages.

**Uniqueness:** Each entity has a unique Machine ID (MID), enabling disambiguation across contexts and languages.

**Open Standards Connection:** Wikidata serves as the primary cross-reference for Knowledge Graph entity identification — the `sameAs` link to a Wikidata Q-number is the most reliable cross-reference between the KG and open standards.

## Relations

- **Knowledge Panel** (`POWERS`): Knowledge Panels are the SERP visualization of Knowledge Graph entities.
- **Entity Establishment** (`RELATED_TO`): The process of gaining a Knowledge Graph entity is central to modern entity SEO.
- **AI Overview** (`POWERS`): Knowledge Graph facts ground AI Overview responses and prevent hallucinations on established entities.

## Status & Evolution

**Current Status:** Active — continuously expanding.

The Knowledge Graph has grown from ~500 million entities in 2012 to billions, expanding entity types, languages, and property depth. AI integration has deepened the connection between the Knowledge Graph and generative search — Gemini uses Knowledge Graph entity data as a factual grounding layer for AI Overviews, making Knowledge Graph presence increasingly valuable for brand and entity visibility in the AI search era.

## Evidence & Sources

- [Google Knowledge Graph — Wikipedia](https://en.wikipedia.org/wiki/Google_Knowledge_Graph) — Wikipedia, retrieved 2026-06-09
- [Introducing the Knowledge Graph: things, not strings](https://blog.google/products/search/introducing-knowledge-graph-things-not/) — Google Blog, retrieved 2026-06-09
