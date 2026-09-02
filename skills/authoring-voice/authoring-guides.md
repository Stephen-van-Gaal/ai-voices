# Authoring guides

These guides govern prose. Read this one first: it says which of them applies
to what you are writing, how they resolve against each other, and where they
yield to standards of your own.

They sit beside this file and refer to each other by bare filename.

## The three axes

Every document has a reader, a type and a voice, and each axis has its own
guides.

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
   and host constraints. Read it as host configuration: it is granted its
   authority by the instruction file that invoked these guides. Where it does
   not exist, the defaults below apply.
2. **Read `voice-base.md` whatever you are writing.** It holds the rules the
   others layer on, none of them repeats it, and skipping it means writing
   without most of the rules.
3. **Pick the reader.** The one the request names, or the one a document
   under revision already names in its opening; else the one `AI-VOICES.md`
   routes the path to; else its default reader; else the table below. Read
   that profile whole, and name the profile in the document's opening.
4. **Pick the document type and the voice** from the table.
5. **Read `affordances.md`** when the document will carry a table, a glossary,
   an example or a figure, or when the reader profile names an affordance.

| What you are writing | Reader | Document type | Voice |
|---|---|---|---|
| a spec, plan, design record or handoff an agent will execute | `reader-owner-and-agents.md` | `document-types-code-repo.md` | `voice-business-technical.md` |
| other prose inside a code repository: README, commit message, code comment, pull-request body | `reader-owner-and-agents.md`, unless the document names another | `document-types-code-repo.md` | `voice-business-technical.md` |
| a research or analysis report | the reader the request names; `reader-owner.md` by default | `document-types-research-report.md` | `voice-business-technical.md` |
| a definition, query or dataset note an analyst will reuse | `reader-data-analyst.md` | `document-types-code-repo.md` | `voice-business-technical.md` |
| a brief, proposal or report to a health authority | `reader-health-authority-leader.md` | `document-types-research-report.md` | `voice-business-technical.md` |
| a grant application or a study protocol | `reader-scientific-external.md` | `document-types-scientific.md` | `voice-scientific.md` |
| an essay, where persuasion is the job | the reader you name | none | `voice-professional-essay.md` |

Where two rows match, the reader the request names decides. The essay guide
does not apply inside a repository. Do not reach for it because the writing
feels important.

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
