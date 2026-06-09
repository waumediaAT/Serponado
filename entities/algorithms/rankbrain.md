---
entityId: "rankbrain"
name: "RankBrain"
type: Algorithm
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Google RankBrain"
  - "RankBrain Algorithm"
sameAs:
  - "https://en.wikipedia.org/wiki/RankBrain"
  - "https://blog.google/products/search/rankbrain/"
parent: "google-algorithm"
namespace: "algorithms"
relations:
  - predicate: RELATED_TO
    target: "bert"
    description: "BERT extended query understanding begun by RankBrain"
  - predicate: AFFECTS
    target: "organic-result"
    description: "RankBrain influences result ranking for novel and ambiguous queries"
  - predicate: RELATED_TO
    target: "informational"
    description: "RankBrain particularly impacts complex informational queries"
attributes:
  launched: "2015-10"
  type: ml
  announced_by: "Greg Corrado, Google Senior Research Scientist"
  target: "Query interpretation for novel and ambiguous queries"
  scope: "query"
  coverage: "~15% of daily queries at launch (2015 figure); all queries in signal weighting"
  mechanism: "Word vector / embedding model — maps novel queries to semantically similar known queries"
  ranking_signal_rank: "3rd most important signal (as stated by Google in 2015)"
  ml_type: "Supervised machine learning with word vectors"
  incorporated_into_core: null
evidence:
  - source: "https://en.wikipedia.org/wiki/RankBrain"
    title: "RankBrain — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
  - source: "https://blog.google/products/search/rankbrain/"
    title: "How RankBrain Helps Google Search Understand The World"
    publisher: "Google Blog"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
lastReviewed: "2026-06-09"
---

# RankBrain

## Definition

RankBrain is Google's first machine learning component deployed directly in the search ranking system, announced in October 2015. It interprets the meaning of search queries — particularly novel, ambiguous, or conversational queries Google has never seen before — by mapping them to semantically similar queries, enabling Google to surface relevant results even without exact keyword matches.

## Description

Before RankBrain, Google handled novel queries (roughly 15% of daily searches are queries Google has never seen before) using hand-written algorithmic rules. These rules were brittle — they could not adapt to new phrasing patterns or account for the full semantic context of conversational queries.

RankBrain introduced machine learning into query interpretation. Using word vector representations (embeddings), RankBrain converts words into mathematical vectors in a high-dimensional semantic space, where semantically related words cluster together. When Google encounters an unfamiliar query, RankBrain identifies its nearest neighbors in this vector space — queries with similar meaning — and uses their ranking patterns to inform results for the new query.

At the time of its announcement, Google's Greg Corrado stated that RankBrain had become the third most important signal in Google's ranking algorithm, behind only links and content. This was a remarkable statement given the hundreds of other signals Google uses.

RankBrain is also a learning system: it observes how users interact with results and adjusts its query-result mapping accordingly. This feedback loop means RankBrain continuously improves its query understanding over time based on actual user satisfaction signals.

With the introduction of BERT (2019) and MUM (2021), RankBrain's role in query understanding has been supplemented by more powerful NLP models. However, RankBrain remains active as a general-purpose query understanding component.

## Key Attributes

**Primary Function:** Handling novel/never-before-seen queries by finding semantic analogues in the known query space.

**Technology:** Word vector embeddings (similar to Word2Vec methodology) mapping words to semantic vector space.

**Scope:** Active on all queries, but most impactful for complex, conversational, or first-time queries.

## Status & Evolution

**Current Status:** Active — supplemented but not replaced by BERT and MUM.

RankBrain was the first major deployment of ML in Google's ranking, opening the door for subsequent systems (BERT, MUM, Gemini). It remains part of the ranking stack but shares query understanding responsibilities with more powerful transformer-based models.

## Evidence & Sources

- [RankBrain — Wikipedia](https://en.wikipedia.org/wiki/RankBrain) — Wikipedia, retrieved 2026-06-09
- [How RankBrain Helps Google Search Understand The World](https://blog.google/products/search/rankbrain/) — Google Blog, retrieved 2026-06-09
