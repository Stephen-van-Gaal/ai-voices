# Reader diff

This file turns a pair of reader profiles into an edit list. `SKILL.md` step 2
sends you here once the source and target readers are settled.

Read both profiles whole before using the table. The table says what a
difference in each slot means and what it changes in the document. It does not
say which formats serve which reader task; `../authoring-voice/affordances.md`
owns that, and the affordance row cites it.

## The slots

Take the slots in this order. The early rows change what the document is for,
and the late rows change how it reads, so a difference in row 3 can make a
difference in row 7 irrelevant.

| Slot | What a difference between the profiles means | What changes in the document |
|---|---|---|
| Who they are | The audience named in the opening is now wrong | Rewrite the sentence naming the reader, in words rather than by profile filename |
| What they already hold | The two readers hold different vocabularies | Re-gloss throughout: gloss what the target lacks, and drop a gloss on a term the target holds. Where the two hold different ground rather than more and less of the same, gloss both |
| What they do with the document | The reader leaves with different work | Change the ask, and change which section leads. A reader who approves needs the ask, the cost and the risk before anything else; a reader who executes needs the procedure |
| What they can check | The reader can verify less, or more | Anything the target cannot check is taken on the credibility of what they can, so supply that. Drop evidence aimed at a check the target will not run |
| Time and attention | The reader has more or less of it | Decide whether the opening must stand alone. A reader with minutes reads only the opening, so everything they must have goes above the fold |
| What costs their trust | The failure modes differ | Sweep for each item the target's profile names. Each one is a defect to find and remove, not a preference |
| Affordances that serve them | The formats differ | Add the affordances the target's profile names and remove those that now serve nobody, subject to **What is not an affordance** below. `../authoring-voice/affordances.md` maps the reader's task to the format |
| Reader test | The acceptance condition differs | Nothing, at this step. `SKILL.md` step 8 runs the target's test against the finished revision |

Where a slot is the same in both profiles, it produces no edit. Say so rather
than leaving the row unmentioned, because a slot nobody reported is
indistinguishable from a slot nobody checked.

## What is not an affordance

The affordance row is the only row licensed to remove anything, so it is the row
that removes the wrong thing. **A repeated block carrying an evidence marker, a
provenance link or an identifier is content wearing an affordance's clothes.**
Change how it is presented; never drop what it carries.

Three tests. A block fails to be an affordance if any of them holds.

1. **Does it say how a claim is known?** An evidence marker, a basis field, a
   confidence label. Dropping it turns a sourced claim into an assertion.
2. **Does it name what produced the claim?** A probe, a run, a source document,
   a person. The reader who can check only half the ground needs this to check
   their half.
3. **Does anything outside the document cite it?** A slug, an id, a heading a
   tool resolves. Dropping it breaks every citation, and the citers are not in
   front of you.

A term used by such a block is not jargon to be cut either, where the
repository's `AI-VOICES.md` carries it in the project vocabulary. That list
names what every reader there already holds, so a profile's gloss rules do not
reach it.

Where the target does not need the block's presentation, keep what it carries
and change its form. A per-claim marker becomes a source named once in the
section's opening. A declared identifier becomes a column in the table that
replaced it.

## Worked example

A cohort definition note is being re-aimed. Its original reader is the data
analyst; its new reader is a health authority leader deciding whether to fund
the work the cohort supports.

**The input.** Roughly 1,200 words. It opens with the definition, gives the
inclusion and exclusion rules, carries the SQL that implements them, names the
source tables, and ends with a worked count against one month of data. Every
clinical term appears bare, because the analyst profile says they hold SQL and
not clinical vocabulary, and the note glosses in the other direction.

**The steps.** Take the slots in order:

- *Who they are.* The opening names an analyst reusing a definition. Rewrite it
  to name a leader deciding whether to fund.
- *What they already hold.* The analyst holds SQL and no clinical vocabulary.
  The leader holds neither, and holds governance and operations instead. Every
  SQL identifier now needs a gloss or removal, and the clinical terms need one
  for the first time.
- *What they do with the document.* The analyst runs the query. The leader
  approves, funds or escalates. The definition stops being the point, and the
  ask, the cost and the risk become it. The lead section changes.
- *What they can check.* The analyst checks that the query runs and the count
  matches. The leader can check neither, and takes both on the credibility of
  the ask, the risk and the named owner. The count stays, with its source; the
  SQL that produced it goes.
- *Time and attention.* The analyst reads until they find the query. The leader
  reads minutes, and often only the opening. The opening must now carry the
  answer, the ask, the cost and the risk on its own.
- *What costs their trust.* The leader's profile names overclaim, an unnamed
  risk they already know of, a bare term, a number with no source, and a
  document with no ask or no owner. Sweep for all six.
- *Affordances that serve them.* Drop the code blocks and the worked count in
  its analyst form. Add a summary block, an action-by-role table, a
  boundary-case table for the risks, and a glossary once three terms need one.
- *Reader test.* Not an edit. Step 8 asks whether the leader could say what they
  are being asked to decide, what it costs, and what could go wrong.

**The output.** A different document, beside the original rather than replacing
it, because the analyst still needs the note as it was. It opens with a summary
block carrying the answer, the ask, the cost and the risk. The definition
survives as one glossed paragraph rather than as rules and SQL. The count stays
with its source named. The tables and the query are gone, and the risks arrive
as a boundary-case table.

**The known answer.** The highest finding sat at level 3, so the disposition was
*re-aim* rather than *redraft*: the content was right and the document carried
the wrong material for this reader. The reader changed, so the result is a new
document and the original stands.
