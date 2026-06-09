---
entityId: "structured-data"
name: "Structured Data (JSON-LD)"
type: Technical_Attribute
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Schema Markup"
  - "Schema.org Markup"
  - "JSON-LD"
  - "Microdata"
  - "Rich Data"
  - "Semantic Markup"
sameAs:
  - "https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data"
  - "https://schema.org"
parent: "technical-attribute"
namespace: "technical"
relations:
  - predicate: POWERS
    target: "review-snippets"
    description: "AggregateRating schema powers star rating rich results"
  - predicate: POWERS
    target: "product-rich-results"
    description: "Product schema powers product rich results"
  - predicate: POWERS
    target: "faq-results"
    description: "FAQPage schema powers FAQ rich results (now restricted)"
  - predicate: POWERS
    target: "how-to-results"
    description: "HowTo schema powers how-to rich results"
  - predicate: POWERS
    target: "job-listings"
    description: "JobPosting schema powers job listing results"
  - predicate: POWERS
    target: "recipe-cards"
    description: "Recipe schema powers recipe rich results"
  - predicate: POWERS
    target: "event-listings"
    description: "Event schema powers event rich results"
  - predicate: RELATED_TO
    target: "knowledge-panel"
    description: "Organization/Person schema on official site supports Knowledge Graph"
  - predicate: RELATED_TO
    target: "knowledge-graph"
    description: "Structured data is a primary signal for Knowledge Graph entity association"
attributes:
  factor_type: technical
  weight: high
  confirmed_by:
    - "Google Search Central structured data documentation"
    - "Rich Results Test tool (official)"
  formats:
    - name: "JSON-LD"
      recommendation: "Strongly recommended by Google"
      implementation: "Inline <script> tag in <head> or <body>"
    - name: "Microdata"
      recommendation: "Accepted but not preferred"
      implementation: "HTML attribute-based (itemscope, itemtype, itemprop)"
    - name: "RDFa"
      recommendation: "Accepted but not preferred"
      implementation: "HTML attribute-based"
  vocabulary: "Schema.org"
  key_types:
    - Article
    - NewsArticle
    - Product
    - AggregateRating
    - Review
    - Recipe
    - HowTo
    - FAQPage
    - Event
    - JobPosting
    - LocalBusiness
    - Organization
    - Person
    - WebSite
    - BreadcrumbList
    - VideoObject
    - ImageObject
    - Course
    - SoftwareApplication
    - Book
    - Dataset
    - ClaimReview
    - Speakable
  testing_tools:
    - "Google Rich Results Test (https://search.google.com/test/rich-results)"
    - "Schema Markup Validator (https://validator.schema.org)"
    - "Google Search Console > Enhancements report"
  affects_feature:
    - review-snippets
    - product-rich-results
    - recipe-cards
    - how-to-results
    - job-listings
    - event-listings
    - breadcrumbs
    - sitelinks-searchbox
    - video-carousel
    - knowledge-panel
evidence:
  - source: "https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data"
    title: "Introduction to Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
    quote: "Structured data is a standardized format for providing information about a page and classifying the page content."
  - source: "https://schema.org"
    title: "Schema.org — Full Hierarchy"
    publisher: "Schema.org (W3C Community Group)"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
lastReviewed: "2026-06-09"
---

# Structured Data (JSON-LD)

## Definition

Structured data is machine-readable code added to web pages that explicitly communicates the type and properties of a page's content to search engines. Using the Schema.org vocabulary (recommended in JSON-LD format), it enables Google to understand entities, relationships, and attributes on a page — unlocking rich results, Knowledge Graph associations, and AI grounding.

## Description

Structured data bridges the gap between human-readable web content and machine understanding. While Google's NLP systems (BERT, MUM, Gemini) can infer a lot from unstructured text, structured data provides explicit, unambiguous declarations: "This page contains a `Product` named 'X' with a price of '$Y' and an `AggregateRating` of 4.5 out of 5."

**JSON-LD** is Google's strongly recommended format. It is implemented as an inline `<script type="application/ld+json">` block, typically in the `<head>` of the page. JSON-LD is preferred because it is decoupled from the visual HTML — the same structured data can be added without changing the page's appearance, and it can be dynamically injected by JavaScript (with some caution around Googlebot's JavaScript processing delays).

The Schema.org vocabulary defines the types and properties available. The core `Thing` type has dozens of subtypes covering the full range of real-world entities (Person, Organization, Place, Product, Event, CreativeWork, Action, etc.). Each type has defined properties that can be populated to provide structured context.

Structured data has two primary SEO applications:
1. **Rich Results** — Eligible schema types unlock enhanced visual displays in the SERP (stars, prices, images, FAQs, steps)
2. **Knowledge Graph Entity Association** — `Organization`, `Person`, and `LocalBusiness` schema with `sameAs` links to Wikidata/Wikipedia helps Google connect a website to its Knowledge Graph entity

The Rich Results Test (Google's official tool) validates whether a page's structured data is correctly implemented and eligible for rich results. Google Search Console's "Enhancements" report shows rich result performance and errors at scale.

**Common Implementation Mistakes:**
- Marking up content not visible on the page (spam policy violation)
- Incorrect nesting (e.g., `AggregateRating` outside a valid parent type)
- Outdated prices or availability in `Product` schema
- Using deprecated schema types
- Missing required properties for specific rich result types

## Key Attributes

**Format:** JSON-LD (recommended), Microdata, RDFa

**Vocabulary:** Schema.org (maintained by Google, Microsoft, Yahoo, Yandex consortium)

**Rich Results Eligibility:** Each schema type has specific required and recommended properties to qualify. Google's Rich Results Test shows eligibility per page.

## Optimization Relevance

Priority structured data implementations by impact:
1. `Product` + `AggregateRating` for e-commerce (star ratings = significant CTR lift)
2. `LocalBusiness` for local businesses (supports Local Pack and Knowledge Panel)
3. `Article`/`NewsArticle` for publishers (supports Top Stories eligibility)
4. `Recipe` for food/cooking sites (Recipe carousel visibility)
5. `HowTo` for tutorial content (step display in results)
6. `JobPosting` for job boards (Google for Jobs)
7. `VideoObject` for video pages (Video rich results)
8. `BreadcrumbList` for all multi-level sites (breadcrumb URL display)
9. `WebSite` with `SearchAction` for Sitelinks Searchbox
10. `Organization`/`Person` with `sameAs` for Knowledge Graph entity building

## Status & Evolution

**Current Status:** Active — critically important and expanding.

Structured data's importance has grown continuously since Google formalized rich results in 2011. The expansion of AI Overviews creates a new dimension: structured data as an AI grounding signal — explicit schema declarations may influence which pages are cited in AI-generated answers. Schema.org continues to add new types; notable recent additions include `Speakable` (for voice search), `CovidTestingFacility`, `HealthTopicContent`, and various media types.

## Evidence & Sources

- [Introduction to Structured Data](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data) — Google Search Central, retrieved 2026-06-09
- [Schema.org — Full Hierarchy](https://schema.org) — Schema.org, retrieved 2026-06-09
