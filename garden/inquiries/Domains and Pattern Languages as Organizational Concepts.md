---
created: 2026-03-06
author: Christopher Allen
brief_summary: "Investigates the relationship between domains (knowledge area indexes across all form types) and pattern languages (collections of patterns organized by scale within a domain). Meeples Together, Group Works, and Rust coding patterns are all pattern languages in different domains — are pattern languages a specialized view of a domain, or a distinct organizational concept?"
tagline: "Pattern languages organize patterns by scale within a domain — are they a view, a subset, or something distinct?"
formatted: "2026-03-14"
---

- is_a::[[Inquiry Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]
- in_domain::[[Synpraxis]]

# Domains and Pattern Languages as Organizational Concepts

## Thesis

A domain page indexes all form types within a knowledge area — principles, patterns, models, glosses, cases, and more. A pattern language (in the Alexandrian sense) is a collection of patterns within a domain, organized by scale and connected by references. The garden currently has domain pages but no pattern language structures. As the Synpraxis domain grows and cooperative game design patterns accumulate, the relationship between these two organizing concepts needs to be defined.

## Known Examples

- **Meeples Together** — pattern language for cooperative game design (Allen & Appelcline). Patterns organized from game-level to component-level. Would live within the Synpraxis domain.
- **Group Works** — pattern language for group process (Group Works Project). Patterns for facilitation and collaboration. Also Synpraxis domain.
- **A Pattern Language** — Alexander's original: 253 patterns from region-level to room-level in the built environment domain.
- **Rust coding patterns** — informal pattern collection in a software domain. Less structured than Alexandrian but recognizable as a pattern language.

These inhabit different domains but share the pattern language structure: patterns connected by scale, each referencing patterns above and below it.

## Open Questions

1. **View vs structure**: Is a pattern language just "all the patterns in domain X, sorted by scale"? Or does it have its own structural contract — a language has a generative sequence that a flat list of patterns doesn't?

2. **Domain page extension**: Should a domain page have a "Pattern Language" section that organizes its patterns by scale? Or should pattern languages be separate forms (a new form type, or a specialized reference)?

3. **Cross-domain patterns**: Some patterns appear in multiple pattern languages (e.g., "trust building" patterns in both cooperative game design and group process). How does the garden handle patterns that belong to multiple languages within different domains?

4. **Relationship to Synpraxis**: The Synpraxis domain explicitly lists pattern languages as a cross-cutting mechanism. Does that mean Synpraxis is the meta-domain for pattern language methodology, while individual pattern languages live in their specific domains?

## Sources

- [[Deep Context as an Architecture for Captured Reasoning]], "Open Questions for Discussion" #10 (lines 465-466)
- [[Synpraxis]] — lists pattern languages as cross-cutting mechanism
- Christopher Alexander, *A Pattern Language* (1977) — the original generative pattern language
- Christopher Allen & Shannon Appelcline, *Meeples Together* (2019) — cooperative game design patterns

## Relations

- relates_to::[[Synpraxis]]
  - Pattern languages for cooperation/collaboration are Synpraxis artifacts.

- relates_to::[[Domain Form]]
  - Questions whether domain pages should incorporate pattern language structure.

- relates_to::[[Pattern Form]]
  - Pattern languages are collections of pattern instances organized by scale.
