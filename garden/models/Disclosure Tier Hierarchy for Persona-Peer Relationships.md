---
created: 2026-03-19
author: Christopher Allen
brief_summary: "Inter-Face Protocol organizes information sharing through a six-tier hierarchy from public to close, applied per persona-peer pair. Each tier defines a boundary the agent respects. Tiers are self-declared, mutual but not symmetric, and deepen over time. The model maps how disclosure, persona, and peer identity intersect."
tagline: "How do disclosure tiers, personas, and peer relationships intersect to govern information sharing?"
---

- is_a::[[Model Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]

# Disclosure Tier Hierarchy for Persona-Peer Relationships

Disclosure in Inter-Face Protocol is not a single setting. It is a **three-dimensional mapping**: for each (persona, peer) pair, a disclosure tier governs what information the agent may share.

## The Structure

```
Disclosure Map: (persona, peer) → tier

Example:
  (blockchain-researcher, Alice) → professional-open
  (blockchain-researcher, Bob)   → professional
  (game-designer, Alice)         → personal
  (game-designer, Bob)           → community-trust
```

The six tiers form a hierarchy from narrow to broad sharing:

```
public → professional → professional-open → community-trust → personal → close
```

Each tier represents a **boundary the agent respects** — not a permission a platform grants. The person controls their own boundaries through their own agent.

## Three Properties

**Self-declared.** Each participant declares their own disclosure tier. No external authority assigns it.

**Mutual but not symmetric.** Both parties declare tiers, but the tiers need not match. Alice may share at "professional" with Bob while Bob shares at "personal" with Alice. Each controls their own boundary.

**Progressive.** Tiers start narrow and may deepen as the relationship matures. Tiers should not downgrade mid-exchange — that signals a trust violation.

## Why This Matters

The persona-peer-tier mapping is what makes IFP's disclosure model richer than binary public/private or platform-controlled privacy settings. The same person shares different things with the same peer depending on which context (persona) is active. This reflects how human relationships actually work — you share different things with a friend depending on whether you are talking about work or personal life.

## Sources

- [IFP-12: Personas and Disclosure Tiers](../../ifp-12-personas.md), Section 3.3
- [IFP-3: Inter-Face Message Format](../../ifp-3-message-format.md), disclosure field

## Relations

- relates_to::[[Persona as Emergent Context Cluster]]
  - Personas are one axis of the disclosure map — each persona has its own tier settings.

- relates_to::[[Disclosure Tier as Information Sharing Boundary]]
  - The gloss defining what a disclosure tier means.

- relates_to::[[Progressive Authentication as Trust Deepening]]
  - Authentication levels and disclosure tiers deepen in parallel — deeper auth enables deeper disclosure.

- relates_to::[[Coercion Resistance as Meta-Lens]]
  - Self-declared disclosure tiers protect against the visibility-to-coercion escalation chain.

- relates_to::[[Choice Architecture and Exit Rights]]
  - The person can always narrow their disclosure or stop sharing — exit rights apply to information sharing.
