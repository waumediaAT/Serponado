---
entityId: "canonical"
name: "Canonical Tag"
type: Technical_Attribute
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "rel=canonical"
  - "Canonical URL"
  - "Canonical Link Element"
  - "Self-Referencing Canonical"
sameAs:
  - "https://developers.google.com/search/docs/crawling-indexing/canonicalization"
  - "https://en.wikipedia.org/wiki/Canonical_link_element"
parent: "technical-attribute"
namespace: "technical"
relations:
  - predicate: RELATED_TO
    target: "indexability"
    description: "Canonical tags direct Google to index the preferred URL version"
  - predicate: RELATED_TO
    target: "crawl-budget"
    description: "Proper canonicalization reduces wasted crawl budget on duplicate content"
  - predicate: RELATED_TO
    target: "hreflang"
    description: "Hreflang tags must self-canonicalize correctly with canonicals for international SEO"
attributes:
  factor_type: technical
  weight: high
  confirmed_by:
    - "Google Search Central canonicalization documentation"
  html_implementation: "<link rel=\"canonical\" href=\"https://example.com/preferred-url\">"
  http_header_implementation: "Link: <https://example.com/preferred-url>; rel=\"canonical\""
  sitemap_implementation: "Only include canonical URLs in XML sitemaps"
  treated_as: "Hint (strong hint) — Google may override if it disagrees"
  use_cases:
    - "URL parameter variations (?sort=price, ?color=red)"
    - "HTTP vs HTTPS duplicates"
    - "www vs non-www duplicates"
    - "Trailing slash vs no trailing slash"
    - "Printer-friendly page versions"
    - "Paginated page series"
    - "Cross-domain content syndication"
    - "Mobile (m.) subdomains"
  self_referencing: "Recommended on every page — canonical pointing to itself"
  cross_domain: "Supported — for content syndicated across multiple domains"
evidence:
  - source: "https://developers.google.com/search/docs/crawling-indexing/canonicalization"
    title: "Canonicalization"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://en.wikipedia.org/wiki/Canonical_link_element"
    title: "Canonical link element — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Canonical Tag

## Definition

The canonical tag (`<link rel="canonical" href="[URL]">`) is an HTML element that signals to search engines which URL is the preferred, authoritative version of a page when duplicate or near-duplicate content exists across multiple URLs. It consolidates ranking signals from all duplicate variants to a single canonical URL.

## Description

Duplicate content is one of the most common technical SEO challenges — the same or very similar content accessible at multiple URLs, caused by URL parameters, protocol variations (HTTP/HTTPS), www/non-www prefixes, trailing slashes, paginated versions, printer-friendly pages, or session IDs.

Without canonical tags, Google must decide independently which version of a page to index, potentially choosing incorrectly or diluting link equity across multiple versions of the same content. The canonical tag provides an explicit directive, consolidating signals.

Canonical tags are treated as a **strong hint** by Google, not an absolute directive. Google may override the canonical if it determines a different URL is the "true" canonical based on other signals (internal linking patterns, sitemap entries, redirects). This behavior means canonical tags must be implemented consistently — if internal links point to one URL and the canonical points to another, Google sees conflicting signals.

**Self-referencing canonicals** — a page with a canonical pointing to its own URL — are recommended on every page as a defensive measure, preventing parameter-appended versions from being interpreted as the canonical.

**Cross-domain canonicals** allow syndicated content to point back to the original source, preventing the syndicated copy from competing in rankings and ensuring the original URL receives all link equity from third-party links to the syndicated version.

## Key Attributes

**Treatment:** Strong hint — Google may override in rare cases.

**Implementation locations:** HTML `<head>`, HTTP response headers (for non-HTML resources), XML sitemaps (should only list canonical URLs).

**Common Mistakes:** Canonical pointing to a redirected URL; canonical in `<body>` instead of `<head>`; paginated pages all canonicalizing to page 1 (prevents page 2+ from indexing); canonical on a noindexed page.

## Status & Evolution

**Current Status:** Active — foundational technical SEO signal.

## Evidence & Sources

- [Canonicalization](https://developers.google.com/search/docs/crawling-indexing/canonicalization) — Google Search Central, retrieved 2026-06-09
- [Canonical link element — Wikipedia](https://en.wikipedia.org/wiki/Canonical_link_element) — Wikipedia, retrieved 2026-06-09
