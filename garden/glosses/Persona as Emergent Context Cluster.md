---
created: 2026-03-19
author: Christopher Allen
brief_summary: "In Inter-Face Protocol, a persona is a coherent subset of a person's full context — not a mask or role, but a genuine reflection of how interests naturally cluster around communities, projects, and relationships. Personas emerge from agent observation of communication patterns rather than requiring explicit enumeration by the human."
tagline: "Personas reflect how human interests naturally cluster, not how systems categorize people"
---

- is_a::[[Gloss Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]

# Persona as Emergent Context Cluster

Systems that handle multiple user contexts typically require the user to define roles upfront: "work," "personal," "hobby." Inter-Face Protocol takes a different approach. A persona is a **coherent subset** of a person's full context, and it **emerges from observation** rather than requiring explicit declaration.

An agent notices that certain topics, contacts, and projects cluster together. A person's blockchain work involves different people, different disclosure comfort levels, and different vocabulary than their cooperative game design work. The agent recognizes these clusters and treats them as distinct contexts — each with its own disclosure tier settings per peer.

This matters because people do not experience their interests as cleanly separated categories. A contact from the blockchain world might also be relevant to cooperative game design. Forced categorization either creates false boundaries or requires the user to maintain overlapping role definitions. Emergent personas accommodate fuzzy boundaries and cross-context serendipity.

The persona is not an identity. The agent identifier (from IFP-5 and IFP-10) stays the same across all personas. Trust is in the person, not the persona. What changes per persona is the disclosure tier — how much context the agent shares with a given peer in a given context.

## Sources

- [IFP-12: Personas and Disclosure Tiers](../../ifp-12-personas.md), Sections 2-4
- Victoria Tanner's insight on persona emergence (IFP-12 acknowledgments)

## Relations

- defines_vocabulary_from::[[Inter-Face Protocol]]
  - "Persona" is IFP's term for emergent context clusters.

- grounds::[[Personas Emerge from Observation Not Enumeration]]
  - The conviction that prescribed enumeration misrepresents how people experience context.

- relates_to::[[Disclosure Tier Hierarchy for Persona-Peer Relationships]]
  - Disclosure tiers are persona-specific — each persona has its own disclosure settings per peer.

- relates_to::[[Progressive Disclosure Over Eager Loading]]
  - Persona-specific disclosure follows the same progressive pattern — share narrowly first, deepen as trust builds.
