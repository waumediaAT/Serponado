---
entityId: "backlinks"
name: "Backlinks"
type: Ranking_Factor
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Inbound Links"
  - "External Links"
  - "Inlinks"
  - "Link Profile"
  - "Link Building"
sameAs:
  - "https://en.wikipedia.org/wiki/Backlink"
  - "https://developers.google.com/search/docs/essentials/spam-policies#link-spam"
parent: "ranking-factor"
namespace: "ranking-factors"
relations:
  - predicate: RELATED_TO
    target: "pagerank"
    description: "PageRank is the foundational algorithm for weighting backlink value"
  - predicate: RELATED_TO
    target: "domain-authority"
    description: "Domain authority is a proxy metric derived from backlink profile"
  - predicate: AFFECTS
    target: "organic-result"
    description: "Backlink profile directly influences page and domain ranking potential"
  - predicate: RELATED_TO
    target: "penguin"
    description: "Google Penguin targets manipulative link building practices"
attributes:
  factor_type: off-page
  weight: high
  confirmed_by:
    - "Google's original PageRank paper (1998)"
    - "Google employees on record (Andrey Lipattsev 2016 — links, content, RankBrain top 3)"
    - "2024 Google API leak (NavBoost and link signals)"
  quality_signals:
    - "Domain authority of linking page"
    - "Topical relevance of linking page to target"
    - "Editorial context (in-content vs footer/sidebar)"
    - "Anchor text (branded, exact-match, generic, partial-match)"
    - "Follow vs. nofollow attribute"
    - "Diversity of linking root domains"
    - "Link velocity (acquisition rate)"
    - "Geographic and language relevance"
  link_attributes:
    follow: "Passes link equity (PageRank)"
    nofollow: "Does not guarantee equity pass; Google treats as hint"
    ugc: "User-generated content — treated like nofollow"
    sponsored: "Paid links — treated like nofollow"
  spam_signals:
    - "Unnatural anchor text distribution (over-optimized exact-match)"
    - "Links from low-quality or irrelevant sites"
    - "Purchased link networks"
    - "Private blog networks (PBNs)"
    - "Reciprocal link schemes"
  affects_feature:
    - organic-result
    - knowledge-panel
evidence:
  - source: "https://developers.google.com/search/docs/essentials/spam-policies#link-spam"
    title: "Google Search Spam Policies — Link Spam"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://en.wikipedia.org/wiki/PageRank"
    title: "PageRank — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Backlinks

## Definition

Backlinks (also called inbound links or inlinks) are hyperlinks on external websites that point to a page on a different domain. In Google's ranking system, backlinks function as votes of confidence — each link from one page to another signals that the linking page considers the linked page credible, relevant, or valuable. The quantity and quality of backlinks is one of Google's most significant ranking factors.

## Description

The power of backlinks as a ranking signal originates from Google's founding insight, formalized in the 1998 PageRank paper by Larry Page and Sergey Brin: the web's link structure is an implicit citation graph, and pages cited more by other credible pages are likely more credible themselves.

Modern link evaluation is far more nuanced than raw count. Google's algorithms assess link quality across multiple dimensions. The **authority** of the linking page (its own PageRank, domain strength) is the primary value multiplier. A single link from a high-authority editorial source (a major news publication, a university research page, an industry association) is worth far more than hundreds of links from obscure, low-quality directories.

**Topical relevance** is the second critical dimension. A link from a page covering the same or closely related topic passes more relevant authority than a link from an unrelated domain. A cycling gear page linking to another cycling gear page passes highly relevant authority; a casino site linking to the same cycling page passes much weaker (and potentially suspicious) authority.

**Anchor text** is the clickable text used for the link. Keyword-relevant anchor text historically sent strong topical signals, but anchor text over-optimization (using the exact target keyword as anchor text across hundreds of links) is a primary spam signal that Penguin targets. A natural backlink profile has a distribution dominated by branded anchors (company/site name), naked URLs, and generic anchors ("click here," "read more"), with keyword anchors as a minority.

The `rel` attribute modifies link equity transmission. `rel="nofollow"` was traditionally binary — no equity pass — but Google changed this in 2019 to treat `nofollow`, `ugc`, and `sponsored` as **hints** rather than directives. Google now exercises discretion about whether to follow these links. In practice, `nofollow` links are generally not credited as ranking signals, though they may still provide some referral and discovery value.

## Key Attributes

**Quality Hierarchy (highest to lowest value):** Editorial in-content links from high-authority topically relevant domains > Resource page links > Directory links (niche, quality directories) > Forum/UGC links > Footer/sidebar links > Links from irrelevant domains.

**Spam Signals:** Any link acquired through payment, exchange, or manipulation (link farms, PBNs, mass guest posts on low-quality sites) violates Google's spam policies. Google's SpamBrain and Penguin systems actively identify and neutralize such links.

**Link Disavow:** Google provides a Disavow Links tool in Search Console for publishers to flag links they believe are harmful to their profile. Use is recommended only for sites that have received manual actions for link spam or have clearly identifiable toxic link patterns.

## Optimization Relevance

Legitimate link acquisition strategies include: earning links through high-quality original content (data studies, research, tools), digital PR (press coverage, journalist outreach), guest posting on genuinely authoritative and relevant sites, reclaiming unlinked brand mentions, broken link building (replacing dead links on other sites), and creating shareable resources (calculators, templates, infographics) that attract organic links.

Reciprocal link schemes, link buying, and PBNs carry significant algorithmic and manual penalty risk and should be avoided.

## Status & Evolution

**Current Status:** Active — among the top 3 ranking signals.

Despite 25 years of algorithm evolution, backlinks remain one of Google's most important signals. Google employees have confirmed links as a top-3 ranking factor as recently as 2016. The 2024 Google API documentation leak provided further evidence that link signals (via "siteAuthority" and related attributes) remain deeply embedded in the ranking system. The weight of backlinks relative to other signals (particularly content quality and E-E-A-T) may be declining incrementally, but they remain foundational.

## Evidence & Sources

- [Google Search Spam Policies — Link Spam](https://developers.google.com/search/docs/essentials/spam-policies#link-spam) — Google Search Central, retrieved 2026-06-09
- [PageRank — Wikipedia](https://en.wikipedia.org/wiki/PageRank) — Wikipedia, retrieved 2026-06-09
