---
entityId: "robots-txt"
name: "robots.txt"
type: Technical_Attribute
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "robots exclusion protocol"
  - "REP"
  - "robot exclusion standard"
  - "/robots.txt"
sameAs:
  - "https://developers.google.com/search/docs/crawling-indexing/robots/intro"
  - "https://en.wikipedia.org/wiki/Robots.txt"
parent: "technical-attribute"
namespace: "technical"
relations:
  - predicate: AFFECTS
    target: "crawlability"
    description: "robots.txt directly controls which URLs Googlebot crawls"
  - predicate: RELATED_TO
    target: "crawl-budget"
    description: "Blocking low-value URLs in robots.txt conserves crawl budget"
  - predicate: RELATED_TO
    target: "indexability"
    description: "robots.txt controls crawling, not indexing — an important distinction"
attributes:
  factor_type: technical
  weight: high
  confirmed_by:
    - "Google Search Central robots.txt documentation"
  location: "Root domain: https://example.com/robots.txt"
  format: "Plain text"
  key_directives:
    - "User-agent: [crawler name or *]"
    - "Disallow: [path]"
    - "Allow: [path]"
    - "Sitemap: [sitemap URL]"
    - "Crawl-delay: [seconds] (not honored by Google)"
  crawl_vs_index_distinction: "robots.txt blocks CRAWLING. A page blocked from crawling can still be INDEXED if linked from external sites."
  googlebot_compliance: "Google honors robots.txt as a mandatory signal, not a hint"
  common_use_cases:
    - "Block low-value URL parameters"
    - "Block internal search result pages"
    - "Block staging/test environments"
    - "Block duplicate content paths"
    - "Block admin/backend paths"
    - "Declare sitemap location"
evidence:
  - source: "https://developers.google.com/search/docs/crawling-indexing/robots/intro"
    title: "Introduction to robots.txt"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://en.wikipedia.org/wiki/Robots.txt"
    title: "robots.txt — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# robots.txt

## Definition

robots.txt is a plain text file placed at the root of a domain (`/robots.txt`) that instructs web crawlers — including Googlebot — which URLs and directories they may or may not crawl. It is the primary crawl control mechanism and the first file Google fetches when discovering a new site.

## Description

robots.txt implements the Robots Exclusion Protocol (REP), a decades-old internet convention that well-behaved web crawlers honor voluntarily. Google treats robots.txt as mandatory — Googlebot will not crawl URLs blocked by valid `Disallow` directives.

The most critical technical distinction about robots.txt: it controls **crawling**, not **indexing**. A URL blocked in robots.txt can still be indexed by Google if it is linked to from external pages that Google can crawl. Google will index the URL's existence (URL + anchor text of incoming links) without being able to crawl its content. To prevent indexing, a `noindex` directive in the page's HTML or HTTP headers is required — but Google cannot read that directive if it cannot crawl the page, creating a catch-22. The correct approach for pages that must not be indexed is to allow crawling but use `noindex`.

The `User-agent` directive specifies which crawler a rule applies to. `*` applies to all crawlers; `Googlebot` applies only to Google's main crawler; `Googlebot-Image` targets only Google's image crawler.

`Crawl-delay` is a directive some crawlers honor to pause between requests — Google does not honor `Crawl-delay` in robots.txt. Crawl rate management for Google is done through Google Search Console's crawl rate settings.

The `Sitemap:` directive in robots.txt declares the location of the site's XML sitemap — the most reliable way to ensure Google discovers it.

## Key Attributes

**Critical Distinction:** Blocks crawling, not indexing. Blocked-from-crawling pages can still be indexed.

**Format:** Plain text, specific syntax. Errors (typos in paths, wrong User-agent names) can cause crawling failures.

**Google's Treatment:** Mandatory — Googlebot strictly honors Disallow directives.

## Status & Evolution

**Current Status:** Active — foundational web standard.

## Evidence & Sources

- [Introduction to robots.txt](https://developers.google.com/search/docs/crawling-indexing/robots/intro) — Google Search Central, retrieved 2026-06-09
- [robots.txt — Wikipedia](https://en.wikipedia.org/wiki/Robots.txt) — Wikipedia, retrieved 2026-06-09
