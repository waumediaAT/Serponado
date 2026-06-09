---
entityId: "image-pack"
name: "Image Pack"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Google Image Results"
  - "Inline Image Results"
  - "Image Strip"
sameAs:
  - "https://developers.google.com/search/docs/appearance/google-images"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: TRIGGERED_BY
    target: "visual"
    description: "Visual intent queries trigger Image Packs"
  - predicate: RELATED_TO
    target: "video-carousel"
    description: "Both are media-type SERP features triggered by visual intent"
attributes:
  position: "Variable — within top 5 organic positions"
  trigger_intents:
    - visual
    - informational
    - navigational
  ctr_impact: medium
  schema_required: "ImageObject (enhances but not required)"
  owned_by: "Google"
  introduced: "2007"
  display: "Horizontal row of image thumbnails with 'Images' label, clicking opens Google Images"
  mobile_display: true
  desktop_display: true
  links_to: "Google Images vertical search"
evidence:
  - source: "https://developers.google.com/search/docs/appearance/google-images"
    title: "Google Images Best Practices"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://moz.com/learn/seo/google-image-pack"
    title: "What Is Google's Image Pack?"
    publisher: "Moz"
    retrieved: "2026-06-09"
    relevanceScore: 0.85
lastReviewed: "2026-06-09"
---

# Image Pack

## Definition

An Image Pack is a SERP feature consisting of a horizontal row of image thumbnails embedded within the organic search results. It appears for queries where Google determines that visual content is relevant, displaying 3–10 images sourced from Google Images, each linking through to Google Images or directly to the source page.

## Description

Image Packs bring visual search results into the main SERP, bypassing the need for users to navigate to the Google Images tab. They appear as a labeled horizontal strip of thumbnail images within the standard organic results listing, typically labeled "Images" or "Images for [query]."

Google's trigger for Image Packs is primarily **visual intent** — queries about physical appearances, design concepts, products, landmarks, people, infographics, and visual how-to content. The system is probabilistic: Google evaluates the overall query-user-context and decides whether a significant portion of users would benefit from seeing visual results.

Each thumbnail in the Image Pack links to the Google Images view, where the full image appears alongside a link to the source page. This means Image Pack appearances drive traffic to Google Images rather than directly to publisher websites — publishers whose images appear in the pack receive indirect exposure through the subsequent Google Images page.

Image Pack positions within the SERP are variable, appearing anywhere from the top 3 results to below the fold, depending on the query type and estimated visual intent strength. For highly visual queries (celebrity photos, interior design, fashion), Image Packs often appear above the first organic result.

## Key Attributes

**Position:** Variable, embedded within organic results. For strongly visual queries: above the fold, often positions 1–3. For moderately visual queries: mid-page.

**Trigger Conditions:** Physical appearance queries, product images, landmark photos, artwork, infographic topics, recipe photos, fashion, design, nature, animals.

**Display Elements:** Horizontal scroll row of image thumbnails with an "Images" heading. Each thumbnail shows a low-res preview. Clicking navigates to Google Images.

**Schema Requirement:** `ImageObject` schema on image-containing pages can help Google understand image content and context but is not required for Image Pack inclusion — Google's image crawlers process images directly.

**Optimization Signals:** Descriptive file names (e.g., `red-running-shoes-nike.jpg` not `IMG_2341.jpg`), detailed alt text, surrounding page context, image caption, page title and topic alignment, image quality and dimensions.

## Optimization Relevance

Image Pack optimization is primarily Google Images SEO. The foundational signals are: descriptive, keyword-relevant alt text; meaningful file names; high image quality (resolution, clarity); surrounding textual context on the page; and structured data (`ImageObject` with `contentUrl`, `name`, `description`, `author`).

Google's documentation specifically recommends using descriptive alt text that conveys image content to both users and crawlers, creating original high-quality images rather than stock photos, and ensuring fast image loading (modern formats like WebP/AVIF, appropriate dimensions, CDN delivery).

## Status & Evolution

**Current Status:** Active — one of Google's oldest vertical search integration features.

Image Packs have been a SERP fixture since around 2007. The feature has evolved primarily in visual design (more prominent display, touch-friendly carousels on mobile) rather than fundamental behavior. The emergence of AI image analysis capabilities (Google Lens, Multisearch) has made image indexing more sophisticated, but the basic Image Pack format remains stable.

## Evidence & Sources

- [Google Images Best Practices](https://developers.google.com/search/docs/appearance/google-images) — Google Search Central, retrieved 2026-06-09
- [What Is Google's Image Pack?](https://moz.com/learn/seo/google-image-pack) — Moz, retrieved 2026-06-09
