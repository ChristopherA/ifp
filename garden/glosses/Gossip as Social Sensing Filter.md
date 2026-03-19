---
created: 2026-03-19
author: Christopher Allen
brief_summary: "In Inter-Face Protocol, 'gossip' is not chatter — it is a filtering mechanism. Agents exchange context pairwise to detect overlaps worth human attention. The value is in what gossip does not surface. Most exchanges produce silence; recommendations emerge only when the overlap is actionable, timely, and specific."
tagline: "Gossip filters attention rather than broadcasting information"
---

- is_a::[[Gloss Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]

# Gossip as Social Sensing Filter

In everyday language, gossip means informal talk about other people. Inter-Face Protocol reclaims the term with a precise meaning: gossip is a **filtering mechanism** for human attention.

Agents exchange context pairwise — not to broadcast, but to detect overlaps that warrant human conversation. The system's value is measured by what it does *not* surface. Most gossip exchanges produce silence. A recommendation reaches a human only when the overlap is actionable, timely, and specific enough to justify the cost of human attention.

This framing inverts the assumption behind social platforms, which measure success by engagement — more messages, more notifications, more time spent. Inter-Face measures success by the quality of the filter: how few recommendations reach the human, and how often those few are worth acting on.

The gossip-as-filter concept is load-bearing for Inter-Face Protocol. It shapes the temperature model (most gossip is cool — weekly background exchange), the phase model (gossip progresses through greeting → context → probe → recommend → close), and the conviction that [[Filtering Is More Valuable Than Connecting]].

## Sources

- [IFP-1: Philosophy and Design Principles](../../ifp-1-philosophy.md), Sections 1-3
- [IFP-3: Inter-Face Message Format](../../ifp-3-message-format.md), conversation phases

## Relations

- defines_vocabulary_from::[[Inter-Face Protocol]]
  - "Gossip" is IFP's name for pairwise agent exchange.

- grounds::[[Filtering Is More Valuable Than Connecting]]
  - The gossip-as-filter concept is the operational mechanism behind the conviction.

- relates_to::[[Conversation Temperature as Protocol Cadence Spectrum]]
  - Most gossip operates at cool temperature — weekly background exchange.

- relates_to::[[Recommendation as Surfaced Opportunity]]
  - Recommendations are the output of successful gossip — what survives the filter.
