---
entityId: "bert"
name: "BERT"
type: Algorithm
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Bidirectional Encoder Representations from Transformers"
  - "BERT Update"
  - "Google BERT"
sameAs:
  - "https://en.wikipedia.org/wiki/BERT_(language_model)"
  - "https://blog.google/products/search/search-language-understanding-bert/"
parent: "google-algorithm"
namespace: "algorithms"
relations:
  - predicate: REPLACES
    target: "rankbrain"
    description: "BERT handles query understanding for a broader set of queries than RankBrain"
  - predicate: RELATED_TO
    target: "mum"
    description: "MUM is BERT's successor for multimodal, multilingual understanding"
  - predicate: AFFECTS
    target: "organic-result"
    description: "BERT changed result sets for ~10% of queries at launch"
attributes:
  launched: "2019-10"
  announced: "2019-10-25"
  type: nlp
  model_architecture: "Transformer — bidirectional encoder"
  target: "Query and content language understanding, semantic context"
  scope: "query, content"
  query_coverage: "~10% of English queries at launch; expanded to all languages"
  key_capability: "Understanding contextual meaning of words in both query and page content"
  training: "Pre-trained on Wikipedia and BookCorpus, fine-tuned for search tasks"
  open_source: true
  origin_paper: "Devlin et al., 2018 (Google AI Language)"
  incorporated_into_core: true
evidence:
  - source: "https://blog.google/products/search/search-language-understanding-bert/"
    title: "Understanding Searches Better Than Ever Before"
    publisher: "Google Blog"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
    quote: "With BERT, we can better understand the nuance and context of words in searches."
  - source: "https://en.wikipedia.org/wiki/BERT_(language_model)"
    title: "BERT (language model) — Wikipedia"
    publisher: "Wikipedia"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# BERT

## Definition

BERT (Bidirectional Encoder Representations from Transformers) is a transformer-based NLP model that Google deployed in Search in October 2019. It enables Google to understand the full contextual meaning of words in a query — particularly the role of prepositions and subtle phrasing differences — rather than treating queries as bags of keywords.

## Description

BERT represented the largest qualitative step change in Google's query understanding between Hummingbird (2013) and MUM (2021). The key innovation is **bidirectionality**: unlike earlier language models that processed text left-to-right or right-to-left, BERT reads the entire sentence simultaneously in both directions, capturing full contextual relationships between all words.

The practical impact is best illustrated by Google's example: the query "2019 brazil traveler to usa need a visa" — the word "to" is critical. A non-contextual model might ignore it; BERT understands that "to" establishes the direction of travel (Brazil→USA), not USA→Brazil. Before BERT, Google returned results about US citizens traveling to Brazil. After BERT, it correctly returned results about Brazilian citizens traveling to the US.

BERT processes both the query and the page content it evaluates, enabling better matching between what users ask and what pages actually answer — even when exact keyword matches don't exist.

Google published BERT as an open-source model in 2018, making it widely accessible to researchers and developers. Its deployment in Search in 2019 affected approximately 1 in 10 English queries — a significant scale given Google processes ~8.5 billion queries per day.

## Key Attributes

**Architecture:** Transformer encoder — bidirectional, attention-based. Pre-trained on 3.3 billion words.

**Scope:** Applied to both query understanding and content evaluation.

**Impact:** Most significant for queries where small words (prepositions, negations, conjunctions) change meaning — conversational queries, YMYL research queries, complex multi-concept queries.

## Status & Evolution

**Current Status:** Active — part of Google's core NLP stack, supplemented by MUM and Gemini for more complex tasks.

BERT remains a foundation of Google's language understanding. Subsequent models (MUM, Gemini) are used for more complex, multi-step tasks, while BERT handles the broad middle of standard query understanding.

## Evidence & Sources

- [Understanding Searches Better Than Ever Before](https://blog.google/products/search/search-language-understanding-bert/) — Google Blog, retrieved 2026-06-09
- [BERT (language model) — Wikipedia](https://en.wikipedia.org/wiki/BERT_(language_model)) — Wikipedia, retrieved 2026-06-09
