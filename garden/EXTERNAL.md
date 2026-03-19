# External References

This garden patch references nodes that exist in the source garden but are not included here. This manifest documents the most important external references so that LLMs and human readers can understand the patch boundary.

## Link Markers

| Marker | Meaning |
|--------|---------|
| `[[Node]]` (no marker) | In-patch — resolvable within this garden/ directory |
| `[[Node]]↗` | Linked external — navigable link to another published garden or patch |
| `[[Node]]⊙` | Exists elsewhere — node exists in an unpublished source garden |
| `[[Node]]` (no marker, no file) | Ghost link — node does not exist yet |

If a wikilink target has no marker and no matching file in this patch, it is a ghost link — a concept that could become a node but hasn't been created yet.

## Foundational References (High-Priority External)

These are referenced by many nodes in the patch. They exist in the source garden and provide important context.

| Target | Form Type | Domain | Referenced By |
|--------|-----------|--------|---------------|
| `[[Deep Context as an Architecture for Captured Reasoning]]` | Decision | Deep Context Architecture | 25 files (most form definitions reference this) |
| `[[Inter-Face Protocol]]` | Protocol | Deep Context Architecture | 7 files (the existing Protocol Form node in the source garden) |
| `[[Garden Precinct]]` | Gloss | Deep Context Architecture | 16 files (form definitions reference precinct structure) |
| `[[Vault Precinct]]` | Gloss | Deep Context Architecture | 5 files |
| `[[Classification via Predicates Not Tags]]` | Decision | Deep Context Architecture | 3 files |

## Status Stages (Referenced by Form Definitions)

Form definitions reference status stages that are structural nodes in the source garden. Only `[[Seed Stage]]` is included in this patch.

| Stage | Description |
|-------|-------------|
| `[[Seed Stage]]` | Initial creation — in patch |
| `[[Growing Stage]]` | Active development — NOT in patch |
| `[[Evergreen Stage]]` | Mature, stable — NOT in patch |
| `[[Pruned Stage]]` | Archived after extraction — NOT in patch |
| `[[Captured Stage]]`, `[[Cleaned Stage]]`, `[[Summarized Stage]]`, `[[Transcribed Stage]]`, `[[Published Stage]]` | Meeting/transcript stages — NOT in patch |

## Form Types (Not All Included)

This patch includes 11 form type definitions. The source garden has additional form types not included:

| Form Type | Why Excluded |
|-----------|-------------|
| `[[Protocol Form]]` | No new protocol nodes in this patch (IFP itself is a protocol, but the Protocol Form node is in the source garden) |
| `[[Case Form]]` | No case nodes in this patch |
| `[[Scenario Form]]` | No scenario nodes in this patch |
| `[[Skill Form]]` | No skill nodes in this patch |
| `[[Reference Form]]` | No reference nodes in this patch |
| `[[Research Form]]` | No research nodes in this patch |
| `[[Opus Form]]` | No opus nodes in this patch |

## Key Decisions and Patterns (External)

These are referenced from copied domain pages or form definitions but not included in the patch:

| Target | Form Type | Why Referenced |
|--------|-----------|---------------|
| `[[Informal Edges Poison the Graph]]` | Pattern | Referenced by domain pages — core graph quality pattern |
| `[[Summary Fields as Load-Bearing Infrastructure]]` | Pattern | Referenced by Graph Vocabulary gloss |
| `[[Ghost Links as Garden Planning Tools]]` | Pattern | Relevant to patch boundary discussion |
| `[[Descriptive Noun-Phrase Names for Predicate Targets]]` | Decision | Naming convention for wikilink targets |

## Person References

| Person | Context |
|--------|---------|
| `[[Christopher Allen]]` | Author of source garden and this patch |
| `[[Peter Kaminski]]` | IFP designer, dialogue partner |
| `[[Victoria Tanner]]` | Contributed persona insight to IFP-12 |
| `[[Coraline Ada Ehmke]]` | Author of Dimensions of Digital Coercion (citation in patch) |
| `[[Martina Kolpondinos]]` | Author of Technology Paternalism article (citation in patch) |

## Statistics

- **Total unique wikilink targets in patch**: 234
- **Resolved in-patch**: 67 (28.6%)
- **External (documented here or in form definitions)**: ~50 high-priority
- **Ghost links / low-priority external**: ~117 (mostly from copied form definitions referencing the full source garden's decision and pattern inventory)
