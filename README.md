# ai-voices

Writing guides for AI agents: who a document is for, what it has to carry,
and how its prose should sound. They install as a Claude Code skill, so an
agent reads them before drafting rather than after.

These are one author's standards, kept here because they need to reach every
project he works in and every agent working alongside him. They are published
rather than kept private so that anyone who finds them useful can take them —
but they were written to serve his writing, not to settle how anyone else should
write. Adapt freely; the guides expect it.

## What is here

Everything lives in `skills/authoring-voice/`. Start with `authoring-guides.md`:
it routes you to the guides that apply, says how they resolve against each
other, and says where they yield.

The guides sit on three axes. Every document takes a voice and at least one
reader; it takes a document type where one covers its kind.

| Axis | Guide | What it governs |
|---|---|---|
| base | `voice-base.md` | The rules underneath everything. No other guide repeats them. |
| reader | `reader-owner.md` | The repository owner: a clinician learning computing, approving and acting on what agents write. |
| reader | `reader-owner-and-agents.md` | A spec, plan or definition one agent executes and the owner approves. |
| reader | `reader-health-authority-leader.md` | Clinical and non-clinical leaders deciding whether to approve or sponsor. |
| reader | `reader-scientific-external.md` | Funders and reviewers; journal editors later. |
| reader | `reader-data-analyst.md` | An analyst reproducing or reusing a definition or query. |
| document type | `document-types-code-repo.md` | What a document inside a repository carries and in what order. |
| document type | `document-types-research-report.md` | The three reading surfaces of a research or analysis report. |
| document type | `document-types-scientific.md` | What a grant or protocol carries and in what order. |
| voice | `voice-business-technical.md` | How prose inside a repository sounds, and a report or brief written for a named reader outside one. |
| voice | `voice-professional-essay.md` | Essays, where persuasion is the job. Not for use inside a repository. |
| voice | `voice-scientific.md` | How grant applications and study protocols sound. |
| shared | `affordances.md` | Tables, glossaries, examples and diagrams, chosen by the reader's task. |
| override | `AI-VOICES.template.md` | The file a repository copies to its root to declare its own defaults. |

The guides reference each other by bare filename and name nothing outside this
directory, so they resolve wherever they are read from.

## Precedence

Host constraints, then document type, then reader, then voice.
`authoring-guides.md` states it in full. The part most worth knowing before you
install them:

**Voice is yours.** If you bring your own standards for register, sentence shape
and word choice, follow yours. These step aside, and you do not have to reconcile
them.

**Reader and document shape are not.** What a document carries, and how it is
glossed, serve whoever reads it next rather than its author, so the
document-type guides and the reader profiles still apply where your own rules
have replaced the voice guides.

## Deploying in a repository

Copy `AI-VOICES.template.md` to the root of the repository as `AI-VOICES.md`
and fill its slots: default reader, default voice, routing by path, the
project vocabulary every reader there holds, host constraints, and any reader
the repository needs that the guides do not ship. Delete the guidance comments
as you fill the slots; one still present marks a slot left unfilled.

A document can also declare its own reader, voice and type in an `ai-voices`
block in its frontmatter, and that block wins over routing by path. Prefer it
wherever a document's audience differs from its neighbours', because a path
route added to capture one file will silently claim the next file added beside
it. The block is namespaced so a host's own `voice` or `readers` key is never
read as a declaration to these guides. `authoring-guides.md` defines it under
**Declaring the guides in frontmatter**.

## Using them

Install the plugin and invoke the `authoring-voice` skill before drafting. An
agent that reads a guide afterwards produces prose written one way and then
patched, which reads worse than either.

To make them apply without being asked, add a line to your own agent instruction
file telling the agent to invoke `authoring-voice` before writing prose.

## What moved in 0.5.0

No file was renamed. Content moved.

| Before | Now |
|---|---|
| base rules restated in the essay and scientific guides | `voice-base.md` only, which now also holds the readability rules and the full AI-ism list |
| grant and protocol shape in `voice-scientific.md` | `document-types-scientific.md` |
| the outline rule in `voice-base.md` | **Before drafting** in `authoring-guides.md` |
| reader descriptions inside the business-technical and document-type guides | the `reader-*.md` profiles |
| the research-report guide proposed as a voice | `document-types-research-report.md` |

## Adapting them

Fork it. The guides are prose, and every rule states its reason, so you can tell
which ones you disagree with and why. They are licensed CC BY 4.0, so adapting
and redistributing them is permitted as long as the source is credited. Two things are worth keeping if you change
anything else: read `voice-base.md` first, because nothing else repeats it, and
keep cross-references as bare filenames, because a path-qualified reference only
resolves in the one place it was written.
