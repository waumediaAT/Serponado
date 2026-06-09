---
entityId: "job-listings"
name: "Job Listings (Google for Jobs)"
type: SERP_Feature
schemaType: DefinedTerm
version: 1.0.0
status: active
aliases:
  - "Google for Jobs"
  - "Job Postings"
  - "Job Search Results"
  - "Job Rich Results"
sameAs:
  - "https://developers.google.com/search/docs/appearance/structured-data/job-posting"
parent: "serp-feature"
namespace: "serp-features"
relations:
  - predicate: REQUIRES
    target: "structured-data"
    description: "JobPosting schema required for Google for Jobs inclusion"
  - predicate: TRIGGERED_BY
    target: "informational"
    description: "Job search queries are a distinct search intent category"
attributes:
  position: "Top of SERP — below ads, above organic results for job queries"
  trigger_intents: [informational, transactional]
  ctr_impact: high
  schema_required: "JobPosting"
  owned_by: "Google"
  introduced: "2017"
  display: "Job title, company, location, salary range, posting date, Apply button"
  aggregates_into: "Google Jobs vertical search"
  required_schema_properties:
    - title
    - description
    - datePosted
    - hiringOrganization
    - jobLocation
  recommended_schema_properties:
    - baseSalary
    - employmentType
    - validThrough
    - skills
    - qualifications
  mobile_display: true
  desktop_display: true
evidence:
  - source: "https://developers.google.com/search/docs/appearance/structured-data/job-posting"
    title: "JobPosting Structured Data"
    publisher: "Google Search Central"
    retrieved: "2026-06-09"
    relevanceScore: 1.0
  - source: "https://blog.google/products/search/connecting-more-americans-jobs/"
    title: "Connecting Americans to Jobs"
    publisher: "Google Blog"
    retrieved: "2026-06-09"
    relevanceScore: 0.9
lastReviewed: "2026-06-09"
---

# Job Listings (Google for Jobs)

## Definition

Job Listings (Google for Jobs) is a SERP feature and vertical search surface displaying job postings from employer websites, job boards, and staffing agencies in response to employment-related queries. Powered by `JobPosting` structured data, it aggregates listings from across the web into a unified job search interface at the top of the SERP.

## Description

Google for Jobs launched in 2017, bringing Google's data aggregation capabilities to employment search — a market previously dominated by dedicated job boards (Indeed, LinkedIn, ZipRecruiter). By extracting `JobPosting` structured data from employer websites and third-party job boards, Google created a universal job search interface directly within the SERP.

The feature appears as a prominent box at the top of the SERP for job-related queries, showing 3–5 listings with expandable detail. Clicking a listing opens a detail view with the full job description, salary information (if provided), company information, and a direct application link.

For employers and recruiters, `JobPosting` schema on job listing pages enables free visibility in Google for Jobs without requiring a listing on any specific job board. The required fields (`title`, `description`, `datePosted`, `hiringOrganization`, `jobLocation`) are minimal; adding optional fields like `baseSalary` and `employmentType` significantly improves listing visibility and click rates.

## Key Attributes

**Schema Required:** `JobPosting` with required and recommended properties.

**Salary Display:** Google strongly encourages including `baseSalary` — listings with salary information receive higher visibility.

**Expiry:** `validThrough` property ensures expired listings are removed; without it, outdated postings persist.

## Status & Evolution

**Current Status:** Active. Available in 100+ countries.

## Evidence & Sources

- [JobPosting Structured Data](https://developers.google.com/search/docs/appearance/structured-data/job-posting) — Google Search Central, retrieved 2026-06-09
- [Connecting Americans to Jobs](https://blog.google/products/search/connecting-more-americans-jobs/) — Google Blog, retrieved 2026-06-09
