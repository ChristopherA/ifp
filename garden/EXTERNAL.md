# External References

Nodes referenced by this garden patch that exist in the source garden but are not included here. Each entry shows the node name, form type, and brief summary from the source garden.

When you see `[[Node Name]]⊙` in a garden node, it links here. The ⊙ marker means the node exists in the source garden but is not published or included in this patch.

**134 nodes documented** from the source garden. 42 references could not be located (may be ghost links or informal references).

## Deep Context Architecture

### Model Form

**Captured Reasoning Exchange Pipeline**: Three-layer model for how captured reasoning moves from human authoring (markdown) through agent traversal (semantic graph) to trusted exchange (Gordian Envelope) — each layer serving a different audience while representing the same knowledge.

**Compound Node Anatomy**: Defines the compound node — a folder-based knowledge object with a lead file, sibling files, renditions, and archives. Generalizes the garden's compound document pattern to vault-wide application.

**Cross-Domain Document Lifecycle Parallels**: Three domains — wiki communities, digital gardens, and AI agent context systems — face the same document lifecycle problems (splitting, staleness, ownership, deletion) under different constraints. Maps the parallels and identifies where the analogy breaks down: statelessness, read frequency, token economics, and automated maintenance.

**Document Lifecycle Governance Heuristics**: Maps wiki governance heuristics for document lifecycle (split, merge, redirect, delete, draftify) to garden and agent context operations. Includes failure modes: the append-only trap (growth by accretion without consolidation) and structure ossification (resistance to reorganization over time).

**Guardrail Hierarchy for Graph Maintenance**: Four enforcement tiers for knowledge graph maintenance, ordered by strength: hard limits (absolute boundaries), safety nets (pre-commit validation), golden paths (preferred defaults via templates and conventions), and audit trails (post-hoc diagnosis). The ordering is load-bearing — higher tiers override lower ones when constraints conflict. The garden's current gap is in safety nets: automated structural checks between golden paths and hard limits.

**Personal Knowledge Management Organizing Principle Spectrum**: Model mapping Personal knowledge management systems on an actionability-meaning spectrum — PARA at the actionability end, Zettelkasten at the meaning end, ACE and GRID as hybrids. Includes a second axis (folder vs. link) and our vault's three-axis resolution (function, meaning, form). Comparison matrix across 8 systems and 9 dimensions.

**Quad Model Mapping to Forms**: Maps the Claude Code quad (rule/process/requirements/reference) onto deep context form types as facets, not forms. Any capability may have all four facets. Rules map to Principle or Boundary, Process to Protocol or Skill, Requirements to Pattern consequences or Case outcomes, Reference to Gloss, Reference, or Citation.

**Status Lifecycle Tracks**: Three status tracks for three kinds of knowledge work. Maturity (Seed→Growing→Evergreen→Pruned) for living documents, curation (uncurated→curated→annotated) for static captures, processing (Captured→Transcribed→Cleaned→Summarized→Published) for meetings. The has_status:: predicate is universal; the vocabulary varies by node type.

**Swanson Linking — Undiscovered Public Knowledge**: Don Swanson demonstrated in 1986 that valuable knowledge exists implicitly across disconnected research literatures. His ABC model: if Literature A establishes A-B and Literature C establishes B-C, but the two share nothing, then A-C is a hypothesis no one has formulated. Applied to the garden, cross-domain typed edges enable the same discovery pattern across domain boundaries.

**Sycophantic Confidence Spiral**: Model describing how AI sycophancy creates circular evidence that inflates user confidence without approaching truth. The mechanism: AI generates data conditioned on user hypotheses, user treats this as independent evidence, beliefs concentrate on initial hypothesis. Default LLM behavior is indistinguishable from explicit sycophancy. Discovery drops from 29.5% to 5.9% when sampling is biased.

**Vocabulary Lifecycle Through Tending**: Model unifying the degradation mechanism common to growing vocabularies, configuration systems, and knowledge graphs. Any accumulating terminology — predicates, tags, rules, skills — degrades retrieval effectiveness without continuous tending. Three gardening activities maintain health: weeding (removing malformed entries), seeding (introducing needed specificity), and fertilizing (enriching with semantic structure).

### Pattern Form

**Context Conservation Hierarchy**: Pattern for accessing compound node content in four tiers of increasing token cost — path listing, lead file YAML, lead file body, siblings — so agents triage relevance cheaply before committing context window capacity.

**Cross-Project Learning Repatriation**: When garden work starts in one workstream but moves to an external project (or vice versa), learnings must be deliberately imported back. Learnings belong where they are consumed, not where they are produced. Without deliberate absorption, decisions made externally leave gaps in the garden's decision record.

**Domain Extensions on Common Frontmatter Base**: Different content types (clippings, meetings, authored docs) extend a common frontmatter base (created, summary, reviewed) with domain-specific fields rather than sharing a monolithic schema. Content-type is the primary routing axis — it determines which additional fields are relevant. Each source's fields stay out of the others' schemas.

**Ghost Links as Garden Planning Tools**: Ghost links — wikilinks pointing to notes that don't exist yet — function as planning tools when treated as intentional graph members rather than lint errors. WikiBonsai's Caudex tracks these as 'zombie nodes' with full graph participation. Reframing ghost link reports from error lists to planning indexes reveals which unwritten nodes carry the most incoming predicates and deserve attention first.

**Git Tags for Sent-Version Tracking**: Track what recipients received of shared documents using signed git tags (sent/<recipient>-<doc-slug>-<date>). The tag name goes in sent_to frontmatter, enabling git diff sent/tag-name to show what changed since the document was sent. Solves the 'what version did they see?' problem for living documents shared externally.

**Graph Structure Validation for Garden Nodes**: Pattern for graph-level lint checks complementing form-level validation: every garden node carries at least one typed predicate, every domain page receives incoming in_domain:: edges, and no orphan nodes exist without domain membership. Shell scripts over rg and jq — a recipe, not a dependency.

**Informal Edges Poison the Graph**: Informal edges poison the graph through precedent poisoning: an agent invents a redundant relationship type, future traversals find it and treat it as precedent for further invention, and semantic noise compounds until retrieval becomes unreliable. Prevention requires ongoing vocabulary curation — awareness, review, consolidation, and clarification — not just enforcement at creation time.

**Knowledge on Three Axes**: Pattern resolving the tension between sorting (findability, stability) and connecting (serendipity, expressiveness) by organizing knowledge on three orthogonal axes: folders for function, links for meaning, forms for epistemic type. No single axis resolves all organizational forces.

**Lead File to Sidecar Discovery**: Pattern proposing a typed edge from lead files to sidecars (has_sidecar:: or has_companion::) to enable bidirectional traversal within compound nodes — agents can discover binary metadata from the lead file without folder scanning.

**Lightweight Governance for Personal Gardens**: For a personal garden with one active user, a rule file (loaded every session) plus a reference file (with ADRs) provides sufficient governance without the full quad pattern. Expansion follows actual use — new form-type tags are added as forms of those types are written, not preemptively planned.

**One Context One Concern**: Pattern for separating research and implementation into distinct context windows. Mixing exploration and execution in a single context causes task interference, attention dilution, and compounding assumptions. Solution: complete research in one context, distill findings into a compressed handoff, execute in a fresh context. Validated by Anthropic's sub-agent architecture and empirical context rot research.

**Predicate Maintenance Recipes Over Tools**: Predicate maintenance uses shell one-liners rather than dedicated tools, preserving the architecture's zero-tooling floor. Inverse-link queries, predicate renames, and ghost link discovery are all achievable with rg and sed. Documenting recipes keeps the graph maintainable without adding dependencies.

**Probe Before Commit**: Before building on an assumption about external state — API shape, file location, metadata schema, permission model, or the garden's own backlog — probe the actual state first. Seven instances across system access, web research, API integration, metadata design, and process adherence validated this cross-cutting pattern during garden development.

**Progressive Summary Before Substance**: Pattern for navigating large knowledge graphs within small context windows — check summary fields first to assess relevance, then load full nodes on demand, following edges only as needed. Validated by the first garden: summary-based matching produced 151 accurate matches versus 287 false positives from keyword search.

**Source Adapter for Heterogeneous Imports**: Each content source (X API, email threading, web scraping) gets its own extraction adapter, then a common vault normalization step maps the result to garden conventions. Source-specific complexity stays in the adapter; the garden receives consistent notes. Three adapter responsibilities: field mapping, artifact cleanup, and content-type classification.

**Still Knowledge, Moving Action**: Pattern resolving the restlessness problem in actionability-based personal knowledge management systems — separate the dynamic action layer (workstreams, projects) from the stable knowledge layer (notes, research, garden nodes). Knowledge stays put; action reorganizes freely.

**Summary Fields as Load-Bearing Infrastructure**: Summary fields (~280 characters) are not optional metadata but load-bearing infrastructure for agent traversal. During vault enrichment, summary-based matching produced 151 accurate matches versus 287 false positives from keyword search. Poor summaries produce retrieval failures.

**Temporary Predicate Scaffolding**: Predicates can serve as temporary scaffolding — built for a specific purpose (ghost link analysis, map of content prioritization), then removed after serving that purpose. During tag normalization, 913 relates_to:: predicates were created to build ghost links for map of content prioritization, then removed to prevent graph pollution. Build it, use it, clean it up.

**Vault Content Graduation**: Content moves from vault precinct types to garden precinct nodes through tending — recognizing when operational captures are ready to become curated knowledge. Clippings graduate to citations, meetings produce decisions, research notes become references. Lateral movement between precincts, not promotion up a hierarchy.

### Principle Form

**Standalone Document Test for Form Candidacy**: The test for whether a knowledge type warrants its own form type: does it produce a standalone document with a known internal structure? A form is a knowledge object with a structural contract — required sections that make its shape predictable. Types that only appear embedded in other forms are structural elements, not forms.

### Inquiry Form

**Automated Gardening Trust Problem**: Open question: can agents reliably garden their own context files — detecting staleness, refactoring bloated sections, removing contradictions? Wiki bot policies are the closest precedent. The recursive trust problem: the agent assessing the quality of its own instructions may be biased by those instructions.

**Compound Node Meeting Structure**: Inquiry into how meeting compound nodes should be structured — whether cleaned transcripts or meeting summaries serve as lead files, what goes in renditions vs. siblings, and how the meeting-capture skill should adapt for compound output.

**Cross-Domain Form Indexing**: How should domain pages handle forms that belong to multiple domains? Authority Conferral Chain bridges Deep Context Architecture and Self-Sovereign Identity. Authentic Collaboration Requires Agency spans Synpraxis and Self-Sovereign Identity. Current approach: list the form in each domain page with in_domain:: predicates on the form. But this creates maintenance burden and raises questions about primary vs secondary domain membership.

**Form Type Distinctiveness in Naming and Structure**: Investigates whether the 16 form types are distinguishable in practice — can a reader recognize an instance's form type from its title and structure alone? 15 of 16 types now have instances with documented naming heuristics. Among instantiated types, naming overlaps persist (pattern vs principle both use 'X Over Y'), and structural contracts blur at boundaries (gloss vs model).

**Garden Publishing Path**: Inquiry into how the deep context garden should be published for external consumption. Five approaches evaluated (Quartz, Jekyll+WikiBonsai, Eleventy, custom Python script, raw HTML) against typed relation rendering, Obsidian syntax support, and zero-tooling philosophy. Custom script recommended for maximum control; approaches are composable.

**Graph-Native Skill Execution**: Inquiry into how garden skills can discover, load, and reason from typed graph nodes during execution — moving from hardcoded file paths to predicate-based traversal. Explores the infrastructure gap between current self-contained skills and graph-native skills that compose with garden knowledge.

**IPARAG Term Origins**: Inquiry into the source and exact meaning of 'IPARAG' — a personal knowledge management method recalled from the Zettelkasten community. Extensive search found no canonical source as of March 2026. Four hypotheses proposed; most likely reading is Inbox-Projects-Areas-Resources-Archives-Goals (the two most common PARA extensions combined).

**Inquiry Lifecycle and Resolution**: When is an inquiry 'done'? Inquiries generate other nodes — cases from tested hypotheses, patterns from validated parallels, references from syntheses. The inquiry may persist as an open thread with resolved and unresolved branches, or archive when its questions are addressed elsewhere. No lifecycle model exists yet.

**Living Document Scale Limits**: Open question: is there a scale threshold beyond which the maintenance cost of living documents exceeds their accumulated value? Jerry Michalski's TheBrain (620,000+ nodes, 28 years) is evidence that single-author knowledge graphs can scale, but at what cost to gardening labor and structural coherence?

**Personal Knowledge Management Method Adoption for Vault Architecture**: Inquiry into what our vault should adopt, modify, or reject from personal knowledge management methods (PARA, ACE, GRID, Zettelkasten, Digital Garden). Five open questions spanning inbox workflows, Categories/ map of content evolution, Goals integration, GRID's validation of note typing, and a minimum viable explanation for onboarding.

**Predicate Vocabulary Stabilization**: The predicate grammar started freeform by design — new predicates welcome when existing ones don't fit. The architecture suggested review after 50+ relations and controlled vocabulary after 200+. The garden is well past both thresholds. When does freeform become inconsistency? What stabilization looks like without rigidity.

**Productivity Separation from Knowledge Vault**: The vault mixes garden content (typed knowledge nodes) with productivity content (daily notes, meetings, goals, inbox). Neither depends on the other. Should productivity move to a separate tool or vault? The connection is through wikilinks, which could cross boundaries if separated.

**Scenario Lifecycle and Aging**: Inquiry into how scenario nodes age — when a scenario is validated by events it becomes a case, but invalidated scenarios may still hold value through their force analysis. Explores lifecycle transitions, retention criteria, and whether wrong-but-useful scenarios should persist or archive.

**Universal Document Lifecycle State Machine**: Open question: is there a single document lifecycle state machine that generalizes across wiki pages, garden nodes, and agent context files? The deep context architecture has three status tracks for three kinds of work — but wiki, garden, and agent domains face the same lifecycle problems under different names.

**Vault-Wide Compound Node Adoption**: Inquiry into which vault document types beyond garden nodes benefit from compound node structure — citations, cases, research notes, meetings, clippings — and what criteria trigger graduation from atomic to compound. Addresses whether compound nodes should be vault-wide or garden-only.

### Gloss Form

**ACE as Three Dimensional Personal Knowledge Management**: Interprets Nick Milo's ACE (Atlas, Calendar, Efforts) as a three-dimensional personal knowledge management framework grounded in STIR (Space, Time, Importance, Relatedness). Closer to our vault's philosophy than PARA — acknowledges the linking layer and uses maps of content — but still lacks epistemic note typing.

**Deep Context as Shared Language**: The term 'deep context' originates from Allen's 2014 writing on shared languages. When practitioners share deep context, a single phrase invokes an entire framework — saying 'Cynefin' communicates the complicated/complex distinction and how to work with each. The architecture makes this implicit understanding explicit and navigable through typed nodes and traversable edges.

**Digital Garden as Growth Ethos**: Interprets the digital garden movement (Caufield's stream-vs-garden distinction, Appleton's six patterns) as a growth ethos — organic, imperfect, associative knowledge development. Our deep context garden adopts the philosophy but adds formal structure: typed nodes, typed predicates, and structural contracts that most digital gardens lack.

**GRID as Note Type Organization**: Interprets GRID (Glossary, Reference, Index, Diary) as the mainstream personal knowledge management method closest to our garden nodes — it organizes by note type rather than actionability or topic. GRID's four types map roughly to Gloss, Reference/Citation, Domain, and Case in our 15-form taxonomy.

**Garden Precinct**: The garden precinct is the zone within Deep Context Architecture where knowledge is curated into typed nodes with structural contracts, tended through growth stages (Seed to Evergreen), and interconnected by typed predicates. It solves the problem of making knowledge retrievable, composable, and trustworthy over time.

**IPARAG as Extended PARA**: Interprets IPARAG as a six-category extension of PARA adding Inbox (capture staging) and Goals (strategic alignment). No canonical source text found as of March 2026 — likely a community coinage combining PARA's two most common extensions into one acronym.

**Johnny Decimal as Permanent Addressing**: Interprets Johnny Decimal as a permanence-first organizational system — every file gets a stable numerical address (e.g., 32.14) that never changes. Solves the problem our vault handles differently: we use git for permanence and wikilinks for stable references instead of numerical addressing.

**Lead File Selection Guidance**: Defines the lead file — the primary access point of a compound node, borrowing from journalism's 'lead' concept. Provides selection criteria by content type: citation cards lead citations, transcripts lead meetings, research notes lead investigations.

**Note Titles as APIs**: Glosses Andy Matuschak's claim that note titles function as APIs — stable abstractions usable as reference handles. The garden extends this by observing that different form types answer structurally different questions, so the shape of a good title API varies by form. Three naming traditions (wiki, pattern language, evergreen notes) converge on this insight.

**PARA as Actionability-First Design**: Interprets PARA (Projects, Areas, Resources, Archives) as an actionability-first organizational method — four categories sorting information by urgency rather than topic. Maps PARA to our vault, identifies the gap: no connection fabric, no epistemic differentiation, and constant reorganization undermines long-term knowledge stability.

### Citation Form

**Altshuler (2026) Nanograph On-Device GraphDB**: Citation of nanograph, an on-device schema-enforced graph database for agentic workflows built on Rust, Arrow, Lance, and DataFusion. Validates Deep Context Architecture design principles from an independent source: typed predicates prevent semantic drift (naming the failure mode 'precedent poisoning'), local-first storage preserves human authority, and decision traces create compounding reasoning value.

**Batista (2026) Rational Analysis of Sycophantic AI**: Bayesian proof that sycophantic AI creates circular evidence inflating confidence without approaching truth. Wason 2-4-6 experiment (N=557) found default GPT suppresses discovery equivalently to explicit sycophancy (5.9% vs 29.5% for unbiased sampling). Formalizes delusional spiraling: rational agents become increasingly wrong when AI samples data conditioned on user hypotheses.

**Chatlatanagulchai (2025) Agent READMEs**: Empirical study of 2,303 agent context files across 1,925 repositories. Finds that CLAUDE.md, AGENTS.md, and similar files behave more like dynamic configurations than static documentation — maintained through frequent incremental additions, with 59-67% undergoing multiple commits. Identifies 16 instruction categories and a gap in security/performance coverage.

**George (2026) Harness Engineering Is Cybernetics**: Citation of George's X article tracing agent harness engineering through three cybernetic instantiations: Watt's governor, Kubernetes controllers, and LLM harnesses. Each closes a feedback loop at a progressively higher layer. The core insight — making human judgment machine-readable is the real engineering work — provides the theoretical framework for why DCA uses typed predicates and structural contracts.

**Peters (2008) Tag Gardening for Folksonomy Enrichment**: Formalizes tag gardening as three activities — weeding (removing bad tags), seeding (introducing specific tags), and fertilizing (enriching with external knowledge organization systems). Proposes power tags from distribution curves as candidates for semantic enrichment. Introduces TagCare for cross-platform personal tag maintenance. The gardening metaphor is deliberate: vocabularies are living systems requiring continuous tending.

**Rajasekaran (2025) Effective Context Engineering for AI Agents**: Anthropic's applied AI team defines context engineering as curating the smallest high-signal token set at each inference step. Introduces four strategies — Write, Select, Compress, Isolate — with empirical data showing ~90% improvement from sub-agent isolation on research tasks. Grounds context management in transformer attention budget constraints.

**Roy (2026) Words Without Consequence, from The Atlantic**: Deb Roy argues that AI has decoupled speech from consequence for the first time. An LLM's apologies are empty because no accountable speaker stands behind them. Routine fluent speech without responsibility degrades the conditions under which promises and advice carry meaning — a shift in the moral structure of language.

**arscontexta (2026) Skill Graphs**: Proposes skill graphs — networks of small SKILL.md files connected by wikilinks — as an alternative to monolithic skill files. Each node holds one complete thought; wikilinks carry semantic meaning in prose so agents follow relevant paths. Progressive disclosure applies recursively inside the graph: index, descriptions, links, sections, full content.

**systematicls (2026) World-Class Agentic Engineering**: A practitioner guide arguing the best agentic engineers are communicators, not coders. Covers context management as the primary constraint, sycophancy-aware prompting patterns, rule and skill lifecycle for agent configuration, and task contracts as completion criteria. Central insight: strip dependencies, separate research from implementation, and iterate on rules and skills.

### Case Form

**Architecture Document Extraction to Garden Forms**: Case documenting the systematic extraction of a 450-line architecture document into 80+ standalone garden nodes across 15+ form types over 12 sessions. The monolithic source defined the entire deep context framework — form types, principles, patterns, models, decisions — and had to be decomposed into a living typed graph.

**Hybrid Bootstrapping for Garden Migration**: Case documenting the first deep context garden bootstrap — a Python script converted topic tags from 913 archive files into 4,294 relates_to predicates, transforming a flat bag of files into a connected graph. Scripted extraction handled structure; hand-authoring handled interpretation. The hybrid approach proved viable at scale.

### Reference Form

**Deep Context Garden Conventions**: Practical conventions for the first deep context garden in this Obsidian vault. Hard line between tags (flat classification, no graph edges) and links (graph edges). Two-namespace tag system: type/ for document category, status/ for maturity. Topic tags explicitly rejected — wikilinks produce graph edges instead.

**Deep Context Implementation Roadmap**: Iteration-by-iteration plan for building a Deep Context garden inside an Obsidian vault. Defines four phases — Foundation, Seed Graph, Content Migration, Publishing — each independently valuable. Uses predicate::[[target]] typed relations and targets an hour-a-day tending rhythm with agent assistance between sessions.

**Structural Elements Within Forms**: Reference for knowledge types that don't warrant their own form type — ADR, Narrative, Warrant, Signal, Commitment, Lexicon entry, Tension/Paradox. Each has a home inside existing forms. Answers 'where does X go?' for the seven types that failed the standalone document test.

**Typed Relations as Simple Graphs in Plain Markdown**: predicate::[[Target]] typed relations turn markdown files into a directed labeled graph with no database or schema. Plain wikilinks answer \

### Research Form

**Deep Context Content Decision Records**: 26 architectural decisions governing content structure for the deep context garden: predicate-based classification over tags, snake_case predicates, five-category form grouping, taxonomy-expansion-follows-use, compound document graduation, and lightweight governance. Merges the previous C- and N- ADR series into a single themed sequence.

**Research Graphs and Precinct Architecture**: Investigates Cornelius's Research Graphs system against the garden's precinct architecture. Maps his 5 note types to existing garden forms and identifies two infrastructure gaps: confidence metadata and provenance chain propagation. Surfaces Swanson's Literature-Based Discovery as a missing model. First instance of Research Form.

### Scenario Form

**Knowledge Graph as Digital Twin of Principal Reasoning**: Explores what happens when deep context gardens reach sufficient density and connection that agents can reliably act on behalf of the garden owner in routine decisions and external communications, shifting the principal-agent dynamic from augmentation toward delegation.

### Form Type

**Boundary Form**: Defines the Boundary form type: a declaration of what an agent may and may not decide. Not what the right choice is, not how to make it, but who holds authority. Amendable through deliberative process, never unilaterally. 1 instance in Garden/boundaries/.

**Case Form**: Defines the Case form type: a specific narrative with outcome recording what was attempted, what resulted, and what was learned. Immutable — history doesn't change, though interpretation may.

**Citation Form**: Defines the Citation form type: a structured dossier on a single work containing bibliographic entry, summary, key points, key quotes, influence, sources, and relations. Named as Author (Year) Abbreviated Title. Atomic at Seed stage, graduating to compound (analysis.md, insights.md, Renditions/, Archives/) as analysis deepens. Append-only.

**Model Form**: Defines the Model form type: a structural representation showing elements, relationships, boundaries, and feedback loops. How things relate to each other. Evolving as understanding grows. Models are explanatory (how things work), distinct from patterns (what to do) and scenarios (what might happen).

**Protocol Form**: Defines the Protocol form type: a specification for multi-party coordination across trust boundaries. Distinguished from a process by who must agree — a protocol works only if all parties follow it. Scope includes human coordination methods alongside technical protocols.

**Pruned Stage**: Defines the Pruned Stage: a garden node no longer current but preserved rather than deleted. Pruning replaces deletion so that link chains and reasoning history remain traceable. Uses superseded_by:: predicates to point to replacements. Lowest retrieval priority among all growth stages.

**Reference Form**: Defines the Reference form type: a comprehensive briefing synthesizing multiple sources and forms into a coherent domain picture. May contain model-like tables, principle-like recommendations, and gloss-like interpretations. Source docs in Research/ carry this type.

**Research Form**: Defines the Research form type: a living investigation that grows through active research, contains form-typed sections with their own predicates, and depletes as findings extract into standalone garden nodes. Distinguished from Reference (static briefing) by its depletion lifecycle and from Inquiry (poses questions) by containing evidence and analysis.

**Scenario Form**: Defines the Scenario form type: a plausible narrative of how the future could unfold given specific drivers and conditions. Scenarios don't predict — they prepare. Value lies in spanning the possibility space. Names state the hypothetical trajectory, not the driving forces.

**Seed Stage**: Defines the Seed Stage, the entry point for all garden nodes: raw capture with low confidence, unprocessed structure, and minimal links. Seeds are extraction products that have enough content to stand alone but have not been tested against other nodes, verified, or refined through use.

**Skill Form**: Defines the Skill form type: a compound node bundling trigger, procedure, quality criteria, and rationale — with graph dependencies declaring which garden nodes the skill reads and follows. Skills bridge the garden's knowledge layer and the agent's execution layer.

### Chat Log

**Chat Log**: Defines the Chat Log vault type: a text chat record from a meeting sidebar or AI conversation, always derived from a parent note via derived_from:: predicate. Preserves original timestamps and speaker attribution without cleanup. Captures links shared, brief exchanges, and introductions alongside the spoken conversation.

### Decision Form

**Artifact Predicate for Binary Metadata**: The artifact:: predicate links a sidecar metadata file to the binary it describes, making the relationship explicit and graph-traversable. Agents find metadata for any binary by checking for a sidecar with artifact:: pointing to it.

**Body Predicates for Meeting Attendees**: Meeting attendees are recorded as body predicates (attendee::[[Person Name]]) instead of YAML frontmatter lists. More verbose for large meetings but graph-traversable, enabling queries like 'which meetings did [[Person]] attend?' Person names as wikilinks create connections to Person Notes.

**Classification via Predicates Not Tags**: Classification uses body-level typed relations (is_a::, has_status::) instead of YAML tags. The general litmus test: is the value a fixed scalar or a connection to a defined concept? Scalars go in frontmatter fields, connections go in typed relations, subject matter goes in wikilinks. Tags produce sets; links produce graphs.

**Custom Python Generator for Typed Relations**: Chose a custom Python static site generator (~150 lines, four-stage pipeline) over Quartz, Jekyll, Eleventy, and Pandoc for publishing a garden with predicate::[[target]] typed relations. Standard markdown parsers ignore wikilinks, typed inline relations, and typed block-level relations — the three syntax patterns the garden depends on. A single-file generator with no external parser dependencies handles exactly what's needed.

**Deep Context as an Architecture for Captured Reasoning**: The decision to capture personal reasoning as typed markdown forms connected by predicates — not as fine-tuned models, retrieval-augmented documents, or tagged notes. Typed forms with structural contracts make reasoning traversable by agents; predicates make it navigable; progressive disclosure makes it fit in context windows.

**Descriptive Noun-Phrase Names for Predicate Targets**: Predicate targets use descriptive noun-phrase names with a two-word minimum and type-distinguishing suffixes (Form, Stage) to prevent namespace collisions while remaining readable in predicate context. Ghost links serve as a natural checklist of definition pages to create.

**Descriptive Slugs for Archive Binaries**: Archive binaries are renamed from publisher gibberish to author-year-descriptive-title-slug.ext for browsable directory listings. Original filenames are preserved in the sidecar's original_filename field.

**Display Name Preservation in Compound Documents**: When a form graduates from atomic file to compound folder, the main file keeps its display name so all existing wikilinks continue to resolve without modification. The folder uses a slug; the file inside keeps the human-readable name.

**Extraction Model for Garden Migration**: Migration from Research/ to Garden/ means extraction — surveying source documents for form-type content chunks, extracting each into its own garden node, connecting via predicates, and reducing originals over time. Source files aren't 1:1 with form types; they contain content spanning multiple nodes.

**Folder-Note Pattern for Compound Documents**: Compound documents use the folder-note pattern where the main file shares its folder's name. Graduation from atomic to compound is a git mv into a new folder. Wikilinks stay stable because Obsidian matches on filename.

**Knowledge Hub Not Binary Archive**: The vault serves as a knowledge hub, not a binary archive. Keep markdown (LLM-readable) and binaries with no other canonical source. Remove binaries available from public URLs, git repos, or re-renderable from sources. Sidecars document where removed artifacts live.

**Linear Processing Stages for Meetings**: Meeting processing uses linear stages (Captured → Transcribed → Cleaned → Summarized → Published) via has_status:: plus fork predicates (is_published::URL, is_shared::DATE) for distribution tracking. Distinct from garden content maturity stages.

**Non-Local Artifact References in Sidecars**: Sidecars can reference artifacts archived elsewhere, not just local binaries in Archives/. A sidecar with no local artifact uses derived_from:: to link to its meeting note and documents canonical sources in prose sections: Source Repository for the permanent location and Public URLs for convenience links.

**Precinct as Organizational Unit**: Adopts 'precinct' from urban planning as the organizational unit within Deep Context Architecture. Two precincts — garden and vault — solve different knowledge problems using shared infrastructure (predicates, scripts, typed edges). Neither is a maturity level of the other.

**Predicates Everywhere for Compound Nodes**: All compound nodes use body predicates for classification regardless of vault folder. No tags in frontmatter — YAML retains only scalar properties. Extends the predicate model from Garden/ to all compound structures in the vault, including Meetings/ and Research/.

**Renditions and Archives Replace Sources**: The original sources/ subfolder in compound citations splits into Renditions/ (searchable markdown copies) and Archives/ (preserved original binaries). The distinction matters because they carry different trust implications and serve different retrieval purposes.

**Renditions and Archives as Distinct Artifact Types**: Rendition names format-transformed markdown copies; archive names preserved original binaries. These terms replace the ambiguous 'source' which collides with source code and source_url. The Rendition - prefix identifies standalone renditions.

**Role-Specific Attribution Predicates for Opus Form**: Opus Form uses role-specific predicates for attribution (principal::, produced_by::, authored_by::, copyright_held_by::, foreword_by::, illustrated_by::, etc.) rather than a flat contributor list. Grounded in the principal-agent framework from agency law and the producer/principal distinction from the January 2026 email thread on authorship in the age of AI.

**Sidecar Files as Metadata Envelopes**: Binary archives get optional .sidecar.md companion files with frontmatter, summary, and typed predicates. Only warranted when a binary is actively cited or requires agent discoverability — most archives don't need sidecars.

**Snake Case for Predicate Naming**: Adopts snake_case for typed relation predicates (derived_from, relates_to) over kebab-case, camelCase, or UPPER_SNAKE. Three factors: alignment with deep context grammar, editor ergonomics (double-click selects whole predicate with underscores but not hyphens), and absence of a dominant external standard.

**Spelled-Out Names Over Internal Acronyms**: Decision to avoid acronyms in garden nodes and vault conventions. Spell out Deep Context Architecture, Self-Sovereign Identity, personal knowledge management, and map of content instead of DCA, SSI, PKM, MOC. Acronyms hurt discoverability, risk collisions across domains, and save negligible bytes. External system names (PARA, ACE, GRID) are proper names, not acronyms to expand.

**Structural Retrieval Hierarchy**: Five retrieval tiers derived from folder location and predicates rather than per-file priority fields: garden evergreen/growing nodes, vault notes, renditions, sidecars, binary archives. Priority changes require structural moves, not metadata edits.

**Universal Compound Form Graduation**: Any form may graduate from atomic file to compound folder when it accumulates related material. The original six-form list of compound-eligible types becomes illustrative, not restrictive. The graduation mechanic applies uniformly.

**Vault Type Targets for Non-Garden Notes**: Non-garden vault types (meetings, transcripts, chat logs, sidecars) get is_a:: targets following the same naming conventions as garden form types: Meeting Note, Transcript, Chat Log, Sidecar. Ghost links initially, definition pages later.

### Meeting Note

**Meeting Note**: Defines the Meeting Note vault type: a record of a synchronous conversation with attendees, topics, and outcomes. Uses body predicates for attendees and processing status. May contain compound documents with transcript, chat log, and recording sidecars.

### Person Note

**Person Note**: Defines the Person Note vault type: a contact-style record for individuals referenced across the vault. Lives in People/Individuals/ and serves as the link target for attendee:: predicates in meetings and author:: references. Includes aliases, meeting history, project associations, and relationship context.

### Sidecar

**Sidecar**: Defines the Sidecar vault type: a markdown metadata envelope for binary or non-local artifacts (video, audio, slides, PDFs) that cannot be represented directly in the knowledge graph. Uses artifact:: predicates to point to canonical sources in local Archives/ folders or remote repositories.

### Transcript

**Transcript**: Defines the Transcript vault type: a cleaned speech-to-text record derived from a meeting recording via derived_from:: predicate. Speaker-normalized (full name first, then first name) with three cleanup levels and configurable filler calibration. Always a sidecar to its meeting note, never standalone.

## Self-Sovereign Identity

### Model Form

**Self-Coercion Through Surveillance Awareness**: Model of how surveillance knowledge creates self-censorship before any rule is violated. People avoid legitimate actions fearing discrimination or negative inference. Covers chilling effects, anticipatory compliance, and the mechanism by which Protective Paternalism's safety framing makes objection socially costly.

### Inquiry Form

**Coercion Resistance as Replacement Framing**: Explores whether 'coercion resistance' or related terms (sanctuary technology, technology paternalism, exodus protocols) can replace overloaded terms like 'privacy' and 'censorship resistance' as the framing for what digital autonomy systems protect against. Maps the emerging terminology landscape across Ethereum (CROPS/sanctuary), Self-Sovereign Identity (coercion lenses), and sociotechnical design (technology paternalism).

### Citation Form

**Brignull (2010) Deceptive Patterns Dark Patterns**: Coined 'dark patterns' in 2010 and created the authoritative taxonomy of manipulative interface design now embedded in EU (DSA, DMA) and US (FTC, CPRA) law. Documents 400+ examples and $400M+ in enforcement settlements. Shows 95% of free mobile apps use deceptive patterns.

**Spiekermann and Pallas (2006) Technology Paternalism**: Originating paper for the concept of Technology Paternalism, introducing the term in the context of ubiquitous computing. Argues that beyond privacy and data security, automated environments raise questions about human control, and proposes 'the right for the last word' — the ability to overrule autonomous system behavior.

## Synpraxis

### Inquiry Form

**Participation to Community Progression as Garden Concepts**: Investigates how the participation-engagement-affinity-association-community framework from the author's pedagogy work should be represented in the garden. Individual terms may be Gloss Form nodes; the progression may be a Model or a synthesis gloss; the relationship to cooperation-collaboration research needs exploration.

### Opus Form

**My Hybrid Flipped Learning Environment**: Christopher Allen explains his teaching philosophy at Bainbridge Graduate Institute, where he applied game design principles to hybrid education. Describes the orient-scan-focus-act-reflect learning cycle, iterative feedback design, flow-based engagement, and collaborative artifact creation that later evolved into the sociosocratic learning method.

**Sociosocratic Learning & Seminars**: Christopher Allen describes the sociosocratic learning method, where small groups build shared language and agency through collaborative artifact creation rather than lectures, following an orient-scan-focus-act-reflect cycle across multiple sessions.

### Decision Form

**Synpraxis as Domain Name**: Coins 'synpraxis' (Greek: syn + praxis = acting together) to name the knowledge domain covering how independent agents achieve outcomes together across varying degrees of integration — including anti-patterns. Chosen over existing terms (collective action, shared agency, cooperative systems) because none covers the full territory: constructive patterns, failure modes, preconditions, and the coordination-cooperation-collaboration spectrum.

## Uncategorized

### Reference Form

**Compound Nodes for Knowledge Management**: Defines compound nodes — folder-based knowledge objects with a lead file, sibling files, renditions, and archives. Introduces terminology (context node, typed edge, lead file, compound node) and proposes strategies for context conservation, binary management, and sidecar linking. Generalizes existing deep context garden ADRs (C07-C22) to vault-wide application.

### Opus Form

**Field Notes on Handpan Sound Models & Instruments**: Personal field notes documenting specific handpan instruments and their sound models — the scale templates, acoustic character, modal theory, and ensemble compatibility. Each instrument is documented as both an interactive web page (with tone circles and audio playback) and portable markdown. Planned for publication at www.spiralrhapsody.com/fieldnotes/.

### Person

**Martina Kolpondinos**: Interaction designer and digital identity researcher. Former member of the Swiss federal eID team. Co-editor of WebVH specification. Founder of KosmaConnect. Active in Revisiting Self-Sovereign Identity workshops, contributing perspectives on technology paternalism and coercion resistance.

### Person Note

**Christopher Allen**: Christopher Allen is the founder and president of Blockchain Commons, author of the 10 Principles of Self-Sovereign Identity (2016), co-editor of the TLS 1.0 draft, and principal authority of this vault's augmented knowledge system. His work bridges applied cryptography, digital identity, and trust architecture through the Gordian stack, XIDs, and the principal authority framework rooted in agency law.

**Jonathan Postel**: Jonathan Postel (1943-1998) — RFC Editor from 1969 until his death, creator of IANA, co-architect of TCP/IP, SMTP, and DNS. His Robustness Principle ('be liberal in what you accept') shaped protocol design for decades. The Inter-Face Protocol's 'clarity over tolerance' principle is a direct, respectful departure from Postel's Law for the age of reasoning agents.

**Peter Kaminski**: Profile of Peter Kaminski — wiki gardener, context engineer, agentic AI course instructor. Projects include MassivePub (static site generator for markdown wikis), TextPile, and the Interface Protocol (IFP) for human-agent-agent-human communication. Starting paid agentic AI course March 2026 using Obsidian and Claude Code. Core drive: helping regular people use capable tools.

### Untyped

**Digital Identity**: MOC spanning the range from centralized identity databases to self-sovereign models where individuals control their own credentials. Anchors on W3C standards (DIDs, Verifiable Credentials) and collaborative design forums (Rebooting the Web of Trust), with trust frameworks governing who trusts whom as a key cross-cutting concern.

**Gordian Envelope as Agent Memory Layer**: Analysis of Gordian Envelope — a recursive CBOR type organizing data as subject-predicate-object triples with SHA-256 content-addressing and selective elision — as a trust and exchange layer for AI agent memory. Covers the five enumerated cases, signing, and how elision enables privacy-preserving memory sharing between agents.

**Research Note**: *(no summary available)*

**The Gardening Problem Returns - Document Lifecycle in the Age of AI Agents**: Collaborative article outline arguing wiki communities spent 25 years developing document lifecycle heuristics (split, merge, rewrite, delete) that AI developers now rediscover under new names. Four authors — Allen, Kaminski, Michalski, Udell — each augmented by different tools, ask whether those heuristics transfer.

### reference

**Revisiting Self-Sovereign Identity Initiative**: The Revisiting Self-Sovereign Identity initiative (2025-2026) develops coercion-prevention lenses and revised principles for the 10th anniversary of the original Ten Principles. Pivoted from community-drafting model to curated approach by Christopher Allen and Shannon Appelcline, with workshop participants providing feedback.

### web_clipping

**Dimensions of Digital Coercion**: Four dimensions of coercive control online: attention (manufactured outrage), ergonomic (privacy trade-offs dressed as consent), trust (assumed benign intent without accountability), cultural (dominant norms as participation prerequisites). Coercion is structural — present in open-source ecosystems as much as commercial platforms.

## Not Located

These references appear in the patch but could not be found in the source garden. They may be ghost links, informal references, or person/concept names.

- Agency Before Collaboration
- Annotated Citation
- Autonomy
- Choice Architecture
- Coercion Resistance
- Conviction
- Coraline Ada Ehmke
- Curated
- Descriptive Slugs for Archive Binaries|descriptive slugs
- Domain Name
- Follow-Up Decision
- Foundational Concept
- Garden Node
- Gordian Envelope as Agent Memory Layer|Gordian Envelope
- Is Collaboration Always Superior to Cooperation
- Is Consensus One Mechanism or Three
- Is the Synpraxis Spectrum a True Continuum
- Living Documents Over Static Publications|living documents
- Name
- Node
- Node Name
- Other Citation
- Other Domain
- Other Opus
- Parent Note
- Person
- Person Name
- Precondition Dependencies in Joint Action
- Precondition Stack for Joint Action
- Previous Decision
- Progressive Trust
- Related Form
- Related Pattern
- Related Principle
- Roy (2026) Words Without Consequence, from The Atlantic|Words Without Consequence
- Series Title
- Source
- Source Document
- Target
- The Gardening Problem Returns
- Value
- target

