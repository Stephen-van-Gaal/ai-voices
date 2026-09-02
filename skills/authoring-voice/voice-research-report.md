# Voice: repository research reports

Read this after `voice-base.md` and `voice-business-technical.md` when a report
inside a code repository turns sources, observed evidence, or both into decision
input. Also read `document-types-code-repo.md`. Its document obligations and the
host repository's required shape take precedence over this guide.

The report has three reading surfaces. Build them in this order so a reader can
stop when they have enough.

## Orientation surface

Open with the answer, why it matters, and the decision the report informs. Name
what the report does not decide when its boundary could otherwise be mistaken
for a recommendation. Route each intended audience to the part that changes
what they should do.

This surface should stand alone for a reader with less than a minute. Keep
source names, search method, and citation detail out of it unless the authority
of a particular source changes the answer.

## Decision surface

Define a load-bearing term before asking the reader to use it. Use one stable
term for each concept. At first use, put the technical term beside a plain
gloss; do not make the reader infer the gloss from examples.

Show how a reader classifies, distinguishes, or acts on the subject. Present
repeated items in the same slots so differences remain visible. For each item,
prefer these slots where they apply:

- what it means;
- a safe example;
- information it must carry;
- operations or uses it supports;
- an inference that its visible form does not support; and
- the strength and source of the supporting evidence.

Give the strongest plausible objection or boundary case near the conclusion it
qualifies. Use synthetic examples unless a real example is itself evidence.

When three or more load-bearing terms fall outside the narrower audience's
working vocabulary, give them a glossary before the classification or
comparison that depends on them. A gloss at first use still helps the prose;
it does not replace the reader's lookup surface.

Choose formats by the reader's task:

| Reader's task | Format | Use it when |
|---|---|---|
| Learn unfamiliar vocabulary | Glossary table: term, plain meaning, why it matters | Three or more technical terms sit outside the narrower audience's working vocabulary. |
| Reach a destination | Classification table or short decision path: question, yes destination, no destination | Answers are mutually exclusive or the order of questions changes the result. |
| Scan the whole model | Compact overview table | Cells can stay short and the table is an index, not the full explanation. |
| Compare repeated subjects | Repeated cards or a field table | Each subject can use the same slots. |
| Avoid a tempting mistake | Boundary-case table: visible form, unsafe inference, information needed | The same surface form can mean different things. |
| Act by role | Action table: reader, action, reason, hand-off | Different audiences leave the report with different work. |

Do not force the whole argument into one table. Keep overview cells to a short
phrase or one sentence. If a subject needs longer cells, several caveats, or
more fields than a reader can scan as one row, keep a compact overview as the
index and move the explanation into repeated cards with stable slots.

## Verification surface

After the decision surface, show how the answer was obtained and how far it can
be trusted. Include the method, evidence coverage, unresolved questions,
limitations, source trace, and references required by the host document.
Distinguish authority from observation: a standard can constrain meaning, while
an example can show that a form occurs without proving what it should mean.

The reader should be able to trace a claim without having to read the trace in
order to understand the claim.

## Revision

Apply the surface and total revision rules in `document-types-code-repo.md`.
Replace explanatory prose with a better route, definition, example, or format;
do not add a second explanation beside the first. A clearer report is usually
shorter at the surface even when its verification record remains complete.
