# Voice: business-technical

How to sound when writing for colleagues who have to act on what you wrote.
Applies to everything written inside a working repository, and to a report or
brief written for a named reader outside one.

**Scope.** This file governs prose choices: register, sentences, words,
paragraph flow. It does not say what a document must contain, which sections it
carries, how it is ordered, or how long it runs. Those are document-type
obligations and live in `document-types-code-repo.md`. Where an obligation
and a voice preference conflict, the obligation wins.

---

## Register

The reader is whoever the document names, and the reader profiles
(`reader-*.md`) say what each already holds and can check. Inside a repository
that is usually `reader-owner-and-agents.md`: a colleague, mid-task, who will
act on what you wrote. They already accept that the document has authority, so
you are informing them rather than winning them over. A rhetorical figure costs
them time and buys nothing.

Address them as a colleague. Do not perform.

**A reader who has not granted the authority yet needs something else from the
same sentences.** `reader-owner.md` approving a design, a spec or a plan is
deciding whether to give it authority, and can decide only against claims they
can check. Name the thing, give the number, cite the path. Persuasion is still
not the job: an approval given to prose the approver could not check records
nothing.

## Sentences

`voice-base.md` holds the rules on one idea per sentence, subordination and
active voice. These add to them.

- Give every sentence a subject and a finite verb. A fragment reads as a
  pronouncement.
- Put the subject first and the verb next.
- Make every contrast do work. See **Contrast** below.
- Aim to keep a sentence under 35 words, with a median near 12 to 15.
- Do not end a paragraph on a short line for emphasis.

## Contrast

A contrast earns its place when the reader might otherwise land on the wrong
side of it. Write `X, not Y` where someone would plausibly conclude Y, and Y is
a real alternative in this document's vocabulary. Cut it where Y exists only to
be denied.

Three tests, in order of how much they settle:

1. **Would a competent reader actually reach Y?** *"an entity, not a repeated
   attribute"* — yes, that is the classification error the rule exists to
   prevent. *"a veto, not a vote"* — no, nobody was going to say vote, and the
   word arrived so it could be rejected.
2. **Does Y appear elsewhere in the document as a real thing?** A term that
   turns up only inside the contrast was manufactured for it.
3. **Does cutting the clause change what the rule permits?** If the sentence
   constrains the same cases without `not Y`, the clause was rhythm.

Symmetry is the tell of the decorative kind: matched clause lengths, matched
grammar, often matched sounds. A working contrast is usually lopsided, because
its two sides are not equally important.

## Words

`voice-base.md` holds the rules on plain words, cutting and metaphor. Two more
apply here.

- Name the concrete thing. Prefer "the source system" to "the world", and "the
  analyst querying this" to "a consumer".
- An adjective is not evidence. Where a claim needs support, the sentence needs a
  number, a name or a path.

## Explanation

When a technical finding is unfamiliar, explain it in the reader's order:

1. what happened or what is true;
2. why it matters to the decision or action;
3. the smallest concrete example that makes the distinction visible;
4. the mechanism, only where the reader still needs it.

Keep the precise term and gloss it rather than replacing it with a vague one.
Use more than one example when the cases behave differently. After drafting,
ask whether the intended reader could explain the finding and its consequence
in their own words while using any necessary exact term correctly. If not,
simplify the explanation or improve the gloss.

## Paragraphs

`voice-base.md` holds the rules on chunking, lists, and opening with what the
reader already has. These add to them.

- One claim per paragraph, stated in its first sentence. An orientation or
  routing paragraph may instead name the document's topic, questions and
  readers; `document-types-code-repo.md` governs that opening.
- Keep paragraphs to four or five sentences.

## Figures to avoid

- Rhetorical questions.
- One-line paragraphs for drama.
- A closing sentence that restates the paragraph.
- The AI-isms listed in `voice-base.md`, unmasking language included.

## Checks

Each check is a regex, so a host can report it. Counts run over prose
paragraphs. Exclude frontmatter, fenced code, tables, headings, and list items,
including the em dash that separates a list label from its value. A document
built mostly from label bullets otherwise fails dash density on its formatting
rather than on its prose.

| Check | Look for | Act when |
|---|---|---|
| manufactured contrast | `, not X` where X appears nowhere else in the document | any |
| symmetric contrast | the two sides within one word of each other in length | advisory — read each one and apply the three tests |
| sentence length | sentences over 35 words | advisory — reread each one and split it if that lowers reader effort |
| subordination | `which`, `that`, `because`, `although`, `while`, `whereas`, `since` | advisory over 0.25 per sentence — inspect rather than reject by count |
| fragments | sentences carrying no finite verb | advisory — no regex detects this reliably, so read for it |
| adjective as evidence | significant, substantial, considerable, clear, key | any, outside a quoted term of art or a heading the host fixes |
| closing restatement | last sentence repeats the paragraph's first | any |
| dash density | `—` in prose | over 5 per 1,000 words |

A count finds what a read-through hides.

These checks are specified for a host to implement. This plugin ships prose and
no scripts, so installing it adds no executable surface; a project that wants
them enforced builds them against the body defined above.
