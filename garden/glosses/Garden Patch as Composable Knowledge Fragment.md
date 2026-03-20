---
created: 2026-03-19
author: Christopher Allen
brief_summary: "A garden patch is a portable, self-contained subset of a Deep Context Architecture garden that can be applied alongside external content. It carries enough form definitions, exemplar nodes, and predicate structure to demonstrate the garden lens without requiring access to the full source garden. Patches are composable — multiple patches can coexist or merge."
tagline: "A portable garden subset that reveals connections in external content without modifying it"
---

- is_a::[\[\[Gloss Form\]\]](../forms/Gloss%20Form.html)
- has_status::[\[\[Seed Stage\]\]](../forms/Seed%20Stage.html)
- in_domain::[\[\[Deep Context Architecture\]\]](../domains/Deep%20Context%20Architecture.html)

# Garden Patch as Composable Knowledge Fragment

A garden patch is a **self-contained collection of garden nodes** that can be placed alongside external content — a specification, a codebase, a document set — to show connections visible through the garden lens without modifying the original content.

## What Makes a Patch Self-Contained

A patch carries everything needed to read it:

- **Form type definitions** for every form type used in the patch
- **Domain pages** for every knowledge domain referenced
- **Copied nodes** from the source garden where cross-references are needed
- **New nodes** seeded from the external content being analyzed
- **Citations** with canonical URLs pointing to source works (not copies of source text)

Wikilinks within a patch (`[\[\[Node Name\]\]⊙](../UPSTREAM.html#:~:text=Node%20Name)`) resolve within the patch directory. Links to the source garden or external works use URLs, not wikilinks, since the source garden may not be published.

## Composability

Patches are composable fragments. Two patches from different source gardens can coexist in the same repository. A patch can be merged back into the source garden. A patch can be extended by adding new nodes. The form type system ensures structural compatibility — a Model Form in one patch follows the same structural contract as a Model Form in any other garden.

## This Mini-Garden Is a Patch

The `garden/` folder in this repository is a garden patch. It contains nodes from Christopher Allen's Deep Context Architecture garden alongside new nodes seeded from the Inter-Face Protocol specifications. The patch demonstrates how IFP concepts connect to broader patterns in identity, trust, collaboration, and protocol design.

## Sources

- This mini-garden — the first instance of a garden patch applied to external specifications

## Relations

- relates_to::[\[\[Content Over Container\]\]](../principles/Content%20Over%20Container.html)
  - A patch carries content (nodes and edges) without depending on a specific container (the source vault).

- relates_to::[\[\[Progressive Disclosure Over Eager Loading\]\]](../principles/Progressive%20Disclosure%20Over%20Eager%20Loading.html)
  - A patch loads only the nodes needed for its context, not the entire source garden.

- relates_to::[\[\[Knowledge Compounds Through Typed Edges Not Filing\]\]](../patterns/Knowledge%20Compounds%20Through%20Typed%20Edges%20Not%20Filing.html)
  - A patch's value comes from the typed edges between nodes, not from the folder structure — the same principle that makes gardens work.
