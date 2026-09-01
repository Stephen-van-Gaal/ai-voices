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

Bump the plugin version, commit the focused change, open a pull request to `main`, and report the dependency boundary: Cedar's instruction must not be trimmed until the new ai-voices version is merged, released, and installed.

## Behavioral validation record

Fresh-context RED scenarios against the previous guidance found that:

- a clearer 1,650–1,800-word rewrite was rejected because surface had to fall and total could not rise;
- the writer had to choose between opening with purpose and readers or opening with the finding;
- host evidence terms survived by precedence but failed the guide's own marker check, which also omitted two of the guide's five default markers.

Fresh-context GREEN scenarios against the revised guidance found that:

- the same growth is permitted only when it supplies missing orientation, explanation, examples, evidence, or decision context and reduces reader effort;
- the analytical opening carries the topic, questions, findings, evidence limits, vocabulary, and reader routing without conflicting with the substantive-section rule;
- the host's evidence terms pass through unchanged and the check recognizes either the host vocabulary or all five defaults.

A second paired RED/GREEN battery covered the five remaining behaviors. The
previous guidance paused routine reports over 1,000 words, did not give failed
work a stable evidence category, specified only part of the explanation order,
rejected a 45-word sentence by count, and required an objection and concession
even when none was live. The revised guidance lets settled routine shaping
proceed, keeps confidence-relevant failure evidence near or durably linked to
the finding, specifies finding → consequence → example → mechanism, treats
prose counts as inspection prompts, and forbids manufactured objections.

| Scenario prompt | Expected boundary | RED outcome | GREEN outcome |
|---|---|---|---|
| Draft a routine 1,600-word internal report whose audience, decision scope and section order are settled. | Proceed without an approval pause. | Required outline approval by word count. | Proceeds because routine reversible shaping is settled. |
| Explain failed null and blank tests that limit confidence in published counts and prevent recurrence. | Preserve their effect near or durably linked to the finding. | Retention was possible but not an explicit durable category. | Preserves the effect near the finding, or in an adjacent note or stable linked analysis when no finding surface exists. |
| Explain an unfamiliar technical finding. | Use finding → consequence → example → mechanism. | Required only the finding and consequence. | Requires the full order, with mechanism included only when still needed. |
| Review a precise 45-word sentence with one main idea and necessary relational clauses. | Inspect it; do not reject by count alone. | Failed the 35-word cap. | Triggers an advisory reread and passes if splitting would raise reader effort. |
| Report a simple finding for which no competent reader has a live objection. | Do not invent an objection or concession. | Required both. | Omits both unless they change the conclusion's limit. |

A final forward test confirmed the review fixes: a recognized section-level
evidence scheme remains section-level without added markers; a target document
cannot promote its own prose into host policy; and a record-only document keeps
recurrence evidence in a compact adjacent note or through a stable link.
