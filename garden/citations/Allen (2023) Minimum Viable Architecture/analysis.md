---
created: 2026-03-19
author: Christopher Allen
brief_summary: "Analysis of how the minimum viable architecture principle applies to Inter-Face Protocol's design decisions — distinguishing load-bearing architectural choices from tactical decisions that could be deferred or changed."
tagline: "Which IFP decisions are load-bearing architecture and which are deferrable tactical choices?"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]

# Analysis: Minimum Viable Architecture Applied to Inter-Face Protocol

The minimum viable architecture principle asks: which decisions are hard to reverse, and which can be deferred until you know more? Applied to IFP, this produces a clear separation.

## Load-Bearing Decisions (Hard to Reverse)

These are the decisions that would reshape the protocol if changed. They are the minimum viable architecture:

**Gossip-as-filter framing** (IFP-1). The entire protocol exists to filter attention, not to connect people. Changing this would make IFP a different system.

**Temperature model** (IFP-1). Cool/warm/hot cadence shapes rate limiting, capability availability, and escalation patterns across every spec. Removing temperature would require redesigning the protocol stack.

**Human legibility constraint** (IFP-1). Every agent action must be auditable by a human in a text editor. This rules out binary formats, opaque compression, and any exchange that is not human-readable. Relaxing this constraint would fundamentally alter the trust model.

**Agent-age protocol principles** (IFP-1). The seven principles — especially replacing Postel's Law with clarity-over-tolerance — commit IFP to a design philosophy that shapes error handling, version negotiation, and capability discovery across every spec.

**Conversation phase model** (IFP-3). Greeting → context → probe → recommend → close → error is the social backbone of every exchange. Changing the phases would require rewriting IFP-3, IFP-9, IFP-11, and IFP-12.

**Dual representation architecture** (IFP-3/4). Human-readable YAML+NL paired with machine-processable JSON. Removing either representation would break either human legibility (losing IFP-3) or cryptographic operations (losing IFP-4).

**Progressive trust model** (IFP-5/12). Authentication and disclosure deepen together. Flattening this to binary (trusted/untrusted) would eliminate progressive authentication, disclosure tiers, and much of the persona model.

## Tactical Decisions (Easy to Change)

These are implementation choices that could be refined without reshaping the protocol:

- **Specific envelope field names** (IFP-3/4) — renaming `disclosure` to `sharing_level` changes no semantics
- **Rate limiting defaults** (IFP-6) — 10 msg/min cool, 60 msg/min hot are heuristics, not architecture
- **Message size limit** (IFP-6) — 1 MB is a reasonable default, not a design commitment
- **Endpoint paths** (IFP-6) — `/.well-known/iface/inbox` follows convention but could change
- **Retry backoff schedule** (IFP-6) — exponential backoff parameters are tuning, not design
- **Relay persistence duration** (IFP-8) — 7 days is a default, not an invariant

## Uncertain Decisions

Some decisions sit between architectural and tactical. The inquiries in this garden patch examine these:

- **Four authentication levels** — Are the boundaries between levels load-bearing or refinable? (See [[Granularity of Progressive Authentication Stages]])
- **Six disclosure tiers** — Are the tier names and count architectural or conventional? (See [[Disclosure Spectrum as Discrete Tiers or Continuous Range]])
- **Six conversation phases** — Is the phase decomposition load-bearing or refinable? (See [[Social Phase Decomposition in Trust-Building Protocols]])
- **Natural language bodies** — Is NL-for-bodies a minimum viable architecture choice or a deferrable bet? (See [[Structured Schema vs Natural Language for Agent Message Content]])
- **Eleven application platforms** — Are these architectural categories or illustrative examples? (See [[Organizing Principle for Agent Application Domains]])

## Sources

- [[Allen (2023) Minimum Viable Architecture]] — the source principle
- [IFP-1 through IFP-12](../../) — the decisions being analyzed
