---
created: 2026-03-19
author: Christopher Allen
brief_summary: "A disclosure tier defines what information an agent may share with a specific peer in a specific persona context. IFP defines six tiers from public to close, each representing a boundary the agent respects when exchanging context. Tiers are self-declared, mutual but not necessarily symmetric, and deepen over time as trust builds."
tagline: "Disclosure tiers are boundaries agents respect, not permissions platforms grant"
---

- is_a::[[Gloss Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]

# Disclosure Tier as Information Sharing Boundary

A disclosure tier is a **boundary** that defines what information an agent may share with a particular peer. Unlike platform privacy settings (which a company controls and may change), disclosure tiers are **self-declared** by each participant and respected by their own agent.

IFP defines six tiers, from narrow to broad sharing:

| Tier | Scope | What the agent may share |
|------|-------|-------------------------|
| **public** | Anyone | Published information, broad interests |
| **professional** | Colleagues, peers | Professional context, work interests |
| **professional-open** | Trusted colleagues | Project challenges, work-in-progress |
| **community-trust** | Trusted community | Community-specific context |
| **personal** | Friends | Life events, personal interests |
| **close** | Deep friends | Vulnerabilities, formative experiences |

Two properties distinguish IFP disclosure from platform privacy:

**Mutual but not symmetric.** Both parties declare tiers, but they need not match. Alice may share at "professional" with Bob while Bob shares at "personal" with Alice. Each person controls their own boundary.

**Persona-specific.** The same person may have different disclosure tiers with the same peer across different personas. A person's blockchain persona might share at "professional" with a contact, while their game design persona shares at "personal" with the same person.

Disclosure tiers connect to the progressive trust model: tiers start narrow and may deepen as the relationship matures, but should not downgrade mid-exchange.

## Sources

- [IFP-12: Personas and Disclosure Tiers](../../ifp-12-personas.md), Section 3.3
- [IFP-3: Inter-Face Message Format](../../ifp-3-message-format.md), disclosure field

## Relations

- defines_vocabulary_from::[[Inter-Face Protocol]]
  - "Disclosure tier" is IFP's mechanism for information sharing boundaries.

- relates_to::[[Disclosure Tier Hierarchy for Persona-Peer Relationships]]
  - The model form that maps the full tier structure.

- relates_to::[[Progressive Authentication as Trust Deepening]]
  - Authentication levels and disclosure tiers deepen in parallel.

- relates_to::[[Choice Architecture and Exit Rights]]
  - Self-declared disclosure tiers preserve the person's right to control their own boundaries.

- relates_to::[[Coercion Resistance as Meta-Lens]]
  - Disclosure tiers protect against the visibility → legibility → control → coercion escalation chain.
