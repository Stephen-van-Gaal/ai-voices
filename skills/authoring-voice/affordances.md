# Affordances

An affordance is a format that lets a reader do something prose alone would
not: stop early, look a term up, compare two things, copy an identifier,
reach a decision. Choose one by the reader's task, never by how much there is
to say. Each reader profile names the affordances that serve that reader.

## By the reader's task

| Reader's task | Format | Use it when |
|---|---|---|
| Stop after a minute | Summary block: the answer, why it matters, the decision it informs, the ask | The reader may read nothing else. It stands alone. |
| Learn unfamiliar vocabulary | Glossary table: term, plain meaning, why it matters here | Three or more terms fall outside the reader's vocabulary. A gloss at first use still applies; the glossary is the lookup surface. |
| Reach a destination | Decision path: question, yes destination, no destination | Answers are mutually exclusive, or the order of questions changes the result. |
| Scan the whole model | Overview table with short cells | The table is an index to the explanation, not the explanation. A plain-meaning cell belongs in it. |
| Compare repeated subjects | Repeated cards, or a field table, with the same slots for every subject | Each subject can use the same slots, so differences stay visible. |
| Avoid a tempting mistake | Boundary-case table: visible form, unsafe inference, information needed | The same surface form can mean different things. |
| Act by role | Action table: reader, action, reason, hand-off | Different readers leave the document with different work. |
| Copy something exactly | Inline code for an identifier or path named in a sentence; a block for a query, a command, or anything copied as one unit | Always. An identifier retyped by hand gets retyped wrong. |
| See how it goes | Worked example: the input, the steps, the output, with a known answer | The reader will apply the rule to a case the rule does not name. |
| See a structure | Diagram, under **Diagrams** below | A flow, a sequence, or a set of relationships the reader would otherwise reconstruct from prose. |

## Rules for any of them

- **One sentence before it says what it holds and how to read it.** A table
  dropped in without one makes the reader work out its purpose from its cells.
- **It replaces prose; it does not sit beside prose saying the same.** Two
  copies of one fact drift. A gloss is not a copy of a fact: a plain-meaning
  cell in an overview table, or a glossary entry that a card also defines,
  serves the reader who stops at the index or the glossary, and stays.
- **Keep table cells to a phrase or one sentence.** Where a subject needs
  longer cells, several caveats, or more fields than a reader can scan as one
  row, keep a compact overview as the index and move the explanation into
  repeated cards with stable slots.
- **Do not force the whole argument into one table.** A table holds what is
  the same shape across items. The argument stays in prose.
- **Match the slots to the reader's task, and leave a slot empty rather than
  force it.** A forced slot is worse than none.

## Diagrams

- **A diagram earns its place** where the reader would otherwise reconstruct
  a flow, a sequence or a set of relationships from prose. It does not earn
  one as decoration, or for what a two-row table already holds.
- **Write the source as a Mermaid fence in the document.** It diffs, it renders
  in the repository, and it carries no binary. An image file is a second
  artifact that goes stale on its own.
- **The caption states the finding.** The diagram is evidence for it, the way
  a number is evidence for a claim. A caption that names only the subject
  ("system overview") leaves the reader to draw the conclusion.
- **Label nodes with the terms the prose uses.** A diagram that renames its
  subjects makes the reader map two vocabularies.
- **A figure takes a design conversation before it is drawn.** Settle what it
  shows, for which reader, and what its caption will say. Diagram craft
  beyond that (which type, how to lay it out) is not covered here yet.
