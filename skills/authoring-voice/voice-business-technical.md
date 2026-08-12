# Voice: business-technical

How to sound when writing for colleagues who have to act on what you wrote.
Applies to everything written inside a working repository.

**Scope.** This file governs prose choices: register, sentences, words,
paragraph flow. It does not say what a document must contain, which sections it
carries, how it is ordered, or how long it runs. Those are document-type
obligations and live in `document-types-code-repo.md`. Where an obligation
and a voice preference conflict, the obligation wins.

---

## Register

The reader is a colleague, mid-task, who will act on what you wrote. They
already accept that the document has authority, so you are informing them rather
than winning them over. A rhetorical figure costs them time and buys nothing.

Address them as a colleague. Do not perform.

## Sentences

- Give every sentence a subject and a finite verb. A fragment reads as a
  pronouncement.
- Put the subject first and the verb next.
- Make every contrast do work. See **Contrast** below.
- Split any sentence that rewards a second reading.
- Cap a sentence at 35 words. Aim for a median near 12 to 15.
- Allow one subordinate clause. A second one is a second sentence.
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

- Use the plain word. Keep a technical term where it is the precise one.
- Name the concrete thing. Prefer "the source system" to "the world", and "the
  analyst querying this" to "a consumer".
- Cut intensifiers and any word that asserts weight without supplying it:
  significant, substantial, considerable, critical, key.
- An adjective is not evidence. Where a claim needs support, the sentence needs a
  number, a name or a path.
- Use a metaphor only where it is the shortest accurate description.

## Paragraphs

- One claim per paragraph, stated in its first sentence.
- Open each paragraph with something the reader already has, and close it with
  what is new.
- Keep paragraphs to four or five sentences.
- Use a list for real enumeration. Do not use one to break up an argument.

## Figures to avoid

- Rhetorical questions.
- One-line paragraphs for drama.
- A closing sentence that restates the paragraph.
- Unmasking language: "strip it down", "read plainly", "smuggled in".
- The AI-isms listed in `voice-base.md`.

## Checks

Counts over the document body. Each is a regex, so a script can report them.

| Check | Look for | Act when |
|---|---|---|
| manufactured contrast | `, not X` where X appears nowhere else in the document | any |
| symmetric contrast | the two sides within one word of each other in length | advisory — read each one and apply the three tests |
| sentence length | sentences over 35 words | any |
| subordination | `which`, `that`, `because`, `although`, `while`, `whereas`, `since` | over 0.25 per sentence |
| fragments | sentences carrying no finite verb | advisory — no regex detects this reliably, so read for it |
| adjective as evidence | significant, substantial, considerable, clear, key | any |
| closing restatement | last sentence repeats the paragraph's first | any |
| dash density | `—` in prose, excluding tables and headings | over 5 per 1,000 words |

A count finds what a read-through hides.

Do not write toward a readability score. Sentence length is the half of one that works,
and it is already a check above; the other half rewards a short vague word over a precise
technical one.
