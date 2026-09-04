# Document types: research and analysis reports

What a report that turns sources, observed evidence, or both into decision
input must carry, and in what order. Read it with the profile of the reader
the report is for. Where the report lives in a code repository, read
`document-types-code-repo.md` too; its obligations also apply there, and the
host repository's required shape takes precedence over this guide. A brief or
proposal sent outside a repository takes this guide alone.

The report has three reading surfaces. Build them in this order, so a reader
can stop when they have enough.

## Orientation surface

- **Open with the answer, why it matters, and the decision the report
  informs.** Name what the report does not decide where its boundary could be
  mistaken for a recommendation.
- **Route each intended reader to the part that changes what they should
  do.** A report read by a health authority leader and by a data analyst has
  two destinations, and the opening names both. One profile, written for both,
  says who they are; `authoring-guides.md` says why a document takes one.
- **This surface stands alone for a reader with less than a minute.** It is
  the summary block in `affordances.md`, and the document's opening; do not
  write both. Keep source names, search method and citation detail out of it,
  unless the authority of one source changes the answer.

## Decision surface

- **Define a load-bearing term before asking the reader to use it.** Use one
  stable term per concept. At first use, put the technical term beside a plain
  gloss; do not make the reader infer the gloss from examples.
- **Show how a reader classifies, distinguishes or acts on the subject.**
  Where the report classifies or compares, present repeated items in the same
  slots, so differences remain visible:
  what it means; a safe example; the information it must carry; the
  operations or uses it supports; an inference its visible form does not
  support; and the strength and source of the supporting evidence.
- **Put the strongest plausible objection or boundary case beside the
  conclusion it qualifies.** Use synthetic examples unless a real example is
  itself evidence.
- **Give a glossary once three or more load-bearing terms fall outside the
  reader profile's vocabulary**, before the classification or comparison that
  depends on them.
- **Choose formats by the reader's task**, from `affordances.md`.

## Verification surface

- **After the decision surface, show how the answer was obtained and how far
  it can be trusted.** Include the method, the evidence coverage, unresolved
  questions, limitations, the source trace, and whatever references the host
  document requires.
- **Distinguish authority from observation.** A standard can constrain
  meaning; an example can show that a form occurs without proving what it
  should mean.
- **A reader traces a claim without having to read the trace to understand
  the claim.** The decision surface carries the claim; this surface carries
  its provenance.
- **Where a page limit leaves no room for the full trace, keep a limits
  section.** One sentence on the method, the limits that change what the
  reader can conclude, and where the full trace lives. The surface shrinks;
  it does not disappear.

## Revision

A revision reduces reader effort. Replace explanatory prose with a better
route, definition, example or format; do not add a second explanation beside
the first. A clearer report is usually shorter at the surface even when its
verification record stays complete. Inside a repository, the surface and total
rules under **When you are revising** in `document-types-code-repo.md` also
apply.
