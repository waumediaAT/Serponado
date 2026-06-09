---
entityId: "e-e-a-t"
name: "E-E-A-T"
type: Ranking_Factor
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Experience Expertise Authoritativeness Trustworthiness"
  - "E-A-T"
  - "EAT"
  - "Double-E-A-T"
sameAs:
  - "https://developers.google.com/search/docs/fundamentals/creating-helpful-content"
  - "https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf"
parent: "ranking-factor"
namespace: "ranking-factors"
relations:
  - predicate: CONTAINS
    target: "content-quality"
    description: "Content quality is a primary dimension of E-E-A-T"
  - predicate: RELATED_TO
    target: "helpful-content"
    description: "Helpful Content System operationalizes E-E-A-T at scale"
  - predicate: AFFECTS
    target: "organic-result"
    description: "E-E-A-T signals influence ranking, particularly for YMYL content"
  - predicate: RELATED_TO
    target: "author-information"
    description: "Author entities and bylines are key E-E-A-T signals"
attributes:
  factor_type: "on-page, off-page, entity"
  weight: high
  confirmed_by:
    - "Google Search Quality Evaluator Guidelines"
    - "Google Search Central documentation"
  ymyl_significance: "Highest — E-E-A-T requirements are strictest for YMYL content"
  components:
    - name: Experience
      added: "December 2022"
      definition: "First-hand or life experience with the topic"
    - name: Expertise
      definition: "Formal knowledge, skills, or demonstrated mastery"
    - name: Authoritativeness
      definition: "Recognition as an authority by peers and authoritative sources"
    - name: Trustworthiness
      definition: "Honesty, accuracy, transparency, and safety"
  ymyl_categories:
    - Health and medical
    - Financial advice
    - Legal advice
    - News and current events
    - Safety information
    - Government and civics
  affects_feature:
    - organic-result
    - knowledge-panel
    - ai-overview
evidence:
  - source: "https://developers.google.com/search/docs/fundamentals/creating-helpful-content"
    title: "Creating Helpful, Reliable, People-First Content"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
    quote: "Google's systems are designed to reward helpful content that demonstrates E-E-A-T."
  - source: "https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf"
    title: "Search Quality Evaluator Guidelines"
    publisher: "Google"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
lastReviewed: "2026-06-09"
---

# E-E-A-T

## Definition

E-E-A-T stands for Experience, Expertise, Authoritativeness, and Trustworthiness — Google's quality evaluation framework used to assess whether content is created by people who have the relevant knowledge, credentials, and integrity to provide reliable information on a topic. It is central to Google's Search Quality Evaluator Guidelines and heavily influences rankings for YMYL (Your Money Your Life) content.

## Description

E-E-A-T is not a single algorithmic signal — it is a multidimensional quality framework that Google's search quality raters apply when manually evaluating search results, and which Google's automated systems attempt to approximate through hundreds of measurable signals.

The framework was originally E-A-T (without the first "E" for Experience) when first codified in the Search Quality Evaluator Guidelines. In December 2022, Google added the first "E" for **Experience**, reflecting the post-Helpful Content era's emphasis on first-hand knowledge. A medical article written by a practicing physician who treats patients carries more Experience than one written by a health copywriter, even if both have similar credentials on paper.

**Expertise** refers to formal knowledge and demonstrated skill in a topic area. This can be formal (medical degree, legal certification, engineering license) or informal (a hobbyist with 20 years of documented practice, a veteran mechanic with no formal certification). Google's systems use author entity recognition, linked credentials, and citation patterns to assess expertise.

**Authoritativeness** is the external recognition of expertise — do authoritative sources in the same domain link to, cite, or reference this content or author? It is the off-page, social-proof component of E-E-A-T, most closely correlated with traditional link authority metrics but extending to editorial mentions, citations, and industry recognition.

**Trustworthiness** is the master signal — Google explicitly states that trustworthiness is the most important of the four. A page can demonstrate experience, expertise, and authoritativeness but still be untrustworthy if it is deceptive, sensationalist, hides funding or conflicts of interest, or is technically insecure (no HTTPS).

E-E-A-T standards are highest for **YMYL (Your Money Your Life)** content — pages that can significantly impact a user's health, financial stability, safety, or major life decisions. Medical symptom pages, financial investment advice, legal rights information — these are held to the strictest E-E-A-T standards because the cost of bad information is highest.

## Key Attributes

**Components:**
- **Experience** — First-hand, lived, or practical experience with the topic
- **Expertise** — Knowledge depth, credentials, demonstrable mastery
- **Authoritativeness** — External recognition, citations, editorial links, reputation
- **Trustworthiness** — Accuracy, honesty, transparency, security, source attribution

**YMYL Categories (highest E-E-A-T bar):** Health, medical, financial, legal, safety, government, major life decisions.

**Measurement:** Not a single score — evaluated through a constellation of signals including author entity recognition, linked credentials, backlink quality and topical alignment, about page transparency, editorial policies, and historical accuracy track record.

## Optimization Relevance

Building E-E-A-T is a long-term program, not a quick fix. Core actions: establish author entities (author bio pages with credentials, links to author's social profiles and academic work, Knowledge Graph entity for notable authors), create comprehensive About and Contact pages, develop editorial policies and corrections procedures, build topically relevant backlinks from authoritative sources, use first-person perspective and personal experience language where appropriate, and cite credible sources with accurate attribution.

For YMYL content specifically: medical content should have physician review; financial content should have CFA/CFP credentials visible; legal content should indicate jurisdiction and attorney review. The absence of authorship signals on YMYL content is a strong negative signal.

## Status & Evolution

**Current Status:** Active — core quality framework with expanding scope.

E-A-T was formalized in Google's Search Quality Evaluator Guidelines in 2014. The addition of the Experience dimension in December 2022 reflected the Helpful Content era's emphasis on genuine human experience over algorithmically generated or secondhand content. As AI-generated content proliferates, E-E-A-T signals (particularly Experience and Trustworthiness) are expected to grow in importance as differentiators between human-expert content and AI-generated content.

## Evidence & Sources

- [Creating Helpful, Reliable, People-First Content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) — Google Search Central, retrieved 2026-06-09
- [Search Quality Evaluator Guidelines](https://static.googleusercontent.com/media/guidelines.raterhub.com/en//searchqualityevaluatorguidelines.pdf) — Google, retrieved 2026-06-09
