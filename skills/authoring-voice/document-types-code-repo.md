# Document types: code repositories

What a document inside a code repository must carry, and in what order. Voice —
register, sentences, words, paragraph flow — is `voice-business-technical.md`.
Where an obligation here conflicts with a voice preference, this file wins.

---

## Every document

- **Open with what it is for and who reads it.** Where a document serves more
  than one reader, route each to the section that answers them.
- **Route a second reader with a reading profile.** Where whatever serves this
  document can return part of it, declare a named list of sections and hand each
  reader theirs. That list is what the reading surface means for this document.
  Where no such mechanism exists, section order carries the obligation instead:
  keep each reader's sections together and say in the opening where they start.
- **Lead with the conclusion.** Put the finding in the first sentence of the
  document and of each section. Do not build toward it. A reader who stops
  halfway should still have the finding.
- **A section that holds only subsections routes instead.** It has no finding
  of its own, so its opening names what the subsections do and the order to
  take them in. One or two sentences, and they are not a cut.
- **Rank by consequence.** Give the most room to whatever costs the reader most
  to get wrong, and put it first.
- **Size it to its reader.** Cut what does not serve the decision the reader
  came to make.
- **Name the vocabulary you assume.** Say in the opening what the reader is
  expected to know already. Gloss anything outside that once, at first use.
- **A long document carries a contents section.** Past roughly 300 lines or ten
  top-level sections a reader needs navigation. Generate it, and never maintain
  it by hand: a hand-written index is a second copy of the heading list, and it
  goes stale the first time a heading moves.
- **A section takes the class of its job, not the file's.** A reference document
  may hold an explanatory section, and each follows the rules of its own class.
  The unit is the section, so a paragraph inside one does not reclassify itself.
  Where the job is unclear, ask what the reader of that section is doing:
  executing, or deciding whether to agree.

## Reference documents

Specs, definitions, contracts, schemas, runbooks. The reader is executing.

- Write a rule as a condition and an action: *"If two things are different kinds
  of thing clinically, model them as separate entities."* Or as an instruction:
  *"Record which difference you used."*
- State the rule first, then its reason. Send anything longer than the rule
  itself to the appendix: the argument for it, the alternative it rejects,
  the worked example. A reader who accepts the rule never goes there.
- Where a rule has exceptions, write "unless" and list them. An alternative is
  not an exception: where a rule permits either of two routes, keep "or".
  Rewriting a disjunction as an exception narrows what the rule allows.
- Where rules apply in sequence, number them and say what ends the sequence.
- Give repeating items the same slots. For a per-entity note: what it is, its
  status, its open question, why it is shaped this way. Slots stop an item
  growing into an essay. Where a run is not homogeneous — some items carry a
  status and an open question, others are cross-cutting rules with neither —
  slot the ones that fit and leave the rest. A forced slot is worse than none.
- Use a table when every item carries the same fields.
- **Do not imply more certainty than you have.** Reference material takes no
  evidence marker, but where a rule or note rests on contested or unresolved
  evidence, say so in the sentence: what is established, what merely
  corroborates, and what needs data nobody has pulled.
- **Give each rule its reason.** A reader who knows why a rule exists can
  apply it to a case the rule does not name, and can tell when it has stopped
  applying. Budget the reason by how much the rule matters and how contested
  it is: a settled, low-stakes rule takes a clause, and a rule that closes off
  a plausible alternative names that alternative and says why it lost. A
  reason longer than the rule it defends moves to the appendix, and the rule
  keeps a clause in its place.

## Explanatory documents

Design rationale, architecture and vision prose, explainers, framing notes,
papers, longer pull-request descriptions. The reader is deciding whether to
agree.

- One claim per section, stated in its first sentence.
- Support it with numbers, names, file paths and dates.
- **Say how you know.** Mark each claim: measured, built, cited, estimated,
  assumed. State a confidence boundary where one exists. A rule is not a
  claim and takes no marker; its reason belongs under Reference documents.
- **A derivative section cites its source once.** Where every claim in a section
  comes from one named source, name it in the section's first sentence and drop
  the per-claim markers, because marking every sentence of a summary reports
  nothing. A claim needing a marker of its own is a new claim, and a new claim
  does not belong in a derivative section.
- Name the strongest objection and answer it in a sentence.
- Concede a real point in one sentence and carry on.
- A section with no finding is background. Move it to an appendix or cut it.

## Scope of a rewrite

A rewrite is document-scoped or section-scoped. Several rules below can only be
executed at document scope, so say which one you are doing before you start.

**Document-scoped.** The whole file is in play: frontmatter, section order,
sibling sections, the appendix, and every identifier the document owns.

**Section-scoped.** The remit is one section. Do not touch frontmatter, do not
add or remove sibling sections, do not restructure the document, and do not
rename an identifier that is cited outside the section. Most rewriting is
section-scoped, because most requests name a section.

### Emitting content that belongs elsewhere

A section-scoped rewrite regularly produces content its section cannot hold: an
appendix entry, a frontmatter change, a sentence belonging to the
document's opening, a rename that has to land in one pass. Do not drop it, and
do not inline it where it does not belong. Write it below the rewritten section
in a marked block that names its destination and what to do there.

```
<!-- BELONGS ELSEWHERE: docs/foo.md ## Appendix — why these rules
     Add a `### ontological-kind` entry holding the merge-attempt argument,
     removed from Constraints in this rewrite. -->
```

These blocks belong to the handoff, not to the document. Whoever merges the
rewrite applies them, and the markers do not survive into the committed file. A
governed document containing one has an unfinished merge.

This is what restores the appendix at section scope. A section-scoped rewrite
may still move a long reason out of its section: cut it from the section and
emit the appendix entry for merge. The reading surface drops immediately and
the appendix arrives when the handoff is applied.

## The appendix

Where a document carries more justification than its rules can hold, it takes
an appendix. This is the only mechanism for moving content off the reading
surface. A collapsible HTML block is not a substitute: it hides the content from
anyone reading the file as text rather than as a rendered page, and the material
stays in the section it was supposed to leave.

- **Name it, do not position it.** `## Appendix — why these rules`. Heading
  matching is by text, and a positional convention breaks the moment a second
  appendix exists.
- **One subsection per rule, titled with whatever stably names that rule.** The
  slug where the document has slugs: `### ontological-kind`. The rule's own
  heading text where it does not: `### Split tests`. Either makes the anchor
  predictable, so a rule can link to its own reason, and either makes both
  directions checkable: every appendix entry names a real rule, and every rule
  needing an extended reason has one. Do not mint a slug to satisfy this — a
  document still on numbered ids gets an appendix keyed by heading, and the
  rename stays separate work.
- **Mirror the main document's order.** An appendix that does not follow the
  document it serves becomes a drawer.
- **Put it last**, after the changelog. It is the least frequently read part of
  the document.
- **The rule keeps a clause.** Only what runs longer than the rule moves. A
  document whose rules carry no reason at all has emptied itself into its
  appendix.

A document's reading profile omits its appendix, so a reader who asked for the
rules receives them without the argument behind them. Where no profile is
declared, shape carries the obligation instead: the appendix goes last, and a
reader who stops at the rules has already read everything the document asks of
them.

## Identifiers

Applies to both kinds.

**An identifier says what it is.** Where a rule, test or criterion needs a
stable id, make the id a hyphenated slug carrying its meaning:
`ontological-kind`, `attribute-disjointness`, `two-source-systems`. Avoid
numbered forms such as `S4` or `REQ-3`, which cost the reader a lookup at every
citation and carry nothing on their own. The field that holds the slug
supplies its family, so the slug carries no prefix of its own. Prose cites the
slug directly, because it already reads as English.

- Every slug resolves in the id-space that owns it.
- A slug runs to at least two words, and no part of it is an abbreviation.
- A slug that has stopped being accurate needs a rename. Classify who cites
  the id before starting, because that decides what is possible:
  - **Only this document and the machine surfaces it owns.** Rename in one
    pass and delete the number. A self-referencing document has no reason to
    carry a pointer that means nothing to its reader.
  - **Live documents or data owned elsewhere.** The rename is a
    cross-artifact transaction. Change every citation in one pass, or change
    none. Where one pass is not available, keep the number and file the
    rename as work of its own.
  - **Historical records only.** They are not citers. Changelogs, design
    specs and plans record what happened, so renaming their citations would
    falsify them, and the rename proceeds without them.
- A section-scoped rewrite never renames (see **Scope of a rewrite**). It
  leaves the ids alone and emits the rename as follow-up work.

A number also conceals whether a sentence is correct. *"That is S1 and S3
rather than S4"* has the texture of precision. Written as words, a reader can
check it.

## Commit messages and code comments

- Explain why, not what. The diff already says what.
- One logical change per commit.
- A comment states what the code cannot: the constraint, the reason for the
  choice, the case that looks wrong and is not.

## When you are drafting

A first draft has no previous version, so every comparative rule below is
inert. Two things take their place.

- **Set the budget from the reader's decision**, not from a word count. Enough
  to make the decision, and no more. Where a sibling section covers comparable
  ground, match its scale.
- **Gloss your own terms.** The rule that names a document's assumed
  vocabulary lives in its opening, which a section drafted before its document
  does not own. Gloss each term at first use and emit the vocabulary
  declaration for the opening.

## When you are revising

These rules need a previous version. A first draft has nothing to compare
against, so none of them applies to one.

- **A revision removes.** Its job is to take out what the draft did not need. A
  pass that leaves the document longer with the same content reorganised it
  rather than revised it.
- **Structure is paid for.** A heading, a numbered procedure, an appendix entry
  and a full-sentence table cell all cost the reader. Adding one makes
  something else redundant, and cutting that is part of the same pass.
- **Report three numbers, and constrain two.** *Surface* is what a reader gets
  by default: what a declared reading profile returns, or the whole document
  where none is declared; at section scope it is the section as delivered.
  *Total* is everything the rewrite produces, emitted content included.
  *Emitted* is what goes to handoff blocks. **Surface must fall and total must
  not rise.** Surface alone rewards relocation: a rewrite can move a thousand
  words to an appendix, report an improvement, and hand the reader a larger
  artifact.
- **Rewrite, do not annotate.** Strike-through, "superseded by" and
  parenthetical corrections leave the reader assembling the current state out
  of a history. Write what is true now and send the history to the changelog.
- **Ask what the document would look like written today**, not what is wrong
  with the one in front of you. The second question preserves the shape you
  already have.

## What the host constrains

A document lives inside tooling — a site generator, a tool that reads one
section at a time, a policy on what may be edited — that has already decided how
the document is read and what may change in it. Where a rule here meets one of
those decisions, the host wins.

- **Heading text is unique within a document.** A repeated heading makes every
  link to it ambiguous, and makes a request for that section ambiguous too, so
  an appendix entry may not repeat the heading of the rule it defends. Title it
  `Why <rule heading>`.
- **Treat every heading as a section boundary.** Anything that reads part of a
  document splits it at headings, so a subheading inside a section can cut that
  section short. Group items within a section by order, not by subheading.
- **A registered heading is an identifier.** Where the host resolves a document
  by shape, tooling retrieves a section by its heading text, so changing the
  text breaks every caller. Classify the citers and rename on the terms set out
  under **Identifiers**, or leave the heading alone and file the rename as work
  of its own.
- **Decision records are immutable.** Where a records policy requires a
  supersession marker to stand, *rewrite, do not annotate* yields to it. Keep
  the corrected claim off the rule surface instead, so a reader who takes only
  the rules never assembles current state out of history.

Before adding a rule that moves content or names a heading, check it against
whatever the host requires of document structure.

## Checks

Counts run over the body defined under **Checks** in
`voice-business-technical.md`.

| Check | Look for | Act when |
|---|---|---|
| reader routing | an opening that names the reader | missing |
| conclusion first | each section's first sentence states its finding | any section without one |
| numeric id | `[A-Z]{1,2}[0-9]+` outside a historical record | document scope with every live citer in scope; never fires at section scope |
| slug format | one hyphen minimum, no part under three characters | any |
| unresolved slug | a slug cited in prose that is in no id-space | any |
| supersession in place | `~~`, "superseded by", "originally" | any |
| unmarked claim | a load-bearing claim with no measured/built/cited marker | any, in an explanatory section that is not derivative |
| reading surface | words a reader gets by default, before and after | any increase in a rewrite for form |
| orphan appendix entry | an appendix subsection whose slug names no rule | any |
| unfinished merge | `BELONGS ELSEWHERE` in a committed document | any |
| reasonless rule | a rule with neither an inline clause nor an appendix entry | any |
| unglossed term | a term outside the stated assumed vocabulary, used bare | any |
