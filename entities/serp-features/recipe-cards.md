---
entityId: "recipe-cards"
name: "Recipe Cards"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Recipe Rich Results"
  - "Recipe Rich Snippets"
  - "Recipe Carousel"
sameAs:
  - "https://developers.google.com/search/docs/appearance/structured-data/recipe"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: REQUIRES
    target: "structured-data"
    description: "Recipe schema is required for recipe rich results"
  - predicate: TRIGGERED_BY
    target: "informational"
    description: "Recipe queries are informational with high visual intent"
attributes:
  position: "Dedicated Recipe carousel above organic, or inline rich result"
  trigger_intents: [informational, transactional]
  ctr_impact: high
  schema_required: "Recipe"
  owned_by: "Google"
  introduced: "2011"
  display: "Image, recipe name, ratings, cook time, calorie count, author"
  required_schema_properties:
    - name
    - image
    - author
    - datePublished
    - description
    - recipeIngredient
    - recipeInstructions
  recommended_schema_properties:
    - prepTime
    - cookTime
    - recipeYield
    - nutrition
    - aggregateRating
    - video
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://developers.google.com/search/docs/appearance/structured-data/recipe"
    title: "Recipe Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://moz.com/learn/seo/recipe-schema"
    title: "Recipe Schema Markup"
    publisher: "Moz"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Recipe Cards

## Definition

Recipe Cards are rich result displays for cooking and food content, showing recipe images, ratings, cook times, calorie information, and author attribution in an enhanced format within the SERP. They are powered by `Recipe` structured data and appear as individual rich snippets or within a dedicated Recipe carousel for recipe-dominant queries.

## Description

Recipe Cards are among the highest-CTR rich result types due to the strong visual impact of recipe images combined with key decision-making metadata (time, difficulty, ratings). For food bloggers and recipe sites, Recipe schema implementation is essentially mandatory — unimplemented recipe pages are functionally invisible in competitive recipe SERPs dominated by rich results.

The Recipe carousel feature groups multiple recipe results from different sites (and sometimes multiple recipes from the same site) into a horizontally scrollable row, often appearing above all organic results. This gives highly rated, well-schemed recipes significantly elevated SERP position.

`AggregateRating` nested within `Recipe` schema enables star ratings in search results — the most CTR-impactful enhancement for recipe pages.

## Key Attributes

**Schema Required:** `Recipe` with comprehensive property coverage.

**Visual Impact:** Recipe images in search results are a primary CTR driver.

**Carousel Presence:** Recipes can appear in dedicated Recipe carousels, effectively at position 0–1.

## Optimization Relevance

Complete `Recipe` schema with high-quality images, `AggregateRating`, and `HowToStep`-style structured instructions. Food photography quality directly affects CTR from image-heavy recipe results. Original recipes with unique names and titles are better targets than derivative copies.

## Status & Evolution

**Current Status:** Active — one of the original rich result types.

## Evidence & Sources

- [Recipe Structured Data](https://developers.google.com/search/docs/appearance/structured-data/recipe) — Google Search Central, retrieved 2026-06-09
- [Recipe Schema Markup](https://moz.com/learn/seo/recipe-schema) — Moz, retrieved 2026-06-09
