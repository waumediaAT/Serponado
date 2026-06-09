---
entityId: "video-carousel"
name: "Video Carousel"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Video Pack"
  - "Video Results"
  - "Video Strip"
sameAs:
  - "https://developers.google.com/search/docs/appearance/video"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: TRIGGERED_BY
    target: "visual"
  - predicate: RELATED_TO
    target: "image-pack"
  - predicate: REQUIRES
    target: "structured-data"
    description: "VideoObject schema strongly improves inclusion eligibility"
attributes:
  position: "Variable — often within top 3 organic results for tutorial/how-to queries"
  trigger_intents: [how-to, tutorial, review, entertainment, informational]
  ctr_impact: high
  schema_required: "VideoObject"
  owned_by: "Google"
  introduced: "2007"
  primary_source: "YouTube (dominant), Vimeo, publisher video pages"
  display: "Horizontal carousel of video thumbnails with title, channel, duration, upload date"
  rich_features: ["ClipMarkup", "SeekToAction", "timestamps"]
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://developers.google.com/search/docs/appearance/video"
    title: "Video SEO Best Practices"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://developers.google.com/search/docs/appearance/structured-data/video"
    title: "Video structured data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 0.95
lastReviewed: "2026-06-09"
---

# Video Carousel

## Definition

The Video Carousel is a SERP feature displaying a horizontally scrollable row of video results — primarily from YouTube — embedded within the organic search results for queries where video content is highly relevant. Each card shows a video thumbnail, title, channel name, duration, and publication date.

## Description

The Video Carousel integrates video content into the main SERP without requiring users to switch to the Google Videos tab. It is most commonly triggered for tutorial, review, how-to, and entertainment queries where users frequently find video more useful than text.

YouTube dominates Video Carousel results due to Google's ownership of the platform and YouTube's dominant video search index. However, non-YouTube video pages can appear if they implement `VideoObject` structured data, have strong domain authority, and offer high-quality video content clearly indexed by Googlebot.

Advanced video rich results features — **Clip Markup** (allows Google to show specific key moments within the video as labeled clips beneath the thumbnail) and **SeekToAction** (enables Google to link directly to a specific timestamp when a user clicks) — can make video results significantly more interactive and click-worthy within the carousel.

## Key Attributes

**Position:** Variable — for tutorial, how-to, and entertainment-dominant queries, may appear at position 1–2. For mixed-intent queries, typically mid-page.

**Schema Requirement:** `VideoObject` with `name`, `description`, `thumbnailUrl`, `uploadDate`, `contentUrl` or `embedUrl`. Add `Clip` markup for timestamp key moments.

**Primary Source:** YouTube. Non-YouTube video pages with `VideoObject` schema and high authority can appear but are less common.

## Optimization Relevance

For non-YouTube video: implement `VideoObject` schema, ensure videos are indexable (not behind login), provide transcript content on the page, use descriptive titles and descriptions. For YouTube: standard YouTube SEO — titles, descriptions with keywords, chapters (chapter markers become eligible for Clip markup), transcripts, engagement signals.

## Status & Evolution

**Current Status:** Active.

Video Carousels have evolved with the addition of Clip markup (2020) and SeekToAction support, making individual video moments directly accessible from the SERP. YouTube Shorts have introduced vertical video thumbnail variants in some SERP surfaces.

## Evidence & Sources

- [Video SEO Best Practices](https://developers.google.com/search/docs/appearance/video) — Google Search Central, retrieved 2026-06-09
- [Video structured data](https://developers.google.com/search/docs/appearance/structured-data/video) — Google Search Central, retrieved 2026-06-09
