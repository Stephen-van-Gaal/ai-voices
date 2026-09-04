---
name: revise-for-reader
description: Use when revising a document that already exists — re-aiming it at a reader it was not written for, or tuning it for the reader it already has. Derives what must change by diffing the source reader profile against the target profile, works from structure down to sentences, and verifies the result against the target reader's own test. Use authoring-voice instead when drafting something new. Where the person writing brings their own standards for voice, theirs apply instead and these step aside.
allowed-tools: Read, Glob, Grep, Edit, Write
---

# Revise for a reader

This skill revises a document that already exists. It covers two jobs: re-aiming
a document at a reader it was not written for, and tuning one for the reader it
already has. Both run the procedure below, and the target reader decides which
of the two you are doing.

The reader of this file is an agent executing a revision and the owner
approving it. The guides it cites sit in the sibling skill and are named by
relative path: `../authoring-voice/voice-base.md`. Read
`../authoring-voice/authoring-guides.md` first, as that file directs, then read
this one.

**The operative rule: a reader profile is a specification, so a revision is a
diff between two specifications.** The profiles state what a reader holds, what
they do with the document, what they can check, and what costs their trust. A
difference between two profiles is the edit list. Revising by taste produces
changes nobody can check and the owner cannot correct.

## When to stop

Stop and ask before doing anything else in these four cases. Each one makes a
revision that looks finished and has silently changed the wrong thing.

- **The source reader does not resolve.** Step 1 says where to look. A revision
  that guesses the original audience rewrites the document against a reader it
  invented.
- **No profile covers the target reader.** Write the profile first, filling the
  eight slots the shipped profiles use. `../authoring-voice/authoring-guides.md`
  step 5 governs this, and `reader-diff.md` cannot run against a profile that
  does not exist.
- **A host constraint forbids the change.** A schema that rejects a frontmatter
  key, a records policy that requires a supersession marker to stand, tooling
  that resolves a section by its heading text. `../authoring-voice/document-types-code-repo.md`
  § What the host constrains says the host wins.
- **The document is a record.** A changelog, a decision log or an immutable
  decision record states what happened. Rewriting one falsifies it.

## The procedure

Run these in order. Step 5 decides how much of steps 6 and 7 you do, and the
sequence ends when step 8 passes or reports what it could not verify.

1. **Settle the scope and the readers.** Say whether the remit is the whole
   document or one section, because several rules can only be executed at
   document scope; `../authoring-voice/document-types-code-repo.md` § Scope of a
   rewrite governs both. Resolve the source reader from the document's
   `ai-voices` frontmatter block, else the repository's `AI-VOICES.md` routing,
   else the reader named in the document's opening. Take the target reader from
   the request. Ask the owner for what a read cannot recover: what must not
   change, what happens to the original, and any constraint the document does
   not state. Do not ask what is wrong with the document.

   Then record the host's **output obligations** separately from its
   prohibitions. A prohibition says what you may not change, and **When to stop**
   covers those. An obligation says what the result must carry however much it
   changes, and nothing else in this procedure looks for one. Read the
   repository's `AI-VOICES.md` and its instruction files for the evidence scheme
   the output must use, the document shape it must take, and the rules binding
   its identifiers. Step 8 verifies the result against this list. A revision
   that satisfies every prohibition and no obligation still fails its host.

2. **Read the document yourself, against the target profile, slot by slot.**
   Take every slot whether or not anyone has mentioned it. Ask what the document
   would look like written today for this reader, rather than what is wrong with
   the one in front of you; the second question preserves the shape you already
   have, and `../authoring-voice/document-types-code-repo.md` § When you are
   revising states the rule. Record each finding with the slot it comes from and
   the level it sits at, per **Choosing the disposition** below. A finding that
   cites no slot is taste, so cut it.

3. **Reconcile your read with what the owner told you.** Where a complaint you
   were given matches a finding, say so. Where your read contradicts it, say
   that plainly and give the evidence, because a complaint names a symptom and
   the owner is entitled to the diagnosis. Where the read found something the
   complaint missed, add it. A complaint you cannot substantiate still gets
   reported as unsubstantiated rather than quietly dropped.

4. **Inventory what must survive, as a table rather than a list.** One row per
   load-bearing item, and these columns:

   | Column | Holds |
   |---|---|
   | Item | The claim, number, caveat, confidence boundary, commitment or named accountability |
   | Evidence marker | How it is known, in the host's evidence vocabulary |
   | Provenance | What produced it: the probe, run, source document or person |
   | Identifier | The slug or id it is cited by, where it has one |
   | Fate | Filled at step 8: carried, emitted, or dropped with a reason |

   Write the table even where a column is empty for every row, because a column
   nobody filled is visibly unanswered and a sentence nobody wrote is not. A
   prose list lets you check the cheap attribute and call the item checked: the
   numbers are trivially verifiable and a provenance field is not, so the check
   runs where the light is. Step 8 walks this table by column.

5. **Choose the disposition**, using the table below. Say which one you chose
   and what the finding levels were that decided it.

6. **Agree the plan before changing prose**, for any disposition above *tune*.
   Give the owner the disposition, the finding levels, the survival inventory,
   and what the document will look like when it is done. A tune proceeds without
   a pause.

7. **Revise from the top down.** Take structure before sections, sections before
   paragraphs, and paragraphs before sentences. Never spend effort at a lower
   level on material a higher level will delete, because a polished sentence in
   a cut section is wasted work and it makes the cut harder to make. Where a
   section-scoped revision produces content its section cannot hold, emit a
   `BELONGS ELSEWHERE` block rather than dropping it or inlining it.

8. **Verify.** Four checks, and report what each returned rather than that it
   ran.

   Run the target profile's own reader test against the result. Where the test
   asks something only a person can answer, say that it could not be run and
   name what you supplied instead of running it.

   **Walk the step 4 table by column, not by row.** Fill the Fate column for
   every row, then report each column's total separately: items carried,
   evidence markers carried, provenance carried, identifiers carried. A row
   whose Item survived and whose Provenance did not is a partial loss, and
   reporting by row hides it behind the attribute that did survive. An
   identifier is carried or emitted, never dropped, because it is how another
   document cites this evidence.

   Check the result against the output obligations recorded at step 1, naming
   each obligation and how the result meets it. A host rule may permit an
   obligation to be discharged some other way. A derivative section can name its
   source once in place of a marker on every claim. Say which route you took,
   and show that you took it.

   Report the three numbers `../authoring-voice/document-types-code-repo.md`
   § When you are revising requires — surface, total and emitted — and name the
   reader need that any material growth serves. Where the revision produced a
   new document and left the original standing, nothing was reduced: report what
   this reader now reads and what the repository gained.

## Choosing the disposition

The disposition follows from how far up the levels the findings reach. Work out
the highest level any finding sits at, and take the row that matches. A revision
never starts at a lower level than its highest finding.

| Level | A finding at this level says | Disposition |
|---|---|---|
| 1 — job | The document does not do what this reader needs at all, or serves two readers who need different documents | Redraft from the evidence, or split into two documents |
| 2 — structure | The content is right and its order, sectioning or opening is wrong for this reader | Restructure |
| 3 — content | Sections carry the wrong material for this reader: missing glosses, missing decision context, method they cannot check | Re-aim |
| 4 — prose | Structure and content hold, and the sentences cost the reader more than they need to | Tune |
| none | The findings are about something the document should not fix | Leave it, and say why |

Two rules govern the table. A document serving two readers splits rather than
compromises: `../authoring-voice/authoring-guides.md` step 4 permits one profile
per document, and a compromise serves neither reader. The second rule decides
what happens to the original. Where the reader changes, the revision produces a
new document beside the original, which still serves the reader it was written
for. Where the reader does not change, the revision replaces what is there.

## What this skill does not decide

It owns the procedure and nothing else. Four things belong elsewhere, and taking
them from here rather than from their own guide is how a revision drifts from
the standards the repository already set.

- **What a document must carry, and in what order.** The
  `../authoring-voice/document-types-*.md` guides own this, including the rules
  on rewrite scope, the appendix, records and identifiers.
- **How the prose sounds.** `../authoring-voice/voice-base.md` and the
  `../authoring-voice/voice-*.md` guides own register, sentences and words.
- **Which formats serve which reader task.** `../authoring-voice/affordances.md`
  owns this, and `reader-diff.md` cites it rather than restating it.
- **Who the reader is.** The profiles own that, and the routing in
  `../authoring-voice/authoring-guides.md` settles which profile applies.
