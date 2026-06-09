# Serponado Entity Standard — v1.0.0

This document defines the canonical format for all entity pages in the Serponado repository. Every entity file must conform to this standard to ensure machine-parseability, cross-referenceability, and grounding consistency.

---

## File Format

Entity pages are **Markdown files with YAML frontmatter**.

- Filename: `[entityId].md` (kebab-case, matching the `entityId` field)
- Location: `entities/[namespace]/[entityId].md`
- Encoding: UTF-8

---

## Frontmatter Schema

```yaml
---
entityId: string           # REQUIRED. Unique kebab-case ID. No spaces. E.g.: featured-snippet
name: string               # REQUIRED. Human-readable display name. E.g.: Featured Snippet
type: EntityType           # REQUIRED. See EntityType enum below
schemaType: string         # RECOMMENDED. Most relevant Schema.org type. E.g.: DefinedTerm
version: semver            # REQUIRED. Semantic version of this entity record. Default: 1.0.0
status: Status             # REQUIRED. See Status enum below
aliases: string[]          # RECOMMENDED. Alternative names, former names, informal names
sameAs: URI[]              # RECOMMENDED. Links to Wikipedia, Wikidata, or other KB URIs
parent: entityId           # OPTIONAL. The entityId of the broader entity this belongs to
namespace: string          # REQUIRED. Subfolder in entities/. E.g.: serp-features
relations: Relation[]      # RECOMMENDED. Typed relationships to other Serponado entities
attributes: object         # REQUIRED. Key-value attributes specific to this entity type
evidence: Evidence[]       # REQUIRED. At least 2 citations supporting key claims
lastReviewed: date         # REQUIRED. ISO 8601 date (YYYY-MM-DD) of last content review
---
```

---

## Field Definitions

### `entityId`

A globally unique, lowercase, hyphen-delimited identifier. Used for file naming, cross-references, and the `index.json` master index.

**Rules:**
- Lowercase only
- Hyphens between words (no underscores, no spaces)
- No special characters except hyphens
- Must be unique across the entire repository

**Examples:** `featured-snippet`, `e-e-a-t`, `rankbrain`, `ai-overview`

---

### `name`

The primary human-readable name of the entity. Title Case recommended.

**Examples:** `Featured Snippet`, `E-E-A-T`, `RankBrain`, `AI Overview`

---

### `type`

The entity's type from the EntityType enum. Determines which attributes are expected and how the entity relates to others in the graph.

**EntityType Enum:**
```
SERP_Feature          # A feature that appears on the SERP
Paid_Feature          # An advertising/paid SERP placement
Ranking_Factor        # A signal that influences position in results
Algorithm             # A core algorithm component (RankBrain, BERT, MUM)
Algorithm_Update      # A named update event (Panda, Penguin, Helpful Content)
Search_Intent         # A query intent type classification
Metric                # A measurable performance or authority signal
Technical_Attribute   # A technical SEO property or configuration
AI_Search_Feature     # An AI-augmented search feature or concept
Layout_Element        # A SERP layout position or anatomical component
Entity_Type           # A category of real-world entity (Person, Org, Place)
Tool                  # An SEO or search-related tool or platform
Concept               # An abstract SERP or SEO concept
```

---

### `schemaType`

The most relevant [Schema.org](https://schema.org) type for this entity. Use `DefinedTerm` for concepts that don't map directly to a Schema.org type.

**Common values:** `DefinedTerm`, `WebPage`, `SoftwareApplication`, `Organization`, `Action`, `Thing`

---

### `version`

Semantic version string for this entity record. Increment the PATCH version for corrections, MINOR for new attributes/relations, MAJOR for structural changes.

**Default:** `1.0.0`

---

### `status`

Current lifecycle status of the entity.

**Status Enum:**
```
active        # Currently present and active in Google/search ecosystem
deprecated    # No longer active; replaced or removed
emerging      # Newly introduced; behavior still evolving
experimental  # Google testing; not widely deployed
historical    # Only relevant historically; no longer exists
```

---

### `aliases`

Array of alternative names for this entity. Include:
- Former names (e.g., `Google My Business` for `Google Business Profile`)
- Informal names (e.g., `Answer Box` for `Featured Snippet`)
- Abbreviated forms (e.g., `PAA` for `People Also Ask`)
- Names used by other engines (e.g., `Bing Knowledge Widget`)

---

### `sameAs`

Array of URIs to external knowledge base representations of this entity.

**Preferred sources (in priority order):**
1. Wikipedia article URL
2. Wikidata entity URL (`https://www.wikidata.org/wiki/Q...`)
3. Google Search Central documentation URL
4. Schema.org type URL

---

### `parent`

The `entityId` of the broader entity that this entity is a subtype or component of. Creates a hierarchical taxonomy.

**Examples:**
- `featured-snippet` → parent: `serp-feature`
- `paragraph-featured-snippet` → parent: `featured-snippet`
- `lcap` → parent: `core-web-vitals`

---

### `namespace`

The subdirectory path within `entities/` where this file lives.

**Valid namespaces:**
```
serp-features
paid-features
ranking-factors
algorithms
intent
metrics
technical
ai-search
layout
knowledge-entities
```

---

### `relations`

Array of typed relationships connecting this entity to other Serponado entities.

**Relation object schema:**
```yaml
- predicate: RelationPredicate   # See predicate list below
  target: entityId               # The entityId of the related entity
  description: string            # OPTIONAL. One-line explanation of the relationship
```

**Relation Predicates:**
```
IS_TYPE_OF          # This entity is a subtype/instance of target
HAS_SUBTYPE         # This entity has target as a named subtype
PART_OF             # This entity is a component of target
CONTAINS            # This entity includes target as a component
TRIGGERS            # This entity causes or activates target
TRIGGERED_BY        # This entity is caused/activated by target
COMPETES_WITH       # This entity and target compete for same SERP space
REQUIRES            # This entity requires target to function
POWERS              # This entity powers or enables target
POWERED_BY          # This entity is powered/enabled by target
REPLACED_BY         # This entity was replaced by target
REPLACES            # This entity replaced target
MEASURES            # This metric quantifies target
MEASURED_BY         # This entity is quantified by target metric
OPTIMIZED_BY        # This entity is optimized through target practice
AFFECTS             # This entity influences target
INTRODUCED_BY       # This entity was introduced by target (algorithm/update)
DEPRECATED_BY       # This entity was made obsolete by target
RELATED_TO          # General semantic relationship
ANALOGOUS_TO        # Functionally similar to target in a different context
```

---

### `attributes`

A key-value map of entity-specific attributes. Required attributes vary by entity type.

**SERP_Feature required attributes:**
```yaml
attributes:
  position: string | string[]     # Where on the SERP it appears
  trigger_intents: string[]       # Which intent types trigger this feature
  ctr_impact: low | medium | high | variable
  schema_required: string | null  # Schema.org type needed, if any
  owned_by: string                # Which search engine controls this
  introduced: year                # Year first deployed
  display: string                 # What it shows (free text)
  mobile_display: boolean
  desktop_display: boolean
```

**Ranking_Factor required attributes:**
```yaml
attributes:
  factor_type: on-page | off-page | technical | user-signal | semantic
  weight: low | medium | high | confirmed | speculative
  confirmed_by: string[]          # Sources confirming it as a ranking factor
  affects_feature: string[]       # Which SERP features this factor enables
```

**Algorithm required attributes:**
```yaml
attributes:
  launched: date
  type: filter | ranking | nlp | ml | spam | quality
  target: string                  # What it evaluates or acts on
  scope: query | page | site | link-graph | all
  incorporated_into_core: date | null
```

**Metric required attributes:**
```yaml
attributes:
  formula: string | null          # Mathematical formula if applicable
  source_tool: string[]           # Tools that report this metric
  unit: string                    # Measurement unit (%, seconds, count, etc.)
  benchmark: string | null        # Industry benchmark or target range
  direction: higher-is-better | lower-is-better | contextual
```

---

### `evidence`

Array of citation objects supporting the entity's claims. Minimum 2 required.

**Evidence object schema:**
```yaml
- source: URI                     # REQUIRED. Direct URL to the source
  title: string                   # REQUIRED. Title of the source page/document
  publisher: string               # RECOMMENDED. Publisher or organization name
  retrieved: date                 # REQUIRED. ISO 8601 date retrieved (YYYY-MM-DD)
  relevanceScore: float           # OPTIONAL. 0.0–1.0 confidence/relevance score
  quote: string                   # OPTIONAL. Key supporting quote (max 200 chars)
```

---

### `lastReviewed`

ISO 8601 date of the most recent content review. Should be updated whenever material changes are made.

---

## Prose Body Structure

Below the frontmatter, every entity page must have a prose section following this structure:

```markdown
# [Entity Name]

## Definition

One to three sentences giving a precise, authoritative definition of the entity. 
This should be the grounding statement — what this entity *is*, not what it does or why it matters.

## Description

3–5 paragraphs explaining the entity in depth. Cover:
- How it works mechanically
- When/why it appears or applies
- Its relationship to the broader SERP ecosystem
- Historical context if relevant

## Key Attributes

Prose elaboration of the most important attributes from the frontmatter. 
Write for a reader who has not seen the frontmatter.

## Optimization Relevance

How SEO practitioners interact with or optimize for this entity. 
What can be influenced, what cannot, and what the strategic implications are.

## Relations

Prose description of the most important relationships (subset of frontmatter relations, the ones that need explanation).

## Status & Evolution

Current status, any significant changes, and trajectory. Flag deprecations, restrictions, or emerging behavior.

## Evidence & Sources

Bulleted list of sources (mirrors the `evidence` frontmatter but in readable format).
```

---

## Validation

Validate entity frontmatter against [`schema/entity.schema.json`](schema/entity.schema.json) before submitting.

```bash
# Using ajv-cli
npx ajv validate -s schema/entity.schema.json -d entities/[namespace]/[entityId].md --parseYaml
```

---

## Naming Conventions Summary

| Component | Convention | Example |
|-----------|-----------|---------|
| File name | `entityId.md` | `featured-snippet.md` |
| `entityId` | kebab-case | `featured-snippet` |
| `name` | Title Case | `Featured Snippet` |
| `type` | PascalCase_With_Underscore | `SERP_Feature` |
| `status` | lowercase | `active` |
| `namespace` | kebab-case | `serp-features` |
| `predicate` | SCREAMING_SNAKE_CASE | `IS_TYPE_OF` |

---

## Versioning

The Serponado Standard itself is versioned. The current version is `1.0.0`.

When the standard changes in a backward-incompatible way, the MAJOR version increments and a migration guide is published in `CHANGELOG.md`.

Entity files declare which standard version they conform to via the `version` field in frontmatter — this refers to the entity record version, not the standard version. Standard version is tracked in this file's header.
