---
entityId: "your-entity-id"
name: "Your Entity Name"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Alternative Name 1"
  - "Alternative Name 2"
sameAs:
  - "https://en.wikipedia.org/wiki/..."
  - "https://www.wikidata.org/wiki/Q..."
parent: "parent-entity-id"
namespace: "serp-features"
relations:
  - predicate: IS_TYPE_OF
    target: "parent-entity-id"
    description: "One-line explanation of this relationship"
  - predicate: TRIGGERED_BY
    target: "informational-intent"
    description: "One-line explanation of this relationship"
  - predicate: COMPETES_WITH
    target: "competing-entity-id"
    description: "One-line explanation of this relationship"
attributes:
  position: "Above organic results"
  trigger_intents:
    - informational
    - how-to
  ctr_impact: high
  schema_required: null
  owned_by: "Google"
  introduced: "2014"
  display: "Description of what the user sees"
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://developers.google.com/search/docs/..."
    title: "Source Page Title"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
    quote: "Optional key quote from the source (max 200 chars)"
  - source: "https://example.com/second-source"
    title: "Second Source Title"
    publisher: "Publisher Name"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Your Entity Name

## Definition

[One to three sentences giving a precise, authoritative definition. What this entity *is*. Use plain, grounding language.]

## Description

[Paragraph 1: How this entity works mechanically. What triggers it, how Google generates or decides to show it, what data sources power it.]

[Paragraph 2: When and why it appears. The conditions under which a user will encounter this entity on the SERP. Query types, intent signals, device conditions.]

[Paragraph 3: Its place in the broader SERP ecosystem. How it relates to other features, what it displaces or coexists with, its visual prominence.]

[Paragraph 4: Historical context. When it was introduced, major changes it has undergone, significant milestones.]

[Paragraph 5 (optional): Edge cases, known limitations, or nuances practitioners should be aware of.]

## Key Attributes

**Position:** [Where on the SERP this entity appears — top, right rail, mid-SERP, bottom, mobile-only, etc.]

**Trigger Conditions:** [What query types, intent signals, or structured data triggers this entity to appear.]

**Display Elements:** [What information is visually shown — title, description, image, rating, price, etc.]

**Search Engine Ownership:** [Which search engine(s) display this feature. Google, Bing, both, or other.]

**Device Availability:** [Desktop, mobile, or both — and any significant differences between platforms.]

**Schema Requirement:** [If structured data is required to appear, specify the Schema.org type and required fields.]

## Optimization Relevance

[Paragraph 1: What SEO practitioners can do to earn or optimize this feature. Be specific — which markup, which content formats, which structural choices.]

[Paragraph 2: What cannot be controlled. What is entirely in Google's hands, what cannot be opted into, what is algorithmically determined.]

[Paragraph 3: The strategic implications. When should you prioritize this? What are the CTR and traffic implications? Are there any risks?]

## Relations

- **[Related Entity Name]** (`[predicate]`): [One sentence explaining why this relationship matters.]
- **[Related Entity Name]** (`[predicate]`): [One sentence explaining why this relationship matters.]
- **[Related Entity Name]** (`[predicate]`): [One sentence explaining why this relationship matters.]

## Status & Evolution

**Current Status:** [active / deprecated / emerging / experimental]

[One paragraph on the current status and any recent significant changes. If deprecated, explain what replaced it and when. If emerging, explain what's known and what's still evolving.]

## Evidence & Sources

- [Source Title](source_url) — [Publisher], retrieved [date]
- [Source Title](source_url) — [Publisher], retrieved [date]
