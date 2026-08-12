# ai-voices

Writing guides for AI agents: how prose inside a repository should sound, and
what a document has to carry. They install as a Claude Code skill, so an agent
reads them before drafting rather than after.

These are one author's standards, kept here because they need to reach every
project he works in and every agent working alongside him. They are published
rather than kept private so that anyone who finds them useful can take them —
but they were written to serve his writing, not to settle how anyone else should
write. Adapt freely; the guides expect it.

## What is here

Everything lives in `skills/authoring-voice/`. Start with `authoring-guides.md`:
it routes you to the guide that applies, says how the guides resolve against each
other, and says where they yield.

| Guide | What it governs |
|---|---|
| `voice-base.md` | The rules underneath everything. No other guide repeats them. |
| `voice-business-technical.md` | How prose inside a repository sounds: register, sentences, words, flow. |
| `document-types-code-repo.md` | What a document carries and in what order. |
| `voice-professional-essay.md` | Essays, where persuasion is the job. Not for use inside a repository. |
| `voice-scientific.md` | Grant applications and study protocols. |

The guides reference each other by bare filename and name nothing outside this
directory, so they resolve wherever they are read from.

## Precedence

The guides state it themselves, and it is the part most worth knowing before you
install them:

**Voice is yours.** If you bring your own standards for register, sentence shape
and word choice, follow yours. These step aside, and you do not have to reconcile
them.

**Document shape is not.** What a document carries and in what order serves
whoever reads it next rather than its author, so `document-types-code-repo.md`
still applies where your own rules have replaced the voice guides.

## Using them

Install the plugin and invoke the `authoring-voice` skill before drafting. An
agent that reads a guide afterwards produces prose written one way and then
patched, which reads worse than either.

To make them apply without being asked, add a line to your own agent instruction
file telling the agent to invoke `authoring-voice` before writing prose.

## Adapting them

Fork it. The guides are prose, and every rule states its reason, so you can tell
which ones you disagree with and why. Two things are worth keeping if you change
anything else: read `voice-base.md` first, because nothing else repeats it, and
keep cross-references as bare filenames, because a path-qualified reference only
resolves in the one place it was written.
