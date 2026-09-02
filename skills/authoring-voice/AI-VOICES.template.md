# AI-VOICES

<!-- GUIDANCE: This file declares how the authoring-voice guides apply in this
repository. Copy it to the repository root as AI-VOICES.md and keep this
heading. Fill each slot below or delete the slot; an agent reading the guides
treats a missing slot as "use the default". Delete each GUIDANCE comment when
its slot is filled. A GUIDANCE comment still present marks an unfilled slot. -->

## Default reader

<!-- GUIDANCE: One reader profile from the guides (`reader-owner.md`,
`reader-owner-and-agents.md`, `reader-health-authority-leader.md`,
`reader-scientific-external.md`, `reader-data-analyst.md`) or one defined under
Additional readers. Name it as the guides do, with the `.md` extension. A
document that names its own reader overrides this. Empty means the routing
table in `authoring-guides.md` decides. -->

## Default voice

<!-- GUIDANCE: One voice guide (`voice-business-technical.md`,
`voice-scientific.md`, `voice-professional-essay.md`), named with the `.md`
extension. Empty means the routing table decides. -->

## Routing by path

<!-- GUIDANCE: One row per path pattern. A document under that path takes the
reader and document type given, unless the document names another reader in
its opening. `authoring-guides.md` defines the pattern syntax and the
precedence between overlapping rows, so those rules survive this comment being
deleted. Empty means only the defaults above apply. -->

| Path | Reader | Document type |
|---|---|---|

## Project vocabulary

<!-- GUIDANCE: Terms every reader of this repository is assumed to hold. A
document here does not gloss a term listed in this table. Give the term and
one line of meaning, so a new reader can learn it here once. Listing a term
exempts the term, not a trap in it: where a listed term's meaning differs from
its visible form, the document still says so. Empty means every term outside
the reader profile is glossed at first use. -->

| Term | Meaning |
|---|---|

## Host constraints

<!-- GUIDANCE: What this repository's tooling has already decided: the
evidence vocabulary (for instance measured, built, cited) and the marker
form a claim carries it in, heading rules,
records policy, diagram format, the id-spaces where a cited slug resolves,
whether a contents generator exists, and the value set a frontmatter field
such as tags takes. These win over every guide. State each as a rule an agent
can apply. Empty means the guides' defaults apply. -->

## Additional readers

<!-- GUIDANCE: Define a reader in the same slots the guides use: who they are;
what they already hold; what they do with the document; what they can check;
time and attention; what costs their trust; affordances that serve them; a
reader test. Name it `reader-<something>.md`, so a routing row cites it the
way it cites a shipped profile. Empty means only the guides' own readers exist
here. -->
