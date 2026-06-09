# Contributing to Serponado

Thank you for contributing to the Serponado entity repository. This guide explains how to add new entities, update existing ones, and maintain the quality standards that make Serponado a reliable reference.

---

## Before You Contribute

1. Read the [Serponado Entity Standard](STANDARD.md) completely — all entity files must conform to this specification.
2. Check the [Entity Index in README.md](README.md#entity-index) to confirm your entity is not already documented.
3. Validate your planned entity against the JSON Schema: [`schema/entity.schema.json`](schema/entity.schema.json).

---

## Adding a New Entity

### Step 1: Determine the namespace

Choose the most appropriate namespace for your entity:

| Namespace | What belongs here |
|-----------|------------------|
| `serp-features` | Any feature that appears on the SERP |
| `paid-features` | Advertising formats and paid placements |
| `ranking-factors` | Confirmed or strongly evidenced ranking signals |
| `algorithms` | Google algorithm systems and named updates |
| `intent` | Search intent types and query classifications |
| `metrics` | Measurable SEO performance and authority metrics |
| `technical` | Technical SEO attributes and configurations |
| `ai-search` | AI-augmented search features and optimization disciplines |
| `layout` | SERP layout positions and anatomical elements |
| `knowledge-entities` | Entity types and knowledge graph concepts |

### Step 2: Create the entity file

1. Copy [`templates/entity-template.md`](templates/entity-template.md) to `entities/[namespace]/[entityId].md`
2. The filename must exactly match the `entityId` field
3. `entityId` must be globally unique — check `index.json`

### Step 3: Fill in the frontmatter

All required fields per the Standard must be present. Pay particular attention to:

- `entityId` — must be kebab-case, globally unique
- `type` — must match the EntityType enum in `schema/entity.schema.json`
- `status` — be accurate about current deployment state
- `sameAs` — at minimum, a Wikipedia or Google official documentation link
- `relations` — use correct predicates from `schema/relation-predicates.json`
- `attributes` — include all required attributes for the entity type
- `evidence` — minimum 2 citations with source URL, title, and retrieved date
- `lastReviewed` — today's date in ISO 8601 format (YYYY-MM-DD)

### Step 4: Write the prose body

Follow the prose structure from [STANDARD.md](STANDARD.md):

1. **Definition** — Precise, grounding, 1–3 sentences
2. **Description** — 3–5 paragraphs covering mechanism, context, history
3. **Key Attributes** — Prose elaboration of important attributes
4. **Optimization Relevance** — How practitioners interact with this entity
5. **Relations** — Prose explanation of key relationships
6. **Status & Evolution** — Current state and trajectory
7. **Evidence & Sources** — Bulleted citation list

### Step 5: Update the index

1. Add your entity to the appropriate table in `README.md`'s [Entity Index section](README.md#entity-index)
2. Add your entity to `index.json`:

```json
{
  "entityId": "your-entity-id",
  "name": "Your Entity Name",
  "type": "SERP_Feature",
  "namespace": "serp-features",
  "status": "active",
  "file": "entities/serp-features/your-entity-id.md"
}
```

### Step 6: Validate

```bash
# Validate frontmatter against JSON Schema
npx ajv validate -s schema/entity.schema.json -d entities/[namespace]/[entityId].md --parseYaml
```

---

## Updating an Existing Entity

When updating an entity:

1. Update the `lastReviewed` date to today
2. Increment the `version` field (PATCH for corrections, MINOR for additions)
3. If `status` is changing (e.g., `active` → `deprecated`), add a note in the Status & Evolution section explaining when and why
4. Update any related entities' frontmatter if the relationship changed
5. Update `index.json` if status or name changed

---

## Deprecating an Entity

When an entity is deprecated (feature removed, replaced, or no longer relevant):

1. Change `status` to `deprecated`
2. Add a `REPLACED_BY` relation to the successor entity (if one exists)
3. Update the Status & Evolution section with the deprecation date and reason
4. Do NOT delete the file — deprecated entities are preserved for historical reference
5. Add `deprecated: true` to the entity's row in the README index table

---

## Quality Standards

All entity contributions must meet these quality bars:

**Accuracy:** All factual claims must be supported by the `evidence` citations. Do not state things Google does that are speculative without labeling them as such.

**Completeness:** Entity pages should be comprehensive enough to ground an LLM or human reader who knows nothing about the entity.

**Evidence:** At minimum, one primary source (official Google documentation preferred) and one secondary source (reputable SEO publication). Retrieved dates must be accurate.

**Neutrality:** Entity pages describe what things are and how they work — not opinion about whether they are good or bad for SEO. Optimization guidance is factual (this schema enables this feature) not prescriptive.

**Relations:** All `target` values in `relations` must be valid `entityId` values that exist in the repository (or are planned — mark planned targets with a comment).

---

## Relation Predicate Selection Guide

| If you want to say... | Use predicate |
|-----------------------|---------------|
| "This is a type of..." | `IS_TYPE_OF` |
| "This has subtypes..." | `HAS_SUBTYPE` |
| "This needs X to work" | `REQUIRES` |
| "X drives this to appear" | `TRIGGERED_BY` |
| "This drives X to appear" | `TRIGGERS` |
| "This and X fight for space" | `COMPETES_WITH` |
| "This was replaced" | `REPLACED_BY` |
| "This replaced something" | `REPLACES` |
| "This measures X" | `MEASURES` |
| "X runs on top of Y" | `POWERED_BY` |
| "This runs X" | `POWERS` |
| "This affects X's behavior" | `AFFECTS` |
| "Generally related" | `RELATED_TO` |
| "Like X but in different context" | `ANALOGOUS_TO` |

---

## Naming Conventions

- `entityId`: kebab-case (`featured-snippet`, `e-e-a-t`, `rankbrain`)
- `name`: Title Case (`Featured Snippet`, `E-E-A-T`, `RankBrain`)
- Filenames: match `entityId` exactly (`featured-snippet.md`)
- Relations `target`: exact `entityId` of the related entity

---

## Questions

Open an issue to discuss before adding:
- New entity types not covered by existing namespaces
- Significant structural changes to existing entities
- Proposed changes to the Standard itself

For small corrections, a PR with explanation is sufficient.
