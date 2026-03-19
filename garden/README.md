# Deep Context Architecture — A Garden Lens on Inter-Face Protocol

This folder contains a **mini-garden** — a small collection of structured knowledge nodes that express Inter-Face Protocol concepts through [Deep Context Architecture](domains/Deep%20Context%20Architecture.html) garden forms.

This is not a critique of the IFP specifications. It is an alternative lens — a way to see connections between IFP's design decisions and broader patterns in identity, trust, collaboration, and protocol design. Peter's specs remain untouched. The garden sits alongside them.

## What Are Garden Forms?

A garden is a collection of **typed nodes** connected by **labeled edges** (predicate links). Each node belongs to a **form type** that determines its structural contract — what question it answers and how it is organized.

Where a traditional document says "here is information about X," a garden node says "here is a **pattern** / **decision** / **conviction** / **model** that answers a specific question about X, and here is how it connects to other nodes."

### Form Types Used in This Mini-Garden

| Form Type | Core Question | Example |
|-----------|--------------|---------|
| **Model** | "How do these elements relate to each other?" | Temperature spectrum, disclosure tiers |
| **Conviction** | "What do we believe is true about the world?" | Filtering over connecting |
| **Decision** | "Why did we choose this over alternatives?" | Clarity over tolerance |
| **Pattern** | "What resolves this recurring tension?" | Errors as negotiation |
| **Principle** | "What must we always or never do?" | Auditable intermediaries |
| **Gloss** | "What does this concept mean through an interpretive lens?" | Gossip as social sensing |
| **Boundary** | "Where does this system's authority end?" | Delegated decision authority |
| **Inquiry** | "What should we think about X?" | Group deliberation mechanism |
| **Domain** | "What knowledge area does this cluster belong to?" | Synpraxis |

Full form type definitions are in [forms/](forms/).

### Predicate Links

Nodes connect through typed predicates — labeled directed edges that say *how* two nodes relate, not just *that* they relate:

```
is_a::[[Pattern Form]]           — classification
in_domain::[[Self-Sovereign Identity]]  — knowledge area
relates_to::[[Progressive Authentication as Trust Deepening]]  — lateral connection
grounds::[[Filtering Is More Valuable Than Connecting]]  — foundational support
```

These are written as `predicate::[[Target]]` in the node body. In a full garden with Obsidian, these become navigable graph edges. Here in markdown, they serve as structured metadata showing the knowledge network.

### Wikilink Markers

Not every wikilink target is in this patch. Markers distinguish what's here from what's elsewhere:

| Marker | Meaning |
|--------|---------|
| `[[Node]]` (no marker) | Node is in this patch, or is a ghost link (concept that could become a node) |
| `[[Node]]↗` | Linked external — destination exists in another published garden with a navigable URL |
| `[[Node]]⊙` | Exists elsewhere — node exists in the source garden but is not published or linked |

See [EXTERNAL.md](EXTERNAL.html) for the manifest of all external references and their source locations.

## What Is a Garden Patch?

This folder is a **garden patch** — a portable, self-contained fragment of a larger garden that can be placed alongside external content to reveal connections through the garden lens. See [Garden Patch as Composable Knowledge Fragment](glosses/Garden%20Patch%20as%20Composable%20Knowledge%20Fragment.html) for the full concept.

A patch carries everything needed to read it: form type definitions, domain pages, copied nodes from the source garden, new nodes seeded from the target content, and citations pointing to canonical source URLs.

## How This Garden Patch Connects to IFP

The patch has five layers:

**Glosses** — Interpretive definitions of IFP's key concepts (gossip, temperature, persona, disclosure tier, agent, capability, relay, recommendation) that frame each concept through a broader lens.

**Models, convictions, decisions, patterns, principles** — New nodes seeded from IFP concepts. These express Peter's design decisions and architectural choices through garden forms, making their connections to broader patterns visible.

**Inquiries** — Open questions that surface hidden assumptions in IFP's design. Where IFP makes decisions without explicit justification (why four authentication levels? why six disclosure tiers? why natural language bodies?), inquiries frame the question and explore alternatives.

**Citations** — Compound citations of Christopher Allen's published works ([Minimum Viable Architecture](citations/Allen%20(2023)%20Minimum%20Viable%20Architecture/Allen%20(2023)%20Minimum%20Viable%20Architecture.html) and [Progressive Trust](citations/Allen%20(2024)%20Progressive%20Trust/Allen%20(2024)%20Progressive%20Trust.html)) with analysis and insights showing how these frameworks apply to IFP's architectural decisions. Citations point to canonical URLs, not copies of source text.

**Existing garden nodes** — Copies from Christopher Allen's Deep Context Architecture garden. These nodes on progressive trust, principal-agent relationships, coercion resistance, and collaboration mechanics already exist in a larger knowledge graph. They show that IFP's concepts connect to a network of related ideas across identity, governance, and protocol design.

## Three Knowledge Domains

The garden nodes in this collection connect to three knowledge domains:

- **[Deep Context Architecture](domains/Deep%20Context%20Architecture.html)** — Architecture for personal knowledge systems that preserve captured reasoning through typed forms, predicate edges, and progressive disclosure.

- **[Self-Sovereign Identity](domains/Self-Sovereign%20Identity.html)** — Individual control of digital identity through principal authority, agency law, and coercion resistance.

- **[Synpraxis](domains/Synpraxis.html)** — How independent agents achieve outcomes together across varying degrees of integration — from coordination through cooperation to collaboration.

## Reading Order

Start anywhere that interests you. If you want a guided path:

1. **Glosses** — Read [Gossip as Social Sensing Filter](glosses/Gossip%20as%20Social%20Sensing%20Filter.html) and [Agent as Human Proxy in Protocol Exchange](glosses/Agent%20as%20Human%20Proxy%20in%20Protocol%20Exchange.html) to see how garden glosses reframe familiar IFP concepts.

2. **Models** — Read [Conversation Temperature as Protocol Cadence Spectrum](models/Conversation%20Temperature%20as%20Protocol%20Cadence%20Spectrum.html) to see how a model form captures structural relationships.

3. **Convictions** — Read [Filtering Is More Valuable Than Connecting](convictions/Filtering%20Is%20More%20Valuable%20Than%20Connecting.html) to see how IFP's core insight maps to a conviction form.

4. **Connections** — Read [Authority Flows from the Person](principles/Authority%20Flows%20from%20the%20Person.html) to see how IFP's identity model connects to Self-Sovereign Identity principles that predate IFP.

## About This Garden

**Author**: Christopher Allen
**Context**: Ongoing dialogue with Peter Kaminski about agency, AI, and structured knowledge
**Source garden**: [Deep Context Architecture](domains/Deep%20Context%20Architecture.html) (not yet published)
**License**: Same as the IFP repository
