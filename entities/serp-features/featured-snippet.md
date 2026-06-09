---
entityId: "featured-snippet"
name: "Featured Snippet"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Answer Box"
  - "Position Zero"
  - "Direct Answer"
  - "Quick Answer Box"
sameAs:
  - "https://en.wikipedia.org/wiki/Featured_snippet"
  - "https://developers.google.com/search/docs/appearance/featured-snippets"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: HAS_SUBTYPE
    target: "paragraph-featured-snippet"
    description: "Paragraph format is a subtype"
  - predicate: HAS_SUBTYPE
    target: "list-featured-snippet"
    description: "List format is a subtype"
  - predicate: HAS_SUBTYPE
    target: "table-featured-snippet"
    description: "Table format is a subtype"
  - predicate: TRIGGERED_BY
    target: "informational"
    description: "Primarily triggered by informational queries"
  - predicate: COMPETES_WITH
    target: "knowledge-panel"
    description: "Both occupy top-of-SERP position and answer questions directly"
  - predicate: COMPETES_WITH
    target: "ai-overview"
    description: "AI Overviews have partially displaced Featured Snippets for many query types"
  - predicate: RELATED_TO
    target: "people-also-ask"
    description: "PAA answers use the same extraction mechanism as Featured Snippets"
  - predicate: MEASURED_BY
    target: "featured-snippet-rate"
    description: "Featured Snippet Rate metric tracks ownership across tracked keywords"
attributes:
  position: "Above first organic result (Position 0)"
  trigger_intents:
    - informational
    - how-to
    - definition
    - comparison
    - question
  ctr_impact: variable
  schema_required: null
  owned_by: "Google"
  introduced: "2014"
  subtypes:
    - paragraph
    - list
    - table
    - video
    - accordion
  display: "Extracted content block with source URL and page title"
  opt_out_method: "data-nosnippet attribute or max-snippet:-1 in robots meta"
  mobile_display: true
  desktop_display: true
  zero_click_risk: high
evidence:
  - source: "https://developers.google.com/search/docs/appearance/featured-snippets"
    title: "Featured Snippets and Your Website"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
    quote: "Featured snippets are special boxes where the format of a regular search result is flipped."
  - source: "https://searchengineland.com/google-featured-snippets-353310"
    title: "Google Featured Snippets: A Complete Guide"
    publisher: "Search Engine Land"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Featured Snippet

## Definition

A Featured Snippet is a selected organic search result that Google displays in a special format above all other organic results, extracting a specific passage of content to directly answer a user's query. It occupies what practitioners call "Position 0" — above Position 1 — and displays the answer alongside a link to the source page.

## Description

Featured Snippets represent Google's attempt to answer user queries directly on the SERP without requiring a click. When Google identifies a query that has a clear, answerable form — a question, a definition request, a how-to query — it scans indexed pages and selects a passage that best answers the question, displaying it in a prominently styled box at the top of the SERP.

The mechanism behind Featured Snippets is natural language processing. Google's systems analyze the semantic relationship between a query and all indexed content that ranks well for it. The system identifies passages within those pages that form a coherent, complete answer — a specific paragraph, a list, a table — and extracts that passage for display. Crucially, Featured Snippets are sourced from pages that already rank organically for the query, typically within the top 10 results.

Featured Snippets appear in four primary formats. **Paragraph snippets** are prose text excerpts, usually 40–60 words, suitable for definitions and explanatory answers. **List snippets** display numbered or bulleted lists, ideal for steps, rankings, or enumerable items. **Table snippets** pull tabular data directly from HTML tables or structured content. **Video snippets** embed a YouTube video with a timestamp pointing to the relevant moment in the content.

Introduced around 2014, Featured Snippets have undergone significant evolution. In early 2020, Google stopped showing the source page again as a separate organic result below the snippet (de-duplication). In 2023, the rise of AI Overviews began displacing Featured Snippets for many informational queries, particularly on mobile, though Featured Snippets remain common for precise factual and definitional queries.

The zero-click implication of Featured Snippets is significant: studies show that for some queries, the snippet answers the question so completely that the user does not click through to the source page. The CTR impact therefore varies widely — for branded or reputation-related queries, Featured Snippets can increase CTR; for simple factual queries, they may reduce it substantially.

## Key Attributes

**Position:** Above all organic results at the top of the SERP, before Position 1. On mobile, appears immediately below the search bar and any ads.

**Trigger Conditions:** Question queries ("how to," "what is," "why does"), definition queries ("define," "[term] meaning"), comparison queries ("X vs Y"), process/tutorial queries ("steps to," "how do I"), and numeric queries ("how many," "what percentage"). Not triggered by navigational or purely transactional queries.

**Display Elements:** A content block containing: (1) the extracted text or table, (2) the page title of the source, (3) the source URL, (4) optionally an image. The display varies by format — paragraph snippets show prose text; list snippets show up to 8 items with a "More items" expansion; table snippets reproduce the table structure.

**Search Engine Ownership:** Google. Bing has an analogous feature ("Rich Answers") but with a different selection mechanism.

**Device Availability:** Both desktop and mobile, though the visual prominence differs. On mobile, Featured Snippets often occupy the entire visible screen before scrolling.

**Schema Requirement:** None — Featured Snippets are algorithmically extracted from any indexed content. Structured data is not required, though `HowTo` or `FAQPage` schema can help for specific formats.

## Optimization Relevance

To increase eligibility for Featured Snippets, content should directly answer question-phrased queries with a clear, concise response immediately following the question — typically in an H2 or H3 heading. The ideal paragraph snippet answer is 40–60 words positioned directly beneath a question heading. For list snippets, using proper `<ol>` or `<ul>` HTML markup with clean item labels increases likelihood of extraction. For table snippets, properly formatted HTML `<table>` elements with headers perform best.

Beyond format, ranking in the top 10 for the query is a prerequisite — Google only extracts Featured Snippets from already-ranking pages. Improving organic visibility is therefore the foundational step. Keyword research should target question-phrased variations of target queries.

Google provides no mechanism to opt into Featured Snippets, but publishers can opt out using `<meta name="robots" content="nosnippet">` or `max-snippet:-1` to prevent all snippet display, or the `data-nosnippet` HTML attribute to prevent specific paragraphs from being extracted.

## Relations

- **AI Overview** (`COMPETES_WITH`): AI Overviews have partially displaced Featured Snippets for complex informational queries, appearing above them or replacing them entirely.
- **People Also Ask** (`RELATED_TO`): The PAA answer extraction mechanism is functionally similar to Featured Snippet extraction — both pull relevant passages from indexed pages.
- **Informational Intent** (`TRIGGERED_BY`): Informational queries are the primary trigger; navigational and transactional queries rarely produce Featured Snippets.
- **Knowledge Panel** (`COMPETES_WITH`): For entity-based questions, a Knowledge Panel may appear instead of a Featured Snippet, depending on whether Google has the answer in its Knowledge Graph.

## Status & Evolution

**Current Status:** Active — but with reduced prevalence as AI Overviews expand coverage.

As of 2024–2026, Featured Snippets remain a significant SERP feature but have declined in frequency for queries where AI Overviews now provide generative answers. Google has not deprecated Featured Snippets, and they continue to appear for a wide range of query types. For queries where the AI Overview appears, Featured Snippets are typically suppressed. The strategic value of Featured Snippet optimization therefore depends increasingly on which query types remain outside the AI Overview coverage model.

## Evidence & Sources

- [Featured Snippets and Your Website](https://developers.google.com/search/docs/appearance/featured-snippets) — Google Search Central, retrieved 2026-06-09
- [Google Featured Snippets: A Complete Guide](https://searchengineland.com/google-featured-snippets-353310) — Search Engine Land, retrieved 2026-06-09
