# Reader-centered analytical writing implementation plan

**Goal:** Make the canonical authoring guidance produce analytical documents that orient readers, explain technical findings plainly, and preserve evidence needed to judge confidence.

**Scope:** Change the ai-voices guidance and validate its behavior. Cedar-specific templates and instruction trimming remain a dependent follow-up after this version is merged, released, and installed.

## Task 1: Establish the behavioral baseline

Run three fresh-context pressure scenarios against the current guide:

1. revise an analytical report when clarity requires added explanation and examples;
2. open an analytical report for implementer and approver readers;
3. apply a host repository's evidence vocabulary.

Record the contradictions, ambiguity, and undesirable constraints produced by the current text.

## Task 2: Revise the canonical guidance

Edit:

- `skills/authoring-voice/voice-base.md`
- `skills/authoring-voice/voice-business-technical.md`
- `skills/authoring-voice/document-types-code-repo.md`

The revised rules must:

- make outline review proportional to risk instead of imposing a universal word-count gate;
- preserve failed or superseded work when it affects confidence or prevents recurrence;
- order technical explanation as finding, significance, example, then mechanism;
- treat sentence-length and subordination counts as diagnostic prompts;
- define a short orientation block for analytical and decision documents;
- make objections conditional on a real live objection;
- let host evidence vocabulary override the guide defaults;
- judge revisions by reader effort, allowing justified growth for missing explanation, evidence, examples, or decision context.

## Task 3: Validate the changed skill

Re-run the same three fresh-context scenarios. Confirm that the guide now permits the intended rewrite, produces a usable orientation block, and preserves the host vocabulary without contradictory checks.

Run the skill validator, inspect the diff, and scan for internal cross-reference or wording conflicts.

## Task 4: Prepare release review

Commit the focused change, open a pull request to `main`, and report the dependency boundary: Cedar's instruction must not be trimmed until the new ai-voices version is merged, released, and installed.

## Behavioral validation record

Fresh-context RED scenarios against the previous guidance found that:

- a clearer 1,650–1,800-word rewrite was rejected because surface had to fall and total could not rise;
- the writer had to choose between opening with purpose and readers or opening with the finding;
- host evidence terms survived by precedence but failed the guide's own marker check, which also omitted two of the guide's five default markers.

Fresh-context GREEN scenarios against the revised guidance found that:

- the same growth is permitted only when it supplies missing orientation, explanation, examples, evidence, or decision context and reduces reader effort;
- the analytical opening carries the topic, questions, findings, evidence limits, vocabulary, and reader routing without conflicting with the substantive-section rule;
- the host's evidence terms pass through unchanged and the check recognizes either the host vocabulary or all five defaults.
