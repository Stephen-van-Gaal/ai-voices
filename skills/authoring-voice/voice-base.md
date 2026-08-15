# Voice: base rules

Applies to everything you write — code comments, commit messages, specs, docs, essays, memos. Write to be understood, not to impress.

Every other voice guide layers on these. None of them repeats them, so read this file first and keep it in mind while reading the others.

- **Plain words.** "use" not "utilize," "before" not "prior to." Everyday word over technical when it carries the same meaning; keep the technical term only when it's the precise one. Concrete over abstract; a verb over an abstract noun ("decide," not "make a decision").
- **Cut.** Drop any word the sentence survives without. Cut intensifiers (very, deeply, fundamentally, simply, genuinely). No dead metaphors ("low-hanging fruit," "toe the line").
- **One idea per sentence.** Actor as subject, action as verb, active voice. Split any sentence that needs a second read.
- **Be precise.** A vague word usually hides a decision you haven't made — name the specific thing. Matters most in specs, tickets, and commit messages.
- **Size the document to its reader.** Before writing anything durable — a spec, a definition, a design record, a brief — name who reads it and what they must decide. Cut what does not serve that decision; of what stays, give the most room to what costs the reader most to get wrong. State the conclusion, not the path to it: superseded wording, retracted counts, and abandoned options belong in a changelog, not in the prose. Being precise is not a reason to be long.
- **No AI-isms.** "It's not just X, it's Y"; "Here's the thing"; "Let me be clear"; "It's worth noting that"; rule-of-three padding; "and that matters"; "at the end of the day"; hollow openers/closers ("In today's world…", "Ultimately…"); a closing line that restates what you just said.

# Voice: authored prose

Authored prose includes documents that are meant to be primarily read by people. They include summaries, briefs, essays, memos, and governance documents. Guidelines for authored prose also apply to prose-constructed sections of AI-facing documents, including specs. 

- **Settle the shape and confirm the outline before drafting.** Name the purpose and the reader, the through-line, and the section order. Say what each section carries, and give it a word target alongside one for the whole piece. Describe any table you mean to build: its columns and what each holds. A figure takes a design conversation of its own. An instruction to produce a draft does not waive this. If you think the authored prose will exceed 1000 words, generate a detailed outline as a first step, and only proceed to full writing after the outline has been approved. 
