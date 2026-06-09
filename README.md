# Serponado — The Ultimate SERP Entity Standard

> **The tornado that swept through every corner of the Search Engine Results Page and documented everything it found.**

Serponado is the most comprehensive open entity repository for Search Engine Results Page (SERP) knowledge. It defines, classifies, and cross-references every entity, attribute, feature, signal, metric, and algorithm relevant to the modern SERP ecosystem. Each entity follows the [Serponado Standard](STANDARD.md) — a machine-readable, human-friendly schema designed for AI grounding, SEO tooling, knowledge graph population, and semantic research.

The name **Serponado** is intentional: like a tornado, SERPs are chaotic, dynamic, ever-shifting systems with hundreds of interacting forces — features appearing and disappearing, algorithms rewriting the rules overnight, AI reshaping what a "result" even means. This repository imposes order on that chaos.

---

## Table of Contents

1. [What Is Serponado?](#what-is-Serponado)
2. [The Nado Philosophy](#the-nado-philosophy)
3. [Repository Architecture](#repository-architecture)
4. [Part I — SERP Feature Taxonomy](#part-i--serp-feature-taxonomy)
   - [Organic SERP Features](#organic-serp-features)
   - [Rich Results & Structured Data Features](#rich-results--structured-data-features)
   - [Local SERP Features](#local-serp-features)
   - [Paid / Advertising Features](#paid--advertising-features)
   - [AI-Augmented Features](#ai-augmented-features)
   - [Universal & Vertical Search Features](#universal--vertical-search-features)
   - [Utility & Instant Answer Features](#utility--instant-answer-features)
5. [Part II — SERP Ranking Factors](#part-ii--serp-ranking-factors)
   - [On-Page Ranking Factors](#on-page-ranking-factors)
   - [Off-Page Ranking Factors](#off-page-ranking-factors)
   - [Technical Ranking Factors](#technical-ranking-factors)
   - [User Signal Factors](#user-signal-factors)
   - [Entity & Semantic Factors](#entity--semantic-factors)
6. [Part III — Google Algorithms & Core Updates](#part-iii--google-algorithms--core-updates)
   - [Core Algorithm Components](#core-algorithm-components)
   - [Named Algorithm Updates](#named-algorithm-updates)
   - [Modern Algorithm Systems](#modern-algorithm-systems)
7. [Part IV — Search Intent Framework](#part-iv--search-intent-framework)
8. [Part V — SERP Metrics & Measurement](#part-v--serp-metrics--measurement)
9. [Part VI — Technical SEO Attributes](#part-vi--technical-seo-attributes)
10. [Part VII — AI Search Landscape](#part-vii--ai-search-landscape)
11. [Part VIII — Knowledge Graph & Entity Framework](#part-viii--knowledge-graph--entity-framework)
12. [Part IX — SERP Layout Anatomy](#part-ix--serp-layout-anatomy)
13. [Part X — Serponado Entity Standard](#part-x--Serponado-entity-standard)
14. [Entity Index](#entity-index)
15. [Glossary](#glossary)
16. [Contributing](#contributing)
17. [License](#license)

---

## What Is Serponado?

A **Search Engine Results Page (SERP)** is the page displayed by a search engine in response to a user query. What appears on that page — how it's structured, what features appear, which signals determine ranking, and how results are scored — is the subject of Serponado.

Serponado is not a tool. It is not a plugin. It is a **standard** — an authoritative, versioned, community-maintained entity repository covering every dimension of the SERP universe:

- Every **SERP feature** Google (and other engines) can display
- Every documented **ranking factor** that influences position
- Every major **algorithm and update** that changed the rules
- Every **search intent type** that shapes what Google shows
- Every **metric** used to measure SERP performance
- Every **technical attribute** that affects crawling, indexing, and rendering
- Every **AI search mechanism** reshaping how results are generated
- Every **entity type** that can appear in or relate to a SERP
- Every **layout element** that defines where results appear

Each entity in this repository is a structured Markdown file following the [Serponado Entity Standard](STANDARD.md). Files include YAML frontmatter for machine-readability and rich prose for human understanding. This makes Serponado suitable for:

- **AI grounding** — injecting authoritative SERP context into LLM prompts or RAG pipelines
- **Knowledge graph population** — structured relation predicates enable graph traversal
- **SEO tooling** — enumerate features, factors, and signals programmatically
- **Research & education** — definitive reference for practitioners, academics, and students
- **Disambiguation** — canonical names, aliases, and `sameAs` links to Wikidata/Wikipedia

---

## The Nado Philosophy

A tornado doesn't stop at the obvious landmarks. It sweeps through every field, every back road, every forgotten corner. Serponado applies this same totalizing approach to SERP knowledge.

**The three principles of Serponado:**

1. **Comprehensiveness over curation** — if it exists in a SERP, it belongs here. Deprecated features, obscure rich result types, experimental AI surfaces — all documented.
2. **Structure over prose** — every entity has typed, machine-readable attributes. Relationships are explicit predicates, not implied by narrative.
3. **Grounding over opinion** — entity pages describe what things *are*, not what SEOs *think* about them. Evidence links are mandatory. Speculation is labeled as such.

---

## Repository Architecture

```
Serponado/
├── README.md                          # This file — the exhaustive reference
├── STANDARD.md                        # The Serponado entity page standard
├── CONTRIBUTING.md                    # How to add/edit entities
├── schema/
│   ├── entity.schema.json             # JSON Schema for entity frontmatter validation
│   └── relation-predicates.json       # All valid relation predicate values
├── templates/
│   └── entity-template.md             # Blank entity page template
├── entities/
│   ├── serp-features/                 # All organic & AI SERP features
│   ├── paid-features/                 # Advertising & paid placements
│   ├── ranking-factors/               # Signals that influence position
│   ├── algorithms/                    # Google algorithm systems & updates
│   ├── intent/                        # Search intent types & query classifications
│   ├── metrics/                       # Performance & authority metrics
│   ├── technical/                     # Technical SEO attributes
│   ├── ai-search/                     # AI-augmented search features & GEO
│   ├── layout/                        # SERP layout positions & anatomy
│   └── knowledge-entities/            # Entity types in the knowledge graph
└── index.json                         # Machine-readable master entity index
```

---

## Part I — SERP Feature Taxonomy

A **SERP feature** is any element that appears on a search results page beyond a standard blue-link organic result. Google currently has over 60 distinct SERP features, appearing contextually based on query type, intent, device, location, and user history.

### Organic SERP Features

These features appear in the organic (unpaid) section of the SERP and influence how standard organic results are displayed or supplemented.

---

#### Featured Snippet

**Entity file:** [`entities/serp-features/featured-snippet.md`](entities/serp-features/featured-snippet.md)

A Featured Snippet is a selected search result that appears above the first organic result — sometimes called "Position 0." Google extracts a short piece of content from a web page and displays it directly in the SERP to answer a user's query without requiring a click.

**Subtypes:**
- **Paragraph** — A block of text (typically 40–60 words) answering a question directly.
- **List** — A numbered or bulleted list of steps, items, or categories.
- **Table** — Tabular data extracted from a comparison or data-heavy page.
- **Video** — A YouTube video clip with a timestamp highlighting the answer.
- **Accordion** — An expandable list format (rare, emerging).

**Key attributes:**
- `position`: Above first organic result (Position 0)
- `trigger_intents`: Informational, How-To, Definition, Comparison
- `ctr_impact`: Highly variable — can increase CTR for low-competition queries, but may reduce it for high-volume queries where users read the answer without clicking ("zero-click")
- `ownership_signal`: Google can show content from any indexed page — cannot be "opted in" but can be opted out via `data-nosnippet` or `max-snippet:-1`
- `introduced`: ~2014

**Optimization signals:** Using question-and-answer H2/H3 structure, concise direct-answer paragraphs beneath question headings, structured lists, and table markup increases featured snippet eligibility.

---

#### Knowledge Panel

**Entity file:** [`entities/serp-features/knowledge-panel.md`](entities/serp-features/knowledge-panel.md)

The Knowledge Panel is a large information box that appears on the right-hand side of desktop SERPs (or at the top of mobile SERPs) for entities — people, places, organizations, things — that Google has identified in its Knowledge Graph.

**Key attributes:**
- `source`: Google Knowledge Graph (data from Wikipedia, Wikidata, official websites, and structured data)
- `entity_types_supported`: Person, Organization, Place, Product, Event, Concept, Work
- `appears_for`: Branded, navigational, and entity-based queries
- `claimable_by`: Verified entity owners via Google Search Console
- `sections`: Summary, Images, Key Facts, Social Profiles, Related Entities
- `position`: Right rail (desktop), Top of SERP (mobile)

**Related features:** Knowledge Card (simpler version for well-known facts), Local Knowledge Panel (for local businesses)

---

#### Knowledge Card

**Entity file:** [`entities/serp-features/knowledge-card.md`](entities/serp-features/knowledge-card.md)

A Knowledge Card is a compact factual answer box — simpler than a Knowledge Panel — that provides a direct answer at the top of the SERP. Common for queries seeking a specific fact (population of a city, birth date of a person, height of a mountain).

**Distinction from Featured Snippet:** Knowledge Cards draw from the Knowledge Graph (structured, verified data), while Featured Snippets pull from indexed web pages.

---

#### People Also Ask (PAA)

**Entity file:** [`entities/serp-features/people-also-ask.md`](entities/serp-features/people-also-ask.md)

People Also Ask is an expandable question-and-answer box that displays related questions users commonly search for alongside the current query. Each question, when clicked, expands to reveal an answer sourced from a web page (similar to a Featured Snippet).

**Key attributes:**
- `behavior`: Dynamically expands — clicking one question loads more related questions (potentially infinite)
- `initial_count`: Typically 3–4 questions
- `position`: Variable — often between 1st and 3rd organic result, sometimes below
- `trigger`: Primarily informational and commercial investigation queries
- `ctr_impact`: Mixed — provides brand exposure and featured-snippet-style visibility; can reduce need to click through

**Optimization:** Structured FAQ and Q&A schema, question-based H2/H3 headings, concise answers under each heading.

---

#### Image Pack

**Entity file:** [`entities/serp-features/image-pack.md`](entities/serp-features/image-pack.md)

A horizontal row of image results embedded within the organic SERP. Clicking an image opens Google Images.

**Key attributes:**
- `source`: Google Images index
- `trigger_intents`: Visual, Navigational, Informational
- `position`: Variable — typically within top 5 organic results
- `optimization_signals`: Alt text, file name, surrounding page context, structured data (ImageObject)

---

#### Video Carousel

**Entity file:** [`entities/serp-features/video-carousel.md`](entities/serp-features/video-carousel.md)

A horizontally scrollable row of video results, typically from YouTube, appearing within the SERP. Shows video thumbnails, titles, duration, uploader, and publication date.

**Key attributes:**
- `primary_source`: YouTube (dominant), but also Vimeo, Dailymotion, and publisher sites with VideoObject schema
- `rich_result_signals`: VideoObject schema, thumbnails, duration, clip markup, SeekToAction markup
- `trigger_intents`: How-to, Tutorial, Review, Entertainment, News

---

#### News Box / Top Stories

**Entity file:** [`entities/serp-features/news-box.md`](entities/serp-features/news-box.md)

A carousel or list of recent news articles from Google News-indexed publishers. Appears at the top of the SERP for timely, news-related queries.

**Key attributes:**
- `eligibility`: Requires Google News publisher approval (or AMP/Web Stories in some regions)
- `freshness_weight`: Extremely high — recency is a primary ranking signal
- `displays`: Headline, source, publication time, thumbnail
- `structured_data`: NewsArticle schema, Article schema
- `temporal_trigger`: Breaking news, current events, named events, recent announcements

---

#### Sitelinks

**Entity file:** [`entities/serp-features/sitelinks.md`](entities/serp-features/sitelinks.md)

Sitelinks are sub-page links displayed beneath the main organic result for branded or navigational queries. They help users navigate directly to specific sections of a site.

**Subtypes:**
- **Sitelinks (standard)** — Up to 6 sub-links with brief descriptions
- **Sitelinks (one-line)** — Compact version showing 2–4 links in a single row
- **Sitelinks Search Box** — Embeds a site-specific search field in the result (requires `WebSite` schema with `SearchAction`)

**Key attributes:**
- `trigger`: Branded/navigational queries where Google has high confidence in the user's target destination
- `control`: Cannot be manually added; Google automatically generates them. Demoting is no longer possible (deprecated in 2016)
- `optimization_signals`: Clear site architecture, strong internal linking, descriptive anchor text, `WebSite` schema

---

#### Related Searches

**Entity file:** [`entities/serp-features/related-searches.md`](entities/serp-features/related-searches.md)

A box appearing at the bottom of the SERP (and sometimes mid-SERP) showing 6–8 related queries. Helps users refine or expand their search.

**Key attributes:**
- `position`: Bottom of SERP (primary), occasionally mid-SERP
- `source`: Google's query association graph / search co-occurrence data
- `SEO_value`: Research tool for identifying related topics and semantic clusters

---

#### People Also Search For (PASF)

**Entity file:** [`entities/serp-features/people-also-search-for.md`](entities/serp-features/people-also-search-for.md)

A feature that appears when a user clicks a search result and then returns to the SERP (back-click behavior). Shows alternative sites users also visited for the same query.

**Key attributes:**
- `trigger`: User back-clicks from an organic result
- `implication`: Strong signal for search dissatisfaction — appearing in PASF for a competitor means users didn't find what they needed there
- `SEO_value`: Competitor research, understanding co-search relationships

---

#### Perspectives / Forum Results

**Entity file:** [`entities/serp-features/perspectives.md`](entities/serp-features/perspectives.md)

Introduced in 2023, Perspectives is a SERP feature surfacing content from forums, social media, and discussion platforms (Reddit, Quora, Stack Exchange, TikTok, YouTube comments) for first-person experience queries.

**Key attributes:**
- `source_types`: Reddit, Quora, Stack Exchange, TikTok, YouTube, personal blogs, forums
- `trigger`: Queries seeking personal experience, recommendations, opinions
- `related_update`: Helpful Content Update's emphasis on first-hand experience (E-E-A-T "Experience" signal)
- `display`: Carousel or list of discussion thread excerpts

---

#### Web Stories

**Entity file:** [`entities/serp-features/web-stories.md`](entities/serp-features/web-stories.md)

Visual story content built with the AMP Stories format (Google Web Stories), displayed as a tappable story carousel in search results.

**Key attributes:**
- `format`: AMP Stories (HTML-based, mobile-first, fullscreen)
- `position`: Typically at top of mobile SERP for visual/entertainment queries
- `optimization_tool`: Google Web Stories WordPress plugin, Web Stories editor

---

#### Review Snippets

**Entity file:** [`entities/serp-features/review-snippets.md`](entities/serp-features/review-snippets.md)

Star ratings and review count displayed beneath an organic result's URL. Powered by structured data markup.

**Key attributes:**
- `schema_types`: `Product`, `Recipe`, `Movie`, `Book`, `Software`, `LocalBusiness`, `Course`, `Event`
- `prohibited_types`: Self-serving reviews on your own site (Google's quality guidelines prohibit schema abuse)
- `display`: Star rating (1–5), numeric score, review count
- `impact_on_ctr`: Significantly increases CTR — strong visual signal in competitive SERPs

---

#### FAQ Results

**Entity file:** [`entities/serp-features/faq-results.md`](entities/serp-features/faq-results.md)

Expandable question-and-answer accordion below a standard organic result, powered by `FAQPage` structured data.

**Key attributes:**
- `schema_required`: `FAQPage` with `Question` and `Answer` markup
- `status_note`: Google restricted FAQ rich results in August 2023 — now only shown for government and health sites
- `display`: Expandable list of Q&A pairs beneath the organic result

---

#### How-To Results

**Entity file:** [`entities/serp-features/how-to-results.md`](entities/serp-features/how-to-results.md)

Step-by-step instruction results powered by `HowTo` structured data. Displays numbered steps, images, duration, and tools required.

**Key attributes:**
- `schema_required`: `HowTo` with `HowToStep` items
- `display`: Numbered steps, optional images per step, total time, tools/materials
- `trigger`: Procedural, instructional, "how to" queries
- `mobile_rich`: More prominent on mobile

---

#### Job Listings

**Entity file:** [`entities/serp-features/job-listings.md`](entities/serp-features/job-listings.md)

A rich result box displaying job postings directly on the SERP, aggregated from employer websites that implement `JobPosting` structured data.

**Key attributes:**
- `schema_required`: `JobPosting` with title, description, datePosted, hiringOrganization, jobLocation, baseSalary
- `aggregation`: Feeds into Google for Jobs vertical
- `display`: Job title, company, location, salary range, posting date, apply button

---

#### Event Listings

**Entity file:** [`entities/serp-features/event-listings.md`](entities/serp-features/event-listings.md)

Structured event information displayed inline in the SERP for event-related queries.

**Key attributes:**
- `schema_required`: `Event` with name, startDate, location (or `VirtualLocation` for online events), url, organizer
- `display`: Event name, date/time, location, ticket link
- `subtypes`: In-person events, Online/Virtual events (added 2020)

---

#### Recipe Cards

**Entity file:** [`entities/serp-features/recipe-cards.md`](entities/serp-features/recipe-cards.md)

Rich recipe results showing cooking details, ratings, and images inline in the SERP — often displayed as a carousel.

**Key attributes:**
- `schema_required`: `Recipe` with name, image, author, datePublished, description, prepTime, cookTime, recipeYield, nutrition, recipeIngredient, recipeInstructions, aggregateRating
- `display`: Image, title, ratings, cook time, calorie count, ingredient count
- `position`: Often a dedicated "Recipes" carousel above standard organic results

---

#### Product Rich Results

**Entity file:** [`entities/serp-features/product-rich-results.md`](entities/serp-features/product-rich-results.md)

Enhanced product information displayed in organic results, including price, availability, ratings, and merchant information.

**Key attributes:**
- `schema_required`: `Product` with offers (price, availability, seller), aggregateRating
- `display`: Product name, price, availability, star ratings, merchant name
- `distinction_from_shopping_ads`: Organic, not paid — but competes with Shopping Ads in the SERP

---

#### Book Results

**Entity file:** [`entities/serp-features/book-results.md`](entities/serp-features/book-results.md)

Book-specific results showing cover images, authors, ratings, and purchase links for book-related queries.

**Key attributes:**
- `schema_required`: `Book` with author, isbn, numberOfPages, publisher, aggregateRating
- `source`: Google Books integration, `Book` schema on publisher sites

---

#### App Results

**Entity file:** [`entities/serp-features/app-results.md`](entities/serp-features/app-results.md)

Mobile application results from Google Play Store and Apple App Store displayed in search results.

**Key attributes:**
- `schema_required`: `SoftwareApplication` or `MobileApplication`
- `displays`: App icon, name, rating, number of reviews, operating system, price
- `primary_trigger`: App name queries, "best [category] app" queries

---

#### Podcast Results

**Entity file:** [`entities/serp-features/podcast-results.md`](entities/serp-features/podcast-results.md)

Podcast episode results shown for podcast-related queries, often linking directly to Google Podcasts or the publisher's feed.

**Key attributes:**
- `schema_required`: Podcast RSS feed with proper metadata; `PodcastSeries` / `PodcastEpisode` schema
- `displays`: Show artwork, episode title, description, duration, publish date

---

#### Course Results

**Entity file:** [`entities/serp-features/course-results.md`](entities/serp-features/course-results.md)

Online course listings appearing in search results for educational and skill-based queries.

**Key attributes:**
- `schema_required`: `Course` with name, description, provider, url, coursePrerequisites, offers
- `displays`: Course title, provider, description, price, duration

---

### Rich Results & Structured Data Features

---

#### Breadcrumb Trail

**Entity file:** [`entities/serp-features/breadcrumbs.md`](entities/serp-features/breadcrumbs.md)

A hierarchical navigation path displayed beneath the URL in an organic result, showing the page's location within the site structure.

**Key attributes:**
- `schema_required`: `BreadcrumbList` with `ListItem` elements (or HTML breadcrumb navigation)
- `display`: Home > Category > Subcategory > Page Name
- `seo_impact`: Improves crawlability understanding, enhances URL display, can improve CTR

---

#### Merchant Listings (Free Product Listings)

**Entity file:** [`entities/serp-features/merchant-listings.md`](entities/serp-features/merchant-listings.md)

Free product listings in Google Shopping that appear in the Shopping tab and sometimes main SERP. Introduced in 2020 when Google opened Shopping to free listings.

**Key attributes:**
- `requirement`: Google Merchant Center account + product feed
- `display`: Product image, title, price, merchant name, rating

---

#### Dataset Rich Results

**Entity file:** [`entities/serp-features/dataset-results.md`](entities/serp-features/dataset-results.md)

Research dataset results powered by `Dataset` schema, surfacing data sets in search results for researchers and data consumers.

**Key attributes:**
- `schema_required`: `Dataset` with name, description, url, keywords, license, creator, distribution
- `appears_in`: Google Dataset Search, main SERP for data-specific queries

---

#### Fact Check Labels

**Entity file:** [`entities/serp-features/fact-check-labels.md`](entities/serp-features/fact-check-labels.md)

Labels displaying the result of third-party fact checks on news articles and claims, shown beneath news results.

**Key attributes:**
- `schema_required`: `ClaimReview` schema
- `eligible_publishers`: Fact-checking organizations listed at ClaimReview sources
- `display`: "Checked by [Organization]: [Rating]" label beneath news snippet

---

#### Author/Byline Information

**Entity file:** [`entities/serp-features/author-information.md`](entities/serp-features/author-information.md)

Author name, photo, and credentials displayed in search results for articles and content, tied to E-E-A-T author entity establishment.

**Key attributes:**
- `schema_required`: `Article` or `NewsArticle` with `author` (linking to `Person` schema)
- `e_e_a_t_signal`: Author entity recognition increases content trustworthiness
- `optimization`: Author bio pages, social profile links, Google author entities via Knowledge Graph

---

### Local SERP Features

---

#### Local Pack (Map Pack / 3-Pack)

**Entity file:** [`entities/serp-features/local-pack.md`](entities/serp-features/local-pack.md)

The Local Pack is a SERP feature displaying a Google Maps embed with 3 local business listings for location-based queries. Previously showed 7 results ("7-Pack"), consolidated to 3 in 2015.

**Key attributes:**
- `result_count`: 3 (formerly 7)
- `trigger_intents`: Local intent, "near me" queries, location-modified queries
- `data_source`: Google Business Profile (formerly Google My Business)
- `ranking_factors`:
  - Relevance (how well the listing matches the query)
  - Distance (proximity of the business to the searcher)
  - Prominence (online and offline reputation, reviews, links)
- `display`: Map embed, business name, category, rating, review count, address, hours, click-to-call

---

#### Local Finder

**Entity file:** [`entities/serp-features/local-finder.md`](entities/serp-features/local-finder.md)

The expanded view of the Local Pack, accessible by clicking "More places." Shows more than 3 results with detailed filtering options.

---

#### Local Knowledge Panel

**Entity file:** [`entities/serp-features/local-knowledge-panel.md`](entities/serp-features/local-knowledge-panel.md)

A Knowledge Panel specifically for local businesses, showing business hours, address, phone number, website, reviews, photos, and Q&A.

**Key attributes:**
- `data_source`: Google Business Profile
- `user_features`: Q&A, reviews, photos, suggested edits
- `owner_features`: Posts, offers, booking links, messaging

---

#### Google Business Profile (GBP)

**Entity file:** [`entities/serp-features/google-business-profile.md`](entities/serp-features/google-business-profile.md)

The free business listing product from Google that powers Local Pack and Local Knowledge Panel appearances. Formerly Google My Business (GMB), rebranded in 2021.

**Key attributes:**
- `eligibility`: Physical locations, service-area businesses, hybrid businesses
- `features`: Posts, Q&A, reviews, photos, products, services, booking, menu
- `verification_methods`: Postcard, phone, email, video, instant (for some categories)

---

### Paid / Advertising Features

---

#### Text Ads (Responsive Search Ads / RSA)

**Entity file:** [`entities/paid-features/text-ads.md`](entities/paid-features/text-ads.md)

The primary Google Ads format — text-based advertisements appearing at the top and bottom of the SERP, marked with an "Ad" or "Sponsored" label. Google Ads replaced Expanded Text Ads (ETAs) with Responsive Search Ads (RSAs) as the default in 2022.

**Key attributes:**
- `format`: RSA — up to 15 headlines (3 shown), 4 descriptions (2 shown), 2 final URLs
- `position`: Top (above organic, up to 3–4 ads) and Bottom (below organic, up to 3 ads)
- `auction_mechanism`: Second-price auction based on Quality Score × Max CPC bid = Ad Rank
- `quality_score_components`: Expected CTR, Ad Relevance, Landing Page Experience
- `ad_extensions` (now called Assets): Sitelinks, Callouts, Structured Snippets, Call, Location, Price, Promotion, Image, Lead Form

---

#### Shopping Ads (Product Listing Ads / PLAs)

**Entity file:** [`entities/paid-features/shopping-ads.md`](entities/paid-features/shopping-ads.md)

Visual product advertisements showing images, prices, merchant names, and ratings at the top of SERPs for commercial/transactional queries.

**Key attributes:**
- `requirement`: Google Merchant Center product feed + Google Ads campaign (Performance Max or Shopping)
- `display`: Product image, title, price, merchant name, shipping info, star rating
- `position`: Prominent placement at top of SERP, Shopping tab
- `bidding`: CPC (Cost Per Click), with Smart Bidding options (tROAS, Maximize Conversion Value)

---

#### Local Service Ads (LSAs)

**Entity file:** [`entities/paid-features/local-service-ads.md`](entities/paid-features/local-service-ads.md)

Pay-per-lead ads for local service businesses (plumbers, electricians, lawyers, etc.) appearing at the very top of SERPs above standard text ads.

**Key attributes:**
- `billing_model`: Pay-per-lead (not pay-per-click)
- `verification`: Google Guarantee / Google Screened badge — background checks required
- `categories`: Home services, Professional services (legal, financial, healthcare)
- `display`: Business name, Google Guarantee badge, rating, phone number, hours

---

#### Dynamic Search Ads (DSAs)

**Entity file:** [`entities/paid-features/dynamic-search-ads.md`](entities/paid-features/dynamic-search-ads.md)

Ads where headlines and landing pages are automatically generated by Google from website content, targeting queries not covered by keyword lists.

---

#### Performance Max (PMax)

**Entity file:** [`entities/paid-features/performance-max.md`](entities/paid-features/performance-max.md)

Google's fully automated, goal-based campaign type that serves ads across all Google surfaces — Search, Shopping, Display, YouTube, Gmail, Maps — from a single campaign using asset groups and audience signals.

---

#### Call-Only Ads

**Entity file:** [`entities/paid-features/call-only-ads.md`](entities/paid-features/call-only-ads.md)

Mobile-specific ads designed exclusively to drive phone calls — clicking the ad initiates a call rather than visiting a website.

---

### AI-Augmented Features

---

#### AI Overview (formerly SGE — Search Generative Experience)

**Entity file:** [`entities/ai-search/ai-overview.md`](entities/ai-search/ai-overview.md)

Google's AI-generated answer appearing above organic results for many queries, powered by Gemini. Launched as Search Generative Experience (SGE) in May 2023, rebranded as AI Overviews and rolled out globally in May 2024.

**Key attributes:**
- `powered_by`: Google Gemini
- `position`: Top of SERP, above all organic and paid results
- `display`: Generative paragraph answer with inline citation chips, expandable sources panel
- `citation_sources`: Links to web pages that informed the answer
- `trigger_queries`: Informational, multi-step research, comparison, how-to queries
- `zero_click_risk`: High — comprehensive answers may eliminate click need
- `opt_out`: Users can turn off AI Overviews per query with "Web" filter
- `ctr_to_cited_sources`: Studies show varied results — some sources see traffic increase from citation, others see decrease

---

#### Perspectives (AI-era)

**Entity file:** [`entities/ai-search/perspectives.md`](entities/ai-search/perspectives.md)

Surfaces first-person experiences, discussions, and forum content alongside AI overviews to provide human perspective alongside AI-generated summaries.

---

### Universal & Vertical Search Features

---

#### Flights Box

**Entity file:** [`entities/serp-features/flights-box.md`](entities/serp-features/flights-box.md)

Interactive flight search widget embedded in the SERP for flight-related queries, powered by Google Flights.

---

#### Hotels Pack

**Entity file:** [`entities/serp-features/hotels-pack.md`](entities/serp-features/hotels-pack.md)

Hotel search results with pricing, availability, ratings, and booking links for hotel and accommodation queries.

---

#### Sports Scores

**Entity file:** [`entities/serp-features/sports-scores.md`](entities/serp-features/sports-scores.md)

Live and recent sports scores, fixtures, and standings displayed directly in the SERP for team, league, and match queries.

---

#### Finance Box / Stock Panel

**Entity file:** [`entities/serp-features/finance-box.md`](entities/serp-features/finance-box.md)

Live stock prices, charts, financial data, and company overviews for financial queries, powered by Google Finance.

---

### Utility & Instant Answer Features

---

#### Weather Box

**Entity file:** [`entities/serp-features/weather-box.md`](entities/serp-features/weather-box.md)

Current weather conditions and forecasts displayed directly in the SERP for weather queries.

---

#### Calculator

**Entity file:** [`entities/serp-features/calculator.md`](entities/serp-features/calculator.md)

An interactive calculator widget embedded in the SERP for mathematical expression queries.

---

#### Definition Box

**Entity file:** [`entities/serp-features/definition-box.md`](entities/serp-features/definition-box.md)

Dictionary definition, pronunciation guide, word origin, and synonyms displayed for "define [word]" or "[word] meaning" queries.

---

#### Translation Box

**Entity file:** [`entities/serp-features/translation-box.md`](entities/serp-features/translation-box.md)

Google Translate widget embedded in the SERP for translation queries.

---

#### Unit Converter

**Entity file:** [`entities/serp-features/unit-converter.md`](entities/serp-features/unit-converter.md)

Interactive conversion tool for units of measurement (length, weight, temperature, currency, etc.).

---

#### Time Zone Converter

**Entity file:** [`entities/serp-features/time-zone-converter.md`](entities/serp-features/time-zone-converter.md)

Current time display and conversion tool for time zone queries.

---

## Part II — SERP Ranking Factors

Ranking factors are the signals that Google's algorithms use to determine the relevance, authority, quality, and trustworthiness of a web page — and therefore its position in the SERP.

Google has stated it uses "hundreds" of signals. The factors documented here represent the most well-documented, confirmed, or strongly corroborated signals.

### On-Page Ranking Factors

---

#### E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness)

**Entity file:** [`entities/ranking-factors/e-e-a-t.md`](entities/ranking-factors/e-e-a-t.md)

E-E-A-T is Google's quality evaluation framework, used primarily by Search Quality Raters to assess content quality. Originally E-A-T (without "Experience"), the first "E" for Experience was added in December 2022.

**Components:**
- **Experience** — Does the author have first-hand or life experience with the topic?
- **Expertise** — Does the author have formal or demonstrated knowledge/skills?
- **Authoritativeness** — Is the author or site recognized as an authority in its field by others?
- **Trustworthiness** — Is the site/page honest, transparent, accurate, and safe?

**YMYL (Your Money Your Life):** E-E-A-T standards are highest for content that can impact health, financial stability, safety, or society.

**Signals:**
- Author bio pages with credentials
- Author Knowledge Graph entity
- About page with organization history
- Editorial policies and corrections pages
- Contact information and physical address
- Expertise verified by backlinks from authoritative sources
- Awards, certifications, press coverage

---

#### Content Relevance

**Entity file:** [`entities/ranking-factors/content-relevance.md`](entities/ranking-factors/content-relevance.md)

How well the content of a page semantically matches the user's query intent, including keyword usage, topic coverage, semantic depth, and entity coverage.

**Signals:**
- Primary keyword usage in title, H1, first 100 words
- Semantic keyword coverage (related terms, entities, concepts)
- NLP-derived topical alignment (via BERT, MUM)
- Content completeness relative to top-ranking competitors
- Entity mentions and co-occurrence patterns

---

#### Content Quality

**Entity file:** [`entities/ranking-factors/content-quality.md`](entities/ranking-factors/content-quality.md)

Google's assessment of whether content is genuinely helpful, original, and created primarily for humans rather than search engines.

**Post-Helpful Content Update signals:**
- Does content provide original analysis, reporting, or synthesis?
- Does it demonstrate first-hand experience?
- Is the primary purpose to help users, or to rank?
- Is there a well-established author/site identity?
- Does the content answer the question comprehensively?

---

#### Content Freshness / Recency

**Entity file:** [`entities/ranking-factors/content-freshness.md`](entities/ranking-factors/content-freshness.md)

The impact of publication date and content update frequency on rankings, particularly for time-sensitive queries.

**Query Deserves Freshness (QDF):** Google identifies queries where freshness matters (news, trends, evolving topics) and boosts recently published or updated content.

**Signals:**
- Original publication date
- Last significant modification date
- Update frequency patterns
- New content additions vs. minor edits
- Freshness of links pointing to the page

---

#### Title Tag

**Entity file:** [`entities/ranking-factors/title-tag.md`](entities/ranking-factors/title-tag.md)

The HTML `<title>` element is a critical on-page signal, displayed as the clickable headline in SERP results. Google may rewrite titles that are misleading, too long, or keyword-stuffed.

**Best practices:**
- 50–60 characters
- Primary keyword near the beginning
- Brand name at the end (for non-home pages)
- Unique per page
- Accurately describes page content

---

#### Meta Description

**Entity file:** [`entities/ranking-factors/meta-description.md`](entities/ranking-factors/meta-description.md)

The HTML `<meta name="description">` tag. Not a direct ranking signal, but influences CTR — the snippet Google shows beneath the title.

**Key attributes:**
- `ranking_factor`: Indirect (via CTR impact)
- `length`: 150–160 characters
- `google_rewrite_rate`: ~70% of the time Google rewrites meta descriptions
- `best_practice`: Include primary keyword, compelling call to action, accurate content summary

---

#### H1 and Heading Structure

**Entity file:** [`entities/ranking-factors/heading-structure.md`](entities/ranking-factors/heading-structure.md)

Proper use of H1–H6 heading tags for content structure and topical signal reinforcement.

**Signals:**
- H1 should match or closely align with the title tag
- H2s signal primary subtopics
- H3s signal sub-subtopics
- Question-phrased H2/H3s increase PAA and Featured Snippet eligibility

---

#### Internal Linking

**Entity file:** [`entities/ranking-factors/internal-linking.md`](entities/ranking-factors/internal-linking.md)

The practice of linking between pages within the same domain, distributing PageRank, establishing topical authority clusters, and improving crawlability.

**Key attributes:**
- `pagerank_distribution`: Links pass PageRank (link equity) internally
- `topical_relevance`: Linking topically related pages signals subject matter depth
- `crawl_efficiency`: Ensures all important pages are discoverable by Google's crawler
- `anchor_text`: Descriptive anchor text reinforces topical relevance of the linked page

---

#### URL Structure

**Entity file:** [`entities/ranking-factors/url-structure.md`](entities/ranking-factors/url-structure.md)

The format and content of a page's URL as a relevance and usability signal.

**Best practices:**
- Short, descriptive, keyword-relevant
- Lowercase with hyphens (not underscores)
- Logical hierarchy reflecting site structure
- No unnecessary parameters or session IDs

---

### Off-Page Ranking Factors

---

#### Backlink Profile

**Entity file:** [`entities/ranking-factors/backlinks.md`](entities/ranking-factors/backlinks.md)

The collective set of external links pointing to a domain or page. Google's original core ranking insight (PageRank) is based on the premise that a link from one page to another is a vote of confidence.

**Key quality signals:**
- **Link Authority** — The authority of the linking page/domain
- **Topical Relevance** — Does the linking page cover related topics?
- **Link Diversity** — Wide variety of linking root domains
- **Anchor Text Distribution** — Natural mix of branded, exact-match, partial-match, generic anchors
- **Link Placement** — Editorial (in-content) links outweigh footer/sidebar links
- **Follow vs. Nofollow** — `dofollow` links pass equity; `nofollow`, `ugc`, `sponsored` do not (but may still be seen as signals)
- **Link Velocity** — Rate of link acquisition; sudden spikes can trigger algorithmic scrutiny

---

#### PageRank

**Entity file:** [`entities/ranking-factors/pagerank.md`](entities/ranking-factors/pagerank.md)

Google's foundational link-based ranking algorithm, introduced by Larry Page and Sergey Brin in 1998. Assigns a relative importance score to each web page based on the number and quality of links pointing to it.

**Key attributes:**
- `formula_basis`: Recursive — a page's PageRank depends on the PageRank of pages linking to it
- `public_metric`: Google stopped showing public PageRank in 2016 (Toolbar PageRank discontinued)
- `third_party_proxies`: Domain Rating (Ahrefs), Domain Authority (Moz), Trust Flow (Majestic)
- `internal_distribution`: PageRank flows through internal links — site architecture affects it

---

#### Domain Authority Signals

**Entity file:** [`entities/ranking-factors/domain-authority.md`](entities/ranking-factors/domain-authority.md)

The aggregate authority and trust of an entire domain, influencing how much weight individual pages inherit.

**Contributing factors:** Total linking root domains, quality of links, brand mentions, Knowledge Graph entity status, age of domain, content consistency, historical spam history.

---

#### Brand Signals

**Entity file:** [`entities/ranking-factors/brand-signals.md`](entities/ranking-factors/brand-signals.md)

Signals indicating that a domain represents a real, recognized brand — a key component of modern Google ranking trust.

**Signals:**
- Branded search volume and CTR
- Google Knowledge Panel existence
- Social media presence and verification
- Press coverage and citations
- Co-occurrence with industry terms in text (without links)
- Direct traffic patterns
- App presence and ratings

---

### Technical Ranking Factors

---

#### Core Web Vitals

**Entity file:** [`entities/ranking-factors/core-web-vitals.md`](entities/ranking-factors/core-web-vitals.md)

Google's set of user experience metrics measuring loading performance, interactivity, and visual stability. Became an official Google ranking factor in June 2021 via the Page Experience Update.

**Current metrics:**
- **LCP (Largest Contentful Paint)** — Loading performance. Target: < 2.5 seconds. Measures time to render the largest visible content element.
- **INP (Interaction to Next Paint)** — Interactivity. Target: < 200 ms. Replaced FID (First Input Delay) in March 2024. Measures all user interactions, not just the first.
- **CLS (Cumulative Layout Shift)** — Visual stability. Target: < 0.1. Measures unexpected layout shifts during page load.

**Supporting metrics (not CWV but related):**
- FCP (First Contentful Paint) — first element painted
- TTFB (Time to First Byte) — server response time
- FID (First Input Delay) — now replaced by INP

---

#### Mobile-Friendliness / Mobile-First Indexing

**Entity file:** [`entities/ranking-factors/mobile-first-indexing.md`](entities/ranking-factors/mobile-first-indexing.md)

Since 2019, Google uses the mobile version of a page as the primary version for indexing and ranking. Sites without a mobile-friendly design are penalized.

**Key attributes:**
- `status`: All new sites mobile-first by default since 2020; legacy sites migrated by 2023
- `requirements`: Responsive design, equivalent content on mobile and desktop, no mobile-specific blocked resources, properly sized tap targets

---

#### Page Speed

**Entity file:** [`entities/ranking-factors/page-speed.md`](entities/ranking-factors/page-speed.md)

Page loading speed as a ranking factor. Became an official factor for desktop in 2010 and mobile in 2018 (Speed Update).

**Key signals:** Server response time (TTFB), render-blocking resources, image optimization, caching, CDN usage, minification of CSS/JS.

---

#### HTTPS / SSL

**Entity file:** [`entities/ranking-factors/https-ssl.md`](entities/ranking-factors/https-ssl.md)

Use of HTTPS (via SSL/TLS certificate) as a lightweight ranking signal since 2014. Sites without HTTPS receive browser security warnings, which negatively impacts CTR and trust.

---

#### Structured Data / Schema Markup

**Entity file:** [`entities/ranking-factors/structured-data.md`](entities/ranking-factors/structured-data.md)

Machine-readable markup using Schema.org vocabulary (JSON-LD recommended) that helps Google understand page content and enables rich results.

**Formats:** JSON-LD (recommended), Microdata, RDFa
**Key schema types for SERP features:** Article, Product, Recipe, HowTo, FAQPage, Event, JobPosting, BreadcrumbList, VideoObject, LocalBusiness, Organization, Person, WebSite

---

### User Signal Factors

---

#### Click-Through Rate (CTR)

**Entity file:** [`entities/metrics/ctr.md`](entities/metrics/ctr.md)

The percentage of impressions that result in a click. While Google has denied CTR as a direct ranking factor, leaked documents (2024 Google API leak) suggested "navBoost" uses click data, and RankBrain is known to use engagement signals.

**Formula:** CTR = (Clicks ÷ Impressions) × 100

---

#### Dwell Time

**Entity file:** [`entities/metrics/dwell-time.md`](entities/metrics/dwell-time.md)

The time between a user clicking a search result and returning to the SERP. Longer dwell time suggests user satisfaction with the content. (Note: Google has not officially confirmed dwell time as a ranking factor.)

---

#### Pogo-Sticking

**Entity file:** [`entities/metrics/pogo-sticking.md`](entities/metrics/pogo-sticking.md)

When a user clicks a result, quickly returns to the SERP, and clicks a different result — signaling dissatisfaction with the first result. Implied negative ranking signal.

---

### Entity & Semantic Factors

---

#### Topical Authority

**Entity file:** [`entities/ranking-factors/topical-authority.md`](entities/ranking-factors/topical-authority.md)

A site's breadth and depth of coverage of a specific topic domain. Sites with comprehensive, interlinked content on a subject earn topical authority that enables ranking for queries in that topic space.

**Building signals:** Content clusters (pillar + supporting pages), internal linking within topic clusters, consistent publishing on related topics, expert authorship.

---

#### Entity Recognition

**Entity file:** [`entities/ranking-factors/entity-recognition.md`](entities/ranking-factors/entity-recognition.md)

Google's ability to identify and classify named entities (people, places, organizations, products, concepts) mentioned on a page, and use entity co-occurrence patterns as relevance signals.

**Related systems:** Google Natural Language API, Knowledge Graph, NLP via BERT/MUM.

---

#### Passage Ranking

**Entity file:** [`entities/ranking-factors/passage-ranking.md`](entities/ranking-factors/passage-ranking.md)

Google's system (announced 2020, rolling out 2021) for ranking individual passages within a long document, allowing a single deeply relevant paragraph to rank for a query even if the broader page isn't highly relevant.

---

## Part III — Google Algorithms & Core Updates

Google's ranking system is not a single algorithm — it's a layered system of algorithms, filters, quality raters, and machine learning models that operate simultaneously.

### Core Algorithm Components

---

#### PageRank

The original Google algorithm (1998). Assigns importance scores based on link graph analysis. Still fundamental but now one of hundreds of signals.

---

#### RankBrain

**Entity file:** [`entities/algorithms/rankbrain.md`](entities/algorithms/rankbrain.md)

Google's first machine learning ranking component, announced in October 2015. Interprets ambiguous or never-before-seen queries by mapping them to similar known queries. Described by Google as the third most important ranking signal at the time of announcement.

**Key attributes:**
- `type`: Machine learning (word vector / embedding based)
- `function`: Query interpretation, query-to-result mapping for novel queries
- `announced`: October 2015
- `deployment`: Affects ~15% of queries (2015 figure)

---

#### BERT (Bidirectional Encoder Representations from Transformers)

**Entity file:** [`entities/algorithms/bert.md`](entities/algorithms/bert.md)

Google's NLP breakthrough model (published 2018, deployed in Search October 2019). Allows Google to understand the context and nuance of words in queries — particularly for conversational queries and prepositions that change meaning.

**Key attributes:**
- `model_type`: Transformer-based NLP model (fine-tuned for search)
- `coverage`: Affects ~10% of English queries (2019), later expanded
- `key_capability`: Understanding context — "can you get medicine for someone pharmacy" (understanding "for someone" changes the search intent)

---

#### MUM (Multitask Unified Model)

**Entity file:** [`entities/algorithms/mum.md`](entities/algorithms/mum.md)

Google's multimodal AI model (announced 2021), described as 1000× more powerful than BERT. Understands and generates text across 75+ languages simultaneously, and can process images, video, and audio.

**Key attributes:**
- `announced`: Google I/O May 2021
- `capabilities`: Cross-lingual understanding, multimodal inputs, complex multi-step query resolution
- `use_case`: Answering complex, multi-part queries; entity understanding across languages; vaccine information panels (first deployment)

---

#### Gemini in Search

**Entity file:** [`entities/algorithms/gemini-search.md`](entities/algorithms/gemini-search.md)

Google's latest large language model integrated into Search to power AI Overviews and other generative features. Replaced MUM as the primary generative backbone.

---

### Named Algorithm Updates

---

#### Google Panda (2011)

**Entity file:** [`entities/algorithms/panda.md`](entities/algorithms/panda.md)

Major update targeting low-quality, thin, and duplicate content. Penalized content farms and sites with high proportions of low-quality pages.

**Key attributes:**
- `first_launched`: February 24, 2011
- `target`: Thin content, duplicate content, content farms, low-quality UGC
- `mechanism`: Site-wide quality score — a single bad section could hurt the entire domain
- `incorporated_into_core`: 2016 (folded into core algorithm, runs continuously)

---

#### Google Penguin (2012)

**Entity file:** [`entities/algorithms/penguin.md`](entities/algorithms/penguin.md)

Major update targeting webspam, specifically manipulative link building practices (paid links, link networks, keyword-stuffed anchor text).

**Key attributes:**
- `first_launched`: April 24, 2012
- `target`: Unnatural link profiles, link schemes, anchor text over-optimization
- `mechanism`: Discounted or penalized sites with manipulative link patterns
- `incorporated_into_core`: September 2016 (real-time, runs continuously)

---

#### Google Hummingbird (2013)

**Entity file:** [`entities/algorithms/hummingbird.md`](entities/algorithms/hummingbird.md)

A complete algorithm rewrite (not an update) focused on conversational search and semantic understanding. The first major step toward entity-based search over keyword matching.

**Key attributes:**
- `launched`: August 2013 (announced October 2013)
- `focus`: Conversational queries, semantic meaning, query intent over keyword matching
- `significance`: Entire query understanding — Panda/Penguin were filters on top of the old algorithm; Hummingbird replaced the core

---

#### Google Pigeon (2014)

**Entity file:** [`entities/algorithms/pigeon.md`](entities/algorithms/pigeon.md)

A local search algorithm update that improved the integration of local results with core web ranking signals and improved distance/location ranking parameters.

**Key attributes:**
- `launched`: July 24, 2014 (US); December 2014 (UK, Canada, Australia)
- `impact`: Local search results quality improved; many local directories gained visibility

---

#### Mobilegeddon (2015)

**Entity file:** [`entities/algorithms/mobilegeddon.md`](entities/algorithms/mobilegeddon.md)

Google's first official mobile-friendliness ranking update, boosting mobile-friendly pages in mobile search results.

**Key attributes:**
- `launched`: April 21, 2015
- `scope`: Mobile SERPs only
- `tool`: Google Mobile-Friendly Test

---

#### Medic Update (2018)

**Entity file:** [`entities/algorithms/medic.md`](entities/algorithms/medic.md)

A major broad core algorithm update that disproportionately affected health, medical, and YMYL (Your Money Your Life) websites. The first update where E-A-T became widely discussed as a quality signal.

**Key attributes:**
- `launched`: August 1, 2018
- `sectors_affected`: Health, medical, finance, legal — YMYL content
- `mechanism`: Raised the bar for E-A-T on high-stakes content

---

#### BERT Update (2019)

**Entity file:** [`entities/algorithms/bert-update.md`](entities/algorithms/bert-update.md)

Deployment of the BERT NLP model in Google Search — the largest step change in query understanding in 5 years.

---

#### Helpful Content Update (2022–2023)

**Entity file:** [`entities/algorithms/helpful-content.md`](entities/algorithms/helpful-content.md)

A series of updates introducing a site-wide classifier that identifies and penalizes content written primarily for search engines rather than humans.

**Key attributes:**
- `first_launched`: August 25, 2022
- `mechanism`: Machine learning classifier assigns a "helpfulness" signal at site level — affects all pages on a site if too much content is deemed unhelpful
- `incorporated_into_core`: March 2024 Core Update absorbed the Helpful Content System
- `signals`:
  - Original analysis vs. regurgitation
  - First-hand experience
  - Depth of expertise
  - Content written for humans, not crawlers
  - Accurate information with sourcing

---

#### March 2024 Core Update

**Entity file:** [`entities/algorithms/march-2024-core.md`](entities/algorithms/march-2024-core.md)

The largest documented Google core algorithm update, taking 45 days to complete rollout. Aimed at reducing unhelpful, low-quality, and AI-generated spam content by 40%.

**Key attributes:**
- `announced`: March 5, 2024
- `rollout_completed`: April 19, 2024
- `duration`: 45 days (longest on record)
- `stated_goal`: Reduce unhelpful content in results by 40%
- `new_spam_policies`: Site reputation abuse (parasite SEO), scaled content abuse (AI spam), expired domain abuse

---

#### SpamBrain

**Entity file:** [`entities/algorithms/spambrain.md`](entities/algorithms/spambrain.md)

Google's AI-based spam detection system, used to identify and neutralize link spam, spammy content, and web spam at scale.

---

## Part IV — Search Intent Framework

Search intent (also called query intent or user intent) describes the goal behind a user's search query. Google's primary task is matching SERP content to intent — the wrong intent match means the wrong result, regardless of other quality signals.

---

#### Informational Intent

**Entity file:** [`entities/intent/informational.md`](entities/intent/informational.md)

The user wants to learn something. The query is seeking knowledge, explanations, definitions, or answers.

**Signals:** Question words (who, what, when, where, why, how), "definition of," "meaning of," "what is," "how does"
**SERP features triggered:** Featured Snippet, People Also Ask, Knowledge Panel, Image Pack
**Content type:** Articles, explainers, tutorials, guides, encyclopedia entries

---

#### Navigational Intent

**Entity file:** [`entities/intent/navigational.md`](entities/intent/navigational.md)

The user wants to reach a specific website or page. They already know the destination.

**Signals:** Brand names, website names, "[brand] login," "[brand] careers"
**SERP features triggered:** Sitelinks, Knowledge Panel, Sitelinks Search Box
**Content type:** Not relevant — the user wants the brand's own page

---

#### Transactional Intent

**Entity file:** [`entities/intent/transactional.md`](entities/intent/transactional.md)

The user intends to complete an action — typically a purchase, download, sign-up, or booking.

**Signals:** "buy," "order," "download," "subscribe," "sign up," "[product] price," "[product] deal"
**SERP features triggered:** Shopping Ads, Product Rich Results, Shopping Carousel
**Content type:** Product pages, checkout pages, landing pages, pricing pages

---

#### Commercial Investigation Intent

**Entity file:** [`entities/intent/commercial-investigation.md`](entities/intent/commercial-investigation.md)

The user is researching products or services before making a purchase decision — comparison shopping or seeking recommendations.

**Signals:** "best," "vs," "review," "comparison," "top," "cheapest," "[product] alternative"
**SERP features triggered:** Review Snippets, Product Rich Results, Perspectives/Forum Results
**Content type:** Comparison articles, review posts, "best X for Y" guides, listicles

---

#### Local Intent

**Entity file:** [`entities/intent/local.md`](entities/intent/local.md)

The user is looking for products, services, or information within a specific geographic area.

**Signals:** "near me," "[service] in [city]," location modifiers, queries with implicit local intent (e.g., "coffee shop," "emergency plumber")
**SERP features triggered:** Local Pack, Local Finder, Local Knowledge Panel, Local Service Ads
**Content type:** Google Business Profile, location pages, local landing pages

---

#### Seasonal / Temporal Intent

**Entity file:** [`entities/intent/seasonal.md`](entities/intent/seasonal.md)

The user's query is driven by time-sensitive events, seasons, or recurring patterns.

**Signals:** Holiday names, year modifiers ("2025"), "this week," trending topics, sports seasons
**SERP features triggered:** News Box, Top Stories, freshness boost in organic
**Content type:** Timely articles, seasonal guides, trending content

---

#### Visual / Image Intent

**Entity file:** [`entities/intent/visual.md`](entities/intent/visual.md)

The user primarily wants images or visual content for the query topic.

**Signals:** Visual topics (fashion, interior design, art, recipes with photos), creative queries
**SERP features triggered:** Image Pack, Video Carousel, Web Stories
**Content type:** Image-heavy pages, image-optimized content

---

#### Voice Search Intent

**Entity file:** [`entities/intent/voice-search.md`](entities/intent/voice-search.md)

Queries phrased conversationally, often longer and more natural language, typically originating from voice assistants (Google Assistant, Siri).

**Signals:** Conversational phrasing, question format, "OK Google" style queries
**SERP output:** Featured Snippets (read aloud), Knowledge Cards
**Content type:** FAQ-structured content, conversational long-form content

---

## Part V — SERP Metrics & Measurement

SERP metrics are the measurable signals used to evaluate performance, authority, and health in the context of search engine optimization.

---

#### Impressions

**Entity file:** [`entities/metrics/impressions.md`](entities/metrics/impressions.md)

The number of times a URL appeared in search results for a query (even if not seen by the user due to position). Reported in Google Search Console.

**Counting rules:** An impression is counted when a URL appears in a search result that a user could see — subject to GSC's position-dependent counting rules.

---

#### Clicks

**Entity file:** [`entities/metrics/clicks.md`](entities/metrics/clicks.md)

The number of times a user clicked a URL from the SERP to your site. Reported in Google Search Console.

---

#### Click-Through Rate (CTR)

**Entity file:** [`entities/metrics/ctr.md`](entities/metrics/ctr.md)

**Formula:** CTR = (Clicks ÷ Impressions) × 100%

**Benchmark CTRs by position (approximate):**
- Position 1: ~27–39%
- Position 2: ~15–18%
- Position 3: ~10–12%
- Position 4: ~7–9%
- Position 5: ~5–6%
- Positions 6–10: 2–4%
- Featured Snippet: Highly variable — can be highest or lower than P1 depending on query

---

#### Average Position

**Entity file:** [`entities/metrics/average-position.md`](entities/metrics/average-position.md)

The mean position of a URL in search results across all queries that triggered an impression. Reported in Google Search Console.

**Caveat:** Average position hides bimodal distributions — a page might rank #1 for some queries and #20 for others, averaging to #10.

---

#### Visibility Index

**Entity file:** [`entities/metrics/visibility-index.md`](entities/metrics/visibility-index.md)

A composite metric measuring the estimated visibility of a domain in organic search, weighted by keyword search volume and position. Used by tools like SISTRIX (Visibility Index) and Semrush.

---

#### Share of Voice (SOV)

**Entity file:** [`entities/metrics/share-of-voice.md`](entities/metrics/share-of-voice.md)

The percentage of total available organic clicks for a defined keyword set captured by a specific domain, relative to competitors.

---

#### Organic Traffic

**Entity file:** [`entities/metrics/organic-traffic.md`](entities/metrics/organic-traffic.md)

Sessions or users arriving at a website via unpaid search results. The primary conversion metric for SEO. Measured in Google Analytics / GA4.

---

#### Dwell Time

**Entity file:** [`entities/metrics/dwell-time.md`](entities/metrics/dwell-time.md)

The duration between a user clicking a result and returning to the SERP. A proxy for content satisfaction.

---

#### Bounce Rate

**Entity file:** [`entities/metrics/bounce-rate.md`](entities/metrics/bounce-rate.md)

The percentage of sessions where the user left the site after viewing only one page. High bounce rate can indicate content-query mismatch.

**Note:** In GA4, "bounce rate" is replaced by "engagement rate" (sessions with engagement events). High bounce rate is not inherently negative — a successful "one-and-done" informational page may have naturally high bounce rate.

---

#### Domain Rating (DR) / Domain Authority (DA)

**Entity file:** [`entities/metrics/domain-authority-metrics.md`](entities/metrics/domain-authority-metrics.md)

Third-party metrics approximating a domain's link authority:
- **Domain Rating (DR)** — Ahrefs' metric, 0–100 logarithmic scale based on backlink quality/quantity
- **Domain Authority (DA)** — Moz's metric, 0–100 logarithmic scale
- **Trust Flow / Citation Flow** — Majestic's dual metric system measuring link quality vs. quantity

**Important:** These are proprietary estimates, not Google signals. Google does not use DA, DR, or TF/CF.

---

#### Referring Domains

**Entity file:** [`entities/metrics/referring-domains.md`](entities/metrics/referring-domains.md)

The count of unique root domains that have at least one link pointing to a target domain/URL. A key link diversity metric.

---

#### Core Web Vitals Score

**Entity file:** [`entities/metrics/core-web-vitals-score.md`](entities/metrics/core-web-vitals-score.md)

CWV assessment (Pass/Fail per metric) from Chrome User Experience Report (CrUX) field data, PageSpeed Insights lab data, and Google Search Console Core Web Vitals report.

---

#### Featured Snippet Rate

**Entity file:** [`entities/metrics/featured-snippet-rate.md`](entities/metrics/featured-snippet-rate.md)

The percentage of tracked keywords for which a domain holds a Featured Snippet. A measure of SERP feature visibility beyond standard position.

---

## Part VI — Technical SEO Attributes

Technical SEO attributes govern how search engines discover, crawl, render, and index web content — the foundation upon which all other ranking signals operate.

---

#### Crawlability

**Entity file:** [`entities/technical/crawlability.md`](entities/technical/crawlability.md)

The ability of search engine crawlers (Googlebot, Bingbot) to discover and access pages on a website.

**Affecting factors:** robots.txt directives, internal linking depth, pagination, JavaScript rendering requirements, server errors (5xx), crawl rate limits, Crawl Budget.

---

#### Crawl Budget

**Entity file:** [`entities/technical/crawl-budget.md`](entities/technical/crawl-budget.md)

The number of pages Googlebot will crawl on a site within a given timeframe. Determined by Crawl Rate Limit (server capacity) and Crawl Demand (popularity/freshness signals).

**Optimization:** Block low-value URLs via robots.txt or noindex, fix crawl errors, reduce duplicate content, improve server speed, remove infinite scroll traps.

---

#### Indexability

**Entity file:** [`entities/technical/indexability.md`](entities/technical/indexability.md)

Whether a crawled page can be added to Google's search index and shown in results.

**Blocking indexation:** `<meta name="robots" content="noindex">`, `X-Robots-Tag: noindex` header, canonical pointing to another URL, soft 404 errors, blocked by login walls.

---

#### robots.txt

**Entity file:** [`entities/technical/robots-txt.md`](entities/technical/robots-txt.md)

A plain-text file at the root of a domain (`/robots.txt`) that instructs crawlers which pages/directories to crawl or avoid.

**Key rules:**
- `Disallow:` — blocks crawling of specified paths
- `Allow:` — overrides Disallow for specific paths
- `Sitemap:` — declares sitemap location
- `User-agent:` — targets specific crawlers

**Critical distinction:** robots.txt controls *crawling*, not *indexing*. A page blocked in robots.txt can still be indexed if linked from elsewhere (Google may index without crawling in some cases).

---

#### XML Sitemap

**Entity file:** [`entities/technical/sitemap-xml.md`](entities/technical/sitemap-xml.md)

An XML file listing URLs on a site for discovery and crawling guidance.

**Types:** Standard sitemap, Image sitemap, Video sitemap, News sitemap, Index sitemap (for large sites with multiple sitemaps)

---

#### Canonical Tag

**Entity file:** [`entities/technical/canonical.md`](entities/technical/canonical.md)

The `<link rel="canonical" href="...">` tag signals Google's preferred version of a URL when duplicate or similar content exists across multiple URLs.

**Use cases:** URL parameter variations, HTTP/HTTPS duplicates, www/non-www duplicates, printer-friendly page versions, paginated content, cross-domain syndication.

---

#### Hreflang Tags

**Entity file:** [`entities/technical/hreflang.md`](entities/technical/hreflang.md)

HTML attributes (or XML sitemap annotations) signaling to Google which language/region version of a page to serve to specific international audiences.

**Format:** `<link rel="alternate" hreflang="en-us" href="...">`
**Implementation:** Must be bidirectional (all alternates must reference each other), include an `x-default` fallback.

---

#### Structured Data (JSON-LD)

**Entity file:** [`entities/technical/structured-data.md`](entities/technical/structured-data.md)

Machine-readable code (JSON-LD is Google's recommended format) implementing Schema.org vocabulary to explicitly communicate page content type and attributes to search engines.

**Formats:** JSON-LD (inline script tag, preferred), Microdata (HTML attribute-based), RDFa (attribute-based, older)
**Testing tools:** Google Rich Results Test, Schema Markup Validator

---

#### Open Graph Protocol

**Entity file:** [`entities/technical/open-graph.md`](entities/technical/open-graph.md)

Facebook's metadata protocol (`og:title`, `og:image`, `og:description`, `og:url`) for controlling how pages appear when shared on social platforms. Not a Google ranking signal, but affects social CTR.

---

#### Core Web Vitals (Technical Optimization)

**Entity file:** [`entities/technical/core-web-vitals-tech.md`](entities/technical/core-web-vitals-tech.md)

Technical implementation practices for meeting Core Web Vitals thresholds:
- **LCP optimization:** Server response time, render-blocking resources, resource load time, element render time. Strategies: preload LCP resource, optimize images (WebP/AVIF, lazy load non-LCP, no lazy load on LCP), remove render-blocking CSS/JS.
- **INP optimization:** Minimize long tasks, reduce JavaScript execution, use web workers, defer non-critical JS.
- **CLS optimization:** Size attributes on images/videos, avoid inserting content above existing content, use CSS transform for animations.

---

#### JavaScript SEO

**Entity file:** [`entities/technical/javascript-seo.md`](entities/technical/javascript-seo.md)

The challenge of ensuring JavaScript-rendered content is crawlable and indexable by search engines. Googlebot executes JavaScript but in a "second wave" (delayed crawl queue) — content only available via JavaScript may be indexed days/weeks later than server-rendered HTML.

**Best practices:** Server-side rendering (SSR), static site generation (SSG), dynamic rendering for critical content, hydration strategies.

---

#### Pagination

**Entity file:** [`entities/technical/pagination.md`](entities/technical/pagination.md)

The technical handling of multi-page content (e.g., page 1, 2, 3 of a blog or product category).

**Current recommendation (post-2019):** Google dropped `rel=prev/next` support in 2019. Each paginated page should be self-canonicalized or use a "view-all" page as canonical. Infinite scroll must be implemented with proper URL fragments for indexability.

---

#### Log File Analysis

**Entity file:** [`entities/technical/log-file-analysis.md`](entities/technical/log-file-analysis.md)

Analysis of web server access logs to understand actual Googlebot crawl behavior — which pages are crawled, how often, with what status codes, and crawl budget allocation.

---

#### AMP (Accelerated Mobile Pages)

**Entity file:** [`entities/technical/amp.md`](entities/technical/amp.md)

Google's open-source framework (launched 2015) for creating fast-loading mobile web pages. AMP was previously required for Top Stories carousel inclusion on mobile — that requirement was removed in 2021.

**Current status:** No longer a ranking factor or Top Stories requirement. Still used by some publishers for performance. Google Web Stories uses an AMP-based format.

---

## Part VII — AI Search Landscape

The AI search landscape describes how large language models and generative AI are transforming the SERP — both how Google generates results and how competing AI search engines operate.

---

#### AI Overview (Google)

**Entity file:** [`entities/ai-search/ai-overview.md`](entities/ai-search/ai-overview.md)

See [AI Overview entry](#ai-overview-formerly-sge--search-generative-experience) in Part I above.

---

#### Generative Engine Optimization (GEO)

**Entity file:** [`entities/ai-search/geo.md`](entities/ai-search/geo.md)

The emerging practice of optimizing content to be cited, quoted, or referenced by AI-generated search answers (AI Overviews, Perplexity, ChatGPT Search, etc.).

**GEO signals (research-backed):**
- Citing authoritative sources and statistics
- Including quotations from experts
- Using fluent, clear prose
- Comprehensive coverage of the topic
- Strong underlying SEO (standard ranking factors still matter for citation selection)
- Entity authority (Knowledge Graph presence)

---

#### Answer Engine Optimization (AEO)

**Entity file:** [`entities/ai-search/aeo.md`](entities/ai-search/aeo.md)

Optimization for answer engines — search interfaces that return direct answers rather than lists of links. Overlaps with GEO but focuses specifically on structured Q&A formats, Featured Snippets, and voice search.

---

#### LLM Optimization (LLMO)

**Entity file:** [`entities/ai-search/llmo.md`](entities/ai-search/llmo.md)

The practice of optimizing brand and content presence within the training data and retrieval mechanisms of large language models — ensuring models mention, recommend, or cite your entity accurately.

---

#### ChatGPT Search

**Entity file:** [`entities/ai-search/chatgpt-search.md`](entities/ai-search/chatgpt-search.md)

OpenAI's web search integration in ChatGPT (launched October 2024), providing real-time web citations within ChatGPT responses.

**Key attributes:**
- `search_provider`: Microsoft Bing (web index)
- `citation_format`: Inline citations with source cards
- `seo_relevance`: Bing indexing and authority affects citation likelihood

---

#### Perplexity AI

**Entity file:** [`entities/ai-search/perplexity.md`](entities/ai-search/perplexity.md)

An AI-powered answer engine that searches the web and synthesizes answers with inline citations. Growing as a Google alternative for research queries.

**Key attributes:**
- `model_basis`: Multiple LLMs (GPT-4, Claude, Sonar)
- `search_index`: Proprietary web crawl + Bing
- `citation_format`: Numbered inline citations, source list

---

#### Bing Copilot / Microsoft Copilot Search

**Entity file:** [`entities/ai-search/bing-copilot.md`](entities/ai-search/bing-copilot.md)

Microsoft's AI-augmented search experience in Bing, powered by OpenAI GPT-4. Provides conversational AI answers alongside traditional web results.

---

#### AI Citation Factors

**Entity file:** [`entities/ai-search/ai-citation-factors.md`](entities/ai-search/ai-citation-factors.md)

The signals that influence whether an AI search engine (AI Overview, Perplexity, ChatGPT Search) cites a specific web source in its generated answer.

**Known factors:**
- Source authority (domain authority, E-E-A-T signals)
- Topical specificity and relevance
- Content recency
- Structural clarity (headers, lists, Q&A formats)
- Factual accuracy and citation density
- Diversity of source types used by the AI system

---

## Part VIII — Knowledge Graph & Entity Framework

The Knowledge Graph is Google's semantic database of real-world entities and relationships, used to understand queries, generate Knowledge Panels, and power AI features.

---

#### Google Knowledge Graph

**Entity file:** [`entities/knowledge-entities/knowledge-graph.md`](entities/knowledge-entities/knowledge-graph.md)

A massive graph database of entities (people, places, organizations, things, concepts) and the relationships between them, powering Google's entity-based search understanding.

**Key attributes:**
- `launched`: May 2012
- `sources`: Wikipedia, Wikidata, Freebase (now incorporated), CIA World Factbook, official websites, structured data
- `size`: Hundreds of billions of facts about billions of entities
- `integration_points`: Knowledge Panel, Knowledge Card, Featured Snippet sourcing, Query interpretation, AI Overviews

---

#### Entity Types (Schema.org Hierarchy)

**Entity file:** [`entities/knowledge-entities/entity-types.md`](entities/knowledge-entities/entity-types.md)

The major entity type categories relevant to SERP:

- **Thing** — Base type for all entities
  - **Person** — Individuals (authors, public figures, professionals)
  - **Organization** — Companies, institutions, NGOs, government bodies
    - **LocalBusiness** — Physical location businesses
  - **Place** — Geographic locations
    - **City, Country, Landmark, Address**
  - **Product** — Physical or digital goods
  - **Event** — Occurrences at a place and time
  - **CreativeWork** — Content artifacts
    - Article, BlogPosting, Book, Movie, MusicRecording, Podcast, VideoObject, WebPage, WebSite
  - **Action** — Activities and interactions
  - **Intangible** — Concepts, roles, quantities, structured values
    - Brand, BreadcrumbList, DefinedTerm, FAQPage, HowTo, JobPosting, Language, Offer, Rating, Review

---

#### Named Entity Recognition (NER)

**Entity file:** [`entities/knowledge-entities/ner.md`](entities/knowledge-entities/ner.md)

Google's process of identifying and classifying named entities (people, organizations, locations, products, dates) in text, used for query understanding and content relevance assessment.

---

#### Entity Disambiguation

**Entity file:** [`entities/knowledge-entities/entity-disambiguation.md`](entities/knowledge-entities/entity-disambiguation.md)

The process of resolving which specific entity a query or mention refers to, when multiple entities share similar names (e.g., "Paris" = city, person's name, or other uses).

**Signals:** Context words, query co-occurrence patterns, geographic signals, entity salience scores.

---

#### Knowledge Graph Entity Establishment

**Entity file:** [`entities/knowledge-entities/entity-establishment.md`](entities/knowledge-entities/entity-establishment.md)

The process by which a real-world entity gains representation in Google's Knowledge Graph — enabling Knowledge Panel generation and entity-based search understanding.

**Establishment signals:**
- Wikipedia article
- Wikidata entry with structured properties
- Structured data markup on official website (Organization, Person, LocalBusiness)
- Press coverage and mentions from authoritative sources
- Social profile verification
- Google Search Console verification

---

## Part IX — SERP Layout Anatomy

SERP layout describes where different result types and features appear on the search results page — both physically (above/below fold) and positionally (ranked order).

---

#### Position Zero

**Entity file:** [`entities/layout/position-zero.md`](entities/layout/position-zero.md)

The Featured Snippet appears "above" Position 1, hence called Position Zero. The page that holds Position Zero simultaneously holds an organic ranking (usually positions 1–5) — the Featured Snippet extracts from a ranked page but displays its content before the organic result.

---

#### Above the Fold

**Entity file:** [`entities/layout/above-the-fold.md`](entities/layout/above-the-fold.md)

The portion of the SERP visible without scrolling. Increasingly dominated by Ads, AI Overviews, and Featured Snippets — organic results may not appear above the fold on competitive queries.

**Vertical scroll depth to first organic result (approximate):**
- Simple informational query: 0–200px (Featured Snippet is first)
- Commercial query: 400–600px (multiple ads before organic)
- AI Overview query: 600–800px+ (AI answer + sources before organic)

---

#### Blue Links

**Entity file:** [`entities/layout/blue-links.md`](entities/layout/blue-links.md)

The traditional organic search results — URL, title, and snippet — the format Google has used since 1998 and still the primary result format for most queries.

---

#### SERP Desktop vs. Mobile Layout

**Entity file:** [`entities/layout/desktop-vs-mobile.md`](entities/layout/desktop-vs-mobile.md)

The SERP layout differs significantly between desktop and mobile:
- **Desktop:** Two-column layout with Knowledge Panel on right, organic results on left; more results visible per scroll
- **Mobile:** Single-column, sequential layout; AI Overviews and Local Pack appear more prominently; features are touch-optimized (carousels, tap targets)

---

#### SERP Carousel

**Entity file:** [`entities/layout/serp-carousel.md`](entities/layout/serp-carousel.md)

A horizontally scrollable row of results (video, images, recipes, products, news). Allows multiple results to occupy a compact vertical space.

---

## Part X — Serponado Entity Standard

The Serponado Standard defines the schema and format for all entity pages in this repository. Every entity file follows this standard to ensure consistency, machine-parseability, and cross-referenceability.

**Full specification:** See [STANDARD.md](STANDARD.md)

### Entity Frontmatter Schema

Every entity file begins with YAML frontmatter using the following schema:

```yaml
---
entityId: string          # Unique kebab-case identifier (required)
name: string              # Display name (required)
type: EntityType          # See EntityType enum (required)
schemaType: string        # Schema.org type or DefinedTerm
version: semver           # Entity schema version (default: 1.0.0)
status: Status            # active | deprecated | emerging | experimental
aliases: string[]         # Alternative names
sameAs: URI[]             # External knowledge base URIs (Wikipedia, Wikidata)
parent: entityId          # Parent entity reference
namespace: string         # Folder path within entities/
relations: Relation[]     # Typed relationships to other entities
attributes: object        # Type-specific key-value attributes
evidence: Evidence[]      # Source citations
lastReviewed: date        # ISO 8601 date of last review
---
```

### EntityType Enum

```
SERP_Feature
Paid_Feature
Ranking_Factor
Algorithm
Algorithm_Update
Search_Intent
Metric
Technical_Attribute
AI_Search_Feature
Layout_Element
Entity_Type
Tool
Concept
```

### Relation Predicates

```
IS_TYPE_OF          # This entity is a subtype of target
HAS_SUBTYPE         # This entity has target as a subtype
PART_OF             # Component relationship
CONTAINS            # This entity contains target
TRIGGERS            # This entity triggers target
TRIGGERED_BY        # This entity is triggered by target
COMPETES_WITH       # Competing for same SERP real estate
REQUIRES            # This entity requires target
POWERS              # This entity powers/enables target
POWERED_BY          # This entity is powered by target
REPLACED_BY         # This entity was replaced by target
REPLACES            # This entity replaced target
MEASURES            # This metric measures target
MEASURED_BY         # This entity is measured by target
OPTIMIZED_BY        # This entity is optimized by target
AFFECTS             # This entity affects target
INTRODUCED_BY       # This entity was introduced by target
DEPRECATED_BY       # This entity was deprecated by target
RELATED_TO          # General semantic relationship
ANALOGOUS_TO        # Functionally similar in different context
```

---

## Entity Index

### SERP Features (35 entities)

| Entity | File | Status |
|--------|------|--------|
| Featured Snippet | [serp-features/featured-snippet.md](entities/serp-features/featured-snippet.md) | active |
| Knowledge Panel | [serp-features/knowledge-panel.md](entities/serp-features/knowledge-panel.md) | active |
| Knowledge Card | [serp-features/knowledge-card.md](entities/serp-features/knowledge-card.md) | active |
| People Also Ask | [serp-features/people-also-ask.md](entities/serp-features/people-also-ask.md) | active |
| Image Pack | [serp-features/image-pack.md](entities/serp-features/image-pack.md) | active |
| Video Carousel | [serp-features/video-carousel.md](entities/serp-features/video-carousel.md) | active |
| News Box / Top Stories | [serp-features/news-box.md](entities/serp-features/news-box.md) | active |
| Local Pack | [serp-features/local-pack.md](entities/serp-features/local-pack.md) | active |
| Sitelinks | [serp-features/sitelinks.md](entities/serp-features/sitelinks.md) | active |
| Related Searches | [serp-features/related-searches.md](entities/serp-features/related-searches.md) | active |
| People Also Search For | [serp-features/people-also-search-for.md](entities/serp-features/people-also-search-for.md) | active |
| Perspectives / Forum Results | [serp-features/perspectives.md](entities/serp-features/perspectives.md) | active |
| Web Stories | [serp-features/web-stories.md](entities/serp-features/web-stories.md) | active |
| Review Snippets | [serp-features/review-snippets.md](entities/serp-features/review-snippets.md) | active |
| FAQ Results | [serp-features/faq-results.md](entities/serp-features/faq-results.md) | deprecated |
| How-To Results | [serp-features/how-to-results.md](entities/serp-features/how-to-results.md) | active |
| Job Listings | [serp-features/job-listings.md](entities/serp-features/job-listings.md) | active |
| Event Listings | [serp-features/event-listings.md](entities/serp-features/event-listings.md) | active |
| Recipe Cards | [serp-features/recipe-cards.md](entities/serp-features/recipe-cards.md) | active |
| Product Rich Results | [serp-features/product-rich-results.md](entities/serp-features/product-rich-results.md) | active |
| Book Results | [serp-features/book-results.md](entities/serp-features/book-results.md) | active |
| App Results | [serp-features/app-results.md](entities/serp-features/app-results.md) | active |
| Podcast Results | [serp-features/podcast-results.md](entities/serp-features/podcast-results.md) | active |
| Course Results | [serp-features/course-results.md](entities/serp-features/course-results.md) | active |
| Breadcrumb Trail | [serp-features/breadcrumbs.md](entities/serp-features/breadcrumbs.md) | active |
| Merchant Listings | [serp-features/merchant-listings.md](entities/serp-features/merchant-listings.md) | active |
| Dataset Rich Results | [serp-features/dataset-results.md](entities/serp-features/dataset-results.md) | active |
| Fact Check Labels | [serp-features/fact-check-labels.md](entities/serp-features/fact-check-labels.md) | active |
| Author Information | [serp-features/author-information.md](entities/serp-features/author-information.md) | active |
| Flights Box | [serp-features/flights-box.md](entities/serp-features/flights-box.md) | active |
| Hotels Pack | [serp-features/hotels-pack.md](entities/serp-features/hotels-pack.md) | active |
| Sports Scores | [serp-features/sports-scores.md](entities/serp-features/sports-scores.md) | active |
| Finance Box | [serp-features/finance-box.md](entities/serp-features/finance-box.md) | active |
| Weather Box | [serp-features/weather-box.md](entities/serp-features/weather-box.md) | active |
| Calculator | [serp-features/calculator.md](entities/serp-features/calculator.md) | active |
| Definition Box | [serp-features/definition-box.md](entities/serp-features/definition-box.md) | active |
| Translation Box | [serp-features/translation-box.md](entities/serp-features/translation-box.md) | active |
| Unit Converter | [serp-features/unit-converter.md](entities/serp-features/unit-converter.md) | active |

### Paid Features (6 entities)

| Entity | File | Status |
|--------|------|--------|
| Text Ads (RSA) | [paid-features/text-ads.md](entities/paid-features/text-ads.md) | active |
| Shopping Ads | [paid-features/shopping-ads.md](entities/paid-features/shopping-ads.md) | active |
| Local Service Ads | [paid-features/local-service-ads.md](entities/paid-features/local-service-ads.md) | active |
| Dynamic Search Ads | [paid-features/dynamic-search-ads.md](entities/paid-features/dynamic-search-ads.md) | active |
| Performance Max | [paid-features/performance-max.md](entities/paid-features/performance-max.md) | active |
| Call-Only Ads | [paid-features/call-only-ads.md](entities/paid-features/call-only-ads.md) | active |

### Ranking Factors (15 entities)

| Entity | File | Status |
|--------|------|--------|
| E-E-A-T | [ranking-factors/e-e-a-t.md](entities/ranking-factors/e-e-a-t.md) | active |
| Content Relevance | [ranking-factors/content-relevance.md](entities/ranking-factors/content-relevance.md) | active |
| Content Quality | [ranking-factors/content-quality.md](entities/ranking-factors/content-quality.md) | active |
| Content Freshness | [ranking-factors/content-freshness.md](entities/ranking-factors/content-freshness.md) | active |
| Backlinks | [ranking-factors/backlinks.md](entities/ranking-factors/backlinks.md) | active |
| PageRank | [ranking-factors/pagerank.md](entities/ranking-factors/pagerank.md) | active |
| Domain Authority Signals | [ranking-factors/domain-authority.md](entities/ranking-factors/domain-authority.md) | active |
| Core Web Vitals | [ranking-factors/core-web-vitals.md](entities/ranking-factors/core-web-vitals.md) | active |
| Mobile-First Indexing | [ranking-factors/mobile-first-indexing.md](entities/ranking-factors/mobile-first-indexing.md) | active |
| Page Speed | [ranking-factors/page-speed.md](entities/ranking-factors/page-speed.md) | active |
| HTTPS / SSL | [ranking-factors/https-ssl.md](entities/ranking-factors/https-ssl.md) | active |
| Structured Data | [ranking-factors/structured-data.md](entities/ranking-factors/structured-data.md) | active |
| Brand Signals | [ranking-factors/brand-signals.md](entities/ranking-factors/brand-signals.md) | active |
| Topical Authority | [ranking-factors/topical-authority.md](entities/ranking-factors/topical-authority.md) | active |
| Entity Recognition | [ranking-factors/entity-recognition.md](entities/ranking-factors/entity-recognition.md) | active |

### Algorithms (12 entities)

| Entity | File | Status |
|--------|------|--------|
| RankBrain | [algorithms/rankbrain.md](entities/algorithms/rankbrain.md) | active |
| BERT | [algorithms/bert.md](entities/algorithms/bert.md) | active |
| MUM | [algorithms/mum.md](entities/algorithms/mum.md) | active |
| Gemini in Search | [algorithms/gemini-search.md](entities/algorithms/gemini-search.md) | active |
| Google Panda | [algorithms/panda.md](entities/algorithms/panda.md) | deprecated |
| Google Penguin | [algorithms/penguin.md](entities/algorithms/penguin.md) | deprecated |
| Google Hummingbird | [algorithms/hummingbird.md](entities/algorithms/hummingbird.md) | active |
| Google Pigeon | [algorithms/pigeon.md](entities/algorithms/pigeon.md) | active |
| Mobilegeddon | [algorithms/mobilegeddon.md](entities/algorithms/mobilegeddon.md) | deprecated |
| Medic Update | [algorithms/medic.md](entities/algorithms/medic.md) | deprecated |
| Helpful Content System | [algorithms/helpful-content.md](entities/algorithms/helpful-content.md) | active |
| March 2024 Core Update | [algorithms/march-2024-core.md](entities/algorithms/march-2024-core.md) | active |

### Search Intent (7 entities)

| Entity | File | Status |
|--------|------|--------|
| Informational Intent | [intent/informational.md](entities/intent/informational.md) | active |
| Navigational Intent | [intent/navigational.md](entities/intent/navigational.md) | active |
| Transactional Intent | [intent/transactional.md](entities/intent/transactional.md) | active |
| Commercial Investigation | [intent/commercial-investigation.md](entities/intent/commercial-investigation.md) | active |
| Local Intent | [intent/local.md](entities/intent/local.md) | active |
| Seasonal Intent | [intent/seasonal.md](entities/intent/seasonal.md) | active |
| Voice Search Intent | [intent/voice-search.md](entities/intent/voice-search.md) | active |

### Metrics (12 entities)

| Entity | File | Status |
|--------|------|--------|
| Impressions | [metrics/impressions.md](entities/metrics/impressions.md) | active |
| Clicks | [metrics/clicks.md](entities/metrics/clicks.md) | active |
| CTR | [metrics/ctr.md](entities/metrics/ctr.md) | active |
| Average Position | [metrics/average-position.md](entities/metrics/average-position.md) | active |
| Visibility Index | [metrics/visibility-index.md](entities/metrics/visibility-index.md) | active |
| Share of Voice | [metrics/share-of-voice.md](entities/metrics/share-of-voice.md) | active |
| Organic Traffic | [metrics/organic-traffic.md](entities/metrics/organic-traffic.md) | active |
| Dwell Time | [metrics/dwell-time.md](entities/metrics/dwell-time.md) | active |
| Bounce Rate | [metrics/bounce-rate.md](entities/metrics/bounce-rate.md) | active |
| Domain Rating / DA | [metrics/domain-authority-metrics.md](entities/metrics/domain-authority-metrics.md) | active |
| Referring Domains | [metrics/referring-domains.md](entities/metrics/referring-domains.md) | active |
| Core Web Vitals Score | [metrics/core-web-vitals-score.md](entities/metrics/core-web-vitals-score.md) | active |

### Technical Attributes (12 entities)

| Entity | File | Status |
|--------|------|--------|
| Crawlability | [technical/crawlability.md](entities/technical/crawlability.md) | active |
| Crawl Budget | [technical/crawl-budget.md](entities/technical/crawl-budget.md) | active |
| Indexability | [technical/indexability.md](entities/technical/indexability.md) | active |
| robots.txt | [technical/robots-txt.md](entities/technical/robots-txt.md) | active |
| XML Sitemap | [technical/sitemap-xml.md](entities/technical/sitemap-xml.md) | active |
| Canonical Tag | [technical/canonical.md](entities/technical/canonical.md) | active |
| Hreflang Tags | [technical/hreflang.md](entities/technical/hreflang.md) | active |
| Structured Data JSON-LD | [technical/structured-data.md](entities/technical/structured-data.md) | active |
| Core Web Vitals Tech | [technical/core-web-vitals-tech.md](entities/technical/core-web-vitals-tech.md) | active |
| JavaScript SEO | [technical/javascript-seo.md](entities/technical/javascript-seo.md) | active |
| AMP | [technical/amp.md](entities/technical/amp.md) | deprecated |
| Log File Analysis | [technical/log-file-analysis.md](entities/technical/log-file-analysis.md) | active |

### AI Search (8 entities)

| Entity | File | Status |
|--------|------|--------|
| AI Overview | [ai-search/ai-overview.md](entities/ai-search/ai-overview.md) | active |
| GEO (Generative Engine Optimization) | [ai-search/geo.md](entities/ai-search/geo.md) | emerging |
| AEO (Answer Engine Optimization) | [ai-search/aeo.md](entities/ai-search/aeo.md) | active |
| LLMO | [ai-search/llmo.md](entities/ai-search/llmo.md) | emerging |
| ChatGPT Search | [ai-search/chatgpt-search.md](entities/ai-search/chatgpt-search.md) | active |
| Perplexity AI | [ai-search/perplexity.md](entities/ai-search/perplexity.md) | active |
| Bing Copilot | [ai-search/bing-copilot.md](entities/ai-search/bing-copilot.md) | active |
| AI Citation Factors | [ai-search/ai-citation-factors.md](entities/ai-search/ai-citation-factors.md) | active |

### Knowledge Entities (5 entities)

| Entity | File | Status |
|--------|------|--------|
| Google Knowledge Graph | [knowledge-entities/knowledge-graph.md](entities/knowledge-entities/knowledge-graph.md) | active |
| Entity Types (Schema.org) | [knowledge-entities/entity-types.md](entities/knowledge-entities/entity-types.md) | active |
| Named Entity Recognition | [knowledge-entities/ner.md](entities/knowledge-entities/ner.md) | active |
| Entity Disambiguation | [knowledge-entities/entity-disambiguation.md](entities/knowledge-entities/entity-disambiguation.md) | active |
| Entity Establishment | [knowledge-entities/entity-establishment.md](entities/knowledge-entities/entity-establishment.md) | active |

---

## Glossary

| Term | Definition |
|------|------------|
| **AEO** | Answer Engine Optimization — optimizing for direct answer surfaces |
| **AIO** | AI Overview — Google's AI-generated SERP answer block |
| **AMP** | Accelerated Mobile Pages — Google's fast-loading mobile web format |
| **BERT** | Bidirectional Encoder Representations from Transformers — Google's NLP model |
| **CLS** | Cumulative Layout Shift — Core Web Vitals visual stability metric |
| **CTR** | Click-Through Rate — clicks divided by impressions |
| **CWV** | Core Web Vitals — LCP, INP, CLS |
| **DA** | Domain Authority — Moz's domain strength metric |
| **DR** | Domain Rating — Ahrefs' domain strength metric |
| **DSA** | Dynamic Search Ads — auto-generated Google Ads from website content |
| **E-E-A-T** | Experience, Expertise, Authoritativeness, Trustworthiness |
| **FID** | First Input Delay — deprecated CWV metric, replaced by INP |
| **GBP** | Google Business Profile — formerly Google My Business |
| **GEO** | Generative Engine Optimization — optimizing for AI-generated answers |
| **GSC** | Google Search Console — Google's webmaster analytics tool |
| **INP** | Interaction to Next Paint — Core Web Vitals interactivity metric |
| **KG** | Knowledge Graph — Google's entity relationship database |
| **KP** | Knowledge Panel — entity information box on right of SERP |
| **LCP** | Largest Contentful Paint — Core Web Vitals loading metric |
| **LLMO** | Large Language Model Optimization — brand optimization within LLM context |
| **LSA** | Local Service Ads — pay-per-lead ads for local service businesses |
| **MUM** | Multitask Unified Model — Google's multimodal AI model |
| **NER** | Named Entity Recognition — identifying entities in text |
| **PAA** | People Also Ask — expandable question-and-answer SERP feature |
| **PASF** | People Also Search For — related search suggestions on back-click |
| **PLA** | Product Listing Ad — visual product ad (now Shopping Ads) |
| **PMax** | Performance Max — Google's cross-channel automated campaign type |
| **QDF** | Query Deserves Freshness — Google's temporal freshness boost system |
| **RSA** | Responsive Search Ads — current Google Ads text format |
| **SERP** | Search Engine Results Page — the page returned by a search engine |
| **SGE** | Search Generative Experience — now called AI Overviews |
| **SOV** | Share of Voice — % of available organic clicks captured |
| **TTFB** | Time to First Byte — server response speed metric |
| **YMYL** | Your Money Your Life — high-stakes content category (health, finance, safety) |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full contribution guide.

**Quick summary:**
1. Fork the repository
2. Copy [`templates/entity-template.md`](templates/entity-template.md) to the appropriate `entities/[namespace]/` directory
3. Fill in all required frontmatter fields and write a comprehensive prose section
4. Validate your frontmatter against [`schema/entity.schema.json`](schema/entity.schema.json)
5. Add your entity to the index table in this README and to `index.json`
6. Submit a pull request with the entity ID and name as the PR title

**Entity quality standards:**
- All required frontmatter fields must be present
- `sameAs` links to Wikipedia and/or Wikidata are required where entities exist there
- At least 2 `evidence` citations with source URL, title, and retrieved date
- Prose section must be genuinely explanatory — not a list of keywords
- Deprecated entities must explain what replaced them and why

---

## License

Serponado is released under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.

You are free to share and adapt this material for any purpose, provided appropriate credit is given to Serponado.

---

*Serponado — Because the only way to understand a tornado is to map every piece of debris it leaves behind.*
