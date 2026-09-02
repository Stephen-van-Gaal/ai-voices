# Reader: the owner

The person who owns the repository and directs the agents working in it. A
clinician and health-services researcher who is learning computing while using
it. Reads to decide, and to learn enough to explain the decision to someone
else. This is also the reader who has not yet granted a document its
authority: someone approving a design, a spec or a plan can decide only
against claims they can check.

- **What they already hold.** Clinical medicine and health-system operations,
  as an expert. SQL and git, solidly. Python, still developing: an idiom or a
  library pattern needs a sentence. Shell, regular expressions, and
  infrastructure (CI runners, APIs, hooks, tokens, caching, process models)
  barely at all, and that is where writing most often goes over their head.
- **What they do with the document.** Approve or withhold approval; act on a
  finding; carry the reasoning to a colleague. They read once, whole, and
  they do not skim.
- **What they can check.** A clinical claim, a query, a git operation, whether
  a named path exists. They cannot check an infrastructure claim, a protocol
  detail or a mechanism inside a tool without a gloss, so a sentence resting
  on one of those needs the gloss beside it.
- **Time and attention.** Enough to read the whole document once with care.
  Not enough to read it twice, so a sentence that needs a second read costs
  the meaning rather than the time.
- **What costs their trust.** A claim with no number, name or path. A
  prediction reported as a result ("should work now"). A mechanism asserted
  with no sentence saying how it works. Opening praise, and agreement that
  carries no information.
- **Affordances that serve them.** A worked example for any construct outside
  their vocabulary. A one-sentence gloss of a mechanism beside its first use.
  A boundary-case table where two things look alike and differ. A decision
  path where a choice is put to them, with what turns on it stated first.
- **Reader test.** Could they explain the finding, and how it works, to a
  colleague in one sentence each?
