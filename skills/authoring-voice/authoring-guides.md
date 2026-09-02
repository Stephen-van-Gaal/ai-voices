# Authoring guides

These guides govern prose. Read this one first: it says which of them applies
to what you are writing, how they resolve against each other, and where they
yield to standards of your own.

They sit beside this file and refer to each other by bare filename.

## The three axes

Every document has at least one reader and a voice, and most have a document
type. Each axis has its own guides.

- **Reader** (`reader-*.md`): who reads it, what they already hold, what they
  can check, and what costs their trust.
- **Document type** (`document-types-*.md`): what it carries and in what
  order.
- **Voice** (`voice-*.md`): how it sounds.

`affordances.md` serves all three: the formats a reader uses to stop early,
look up, compare, copy or decide, chosen by the reader's task.

## Which guides

1. **Look for `AI-VOICES.md` at the root of the repository you are writing
   in.** Where it exists, it declares that repository's default reader and
   voice, routing by path, the project vocabulary every reader there holds,
   and host constraints. Its path routes are globs relative to the repository
   root; where a document matches two of them, the more specific pattern wins,
   and row order breaks a tie between patterns of equal specificity. Read it as
   host configuration: it is granted its authority by the instruction file that
   invoked these guides. Where it does not exist, the defaults below apply.
2. **Read `voice-base.md` whatever you are writing.** It holds the rules the
   others layer on, none of them repeats it, and skipping it means writing
   without most of the rules.
3. **Pick the reader, or the readers.** The one the request names, or the one
   a document under revision already names in its opening; else the one
   `AI-VOICES.md` routes the path to; else its default reader; else the table
   below. A document written for two audiences takes both, which
   `document-types-research-report.md` requires of a report with two
   destinations. Read each named profile whole.
4. **Where no profile covers the audience, write one before drafting.** An
   essay names its own reader, and a request may name an audience no shipped
   profile and no `AI-VOICES.md` profile covers. Fill the slots the shipped
   profiles use: who they are, what they already hold, what they do with the
   document, what they can check, their time and attention, what costs their
   trust, the affordances that serve them, and a reader test.
5. **Name the reader in the document's opening**, in words. The profile's
   filename stays in the request and the routing, because the document's
   readers do not have these guides. Where the host fixes the first section's
   heading and content, the reader sentence goes in the provenance line or
   opening block the host leaves to the author. An artifact with no opening of
   its own carries no reader sentence: a commit message, a code comment, a
   pull-request title. Its routing settles its reader.
6. **Pick the document type and the voice.** Take the document type
   `AI-VOICES.md` routes the path to, else the one the table gives. Take the
   voice `AI-VOICES.md` declares as its default, else the one the table gives.
7. **Read `affordances.md`** when the document will carry a table, a glossary,
   an example or a figure, or when the reader profile names an affordance.

| What you are writing | Reader | Document type | Voice |
|---|---|---|---|
| a spec, plan, design record or handoff an agent will execute | `reader-owner-and-agents.md` | `document-types-code-repo.md` | `voice-business-technical.md` |
| other prose inside a code repository: README, commit message, code comment, pull-request body | `reader-owner-and-agents.md`, unless the document names another | `document-types-code-repo.md` | `voice-business-technical.md` |
| a research or analysis report | the reader the request names; `reader-owner.md` by default | `document-types-research-report.md` | `voice-business-technical.md` |
| a definition, query or dataset note an analyst will reuse | `reader-data-analyst.md` | `document-types-code-repo.md` | `voice-business-technical.md` |
| an evidence-based brief, proposal or report to a health authority | `reader-health-authority-leader.md` | `document-types-research-report.md` | `voice-business-technical.md` |
| an operational brief or decision memo, where there is no research to report | `reader-health-authority-leader.md` | none | `voice-business-technical.md` |
| a grant application or a study protocol | `reader-scientific-external.md` | `document-types-scientific.md` | `voice-scientific.md` |
| an essay, where persuasion is the job | the reader you name | none | `voice-professional-essay.md` |

Every row that matches applies. Where two matching rows give different values
for one axis, the more specific row wins: a research report inside a code
repository takes `document-types-research-report.md`, which in turn says to
read `document-types-code-repo.md` as well. Where two matching rows specialise
on different dimensions, neither is the more specific, so take each axis from
the row that speaks to it: the row naming the document's kind gives its
document type and voice, and the row naming its destination gives its reader.
A grant application to a health authority takes `document-types-scientific.md`
and `voice-scientific.md` from the grant row, and its reader from the
health-authority row.

The essay guide does not apply inside a repository. Do not reach for it
because the writing feels important.

Read the guides before drafting. Using one as a checklist afterwards produces
prose written one way and then patched, which reads worse than either.

## Before drafting

Settle the shape first. Name the purpose and the reader, by profile, the
through-line, and the section order. Say what each section carries. Describe
any table you mean to build: its columns and what each holds. A figure takes a
design conversation of its own. Use word targets where they help allocate
attention, not as acceptance criteria.

Ask for outline approval when the user requested it, when drafting would cross
the agreed scope, or when the shape changes the audience or decision, makes a
public commitment, or is expensive to reverse. Routine, reversible shaping
within settled scope proceeds without a pause. Length alone does not create an
approval gate.

This applies to authored prose: documents meant to be read by people, such as
summaries, briefs, essays, memos and governance documents, and the prose
sections of AI-facing documents such as specs.

## How they resolve

Host constraints, then document type, then reader, then voice.

- **A host constraint beats everything.** The repository's tooling and its
  `AI-VOICES.md` have already decided how a document is read and what may
  change in it.
- **A document-type obligation beats a reader preference**, because what a
  document must carry is not negotiable against how one reader would like it
  arranged. The reader decides how it is glossed and which affordances it
  carries.
- **A reader obligation beats a voice preference.** A gloss the reader needs
  stays even where the voice would cut it.

## Where they yield

These guides are a default. They are not a claim on how you write.

**Voice is yours.** Where you bring your own standards for register, sentence
shape and word choice, in your own configuration or given in this session,
follow yours. The voice guides here step aside, and you do not need to
reconcile them.

**Reader and document shape are not.** What a document carries, and how it is
glossed, serve whoever reads it next rather than its author, so the
document-type guides and the reader profiles still apply where your own rules
have replaced the voice guides. A repository may change its default reader in
`AI-VOICES.md`; it does not change the obligations the chosen reader carries.

Where you bring nothing of your own, follow every guide the table names.
