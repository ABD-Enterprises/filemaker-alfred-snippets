<!-- markdownlint-disable-file MD041 -->
<!--
AI reviewers
(Gemini Code Assist, GitHub Copilot, Codex) should auto-populate the
sections below from the diff, the linked issue's ai-task block, and the
CHANGELOG diff. Humans confirm; agents draft.

MD041 (first-line-heading) is disabled because GitHub renders this
template inline as the PR body — a top-level `#` heading here would
render as a giant heading above the user's PR description. The first
section heading is `## Summary` by design.
-->

## Summary

<!-- 1-2 sentences. What changed and why. AI reviewers: derive from the diff
     and the linked issue's `done_when` clauses. -->

## Linked issue

<!-- Link the issue this change resolves, or carry the `chore:trivial`
     label. No CI or merge gate reads this section. -->

Closes #__ISSUE__

## Changes

<!-- Bullet list of the meaningful changes. One bullet per logical change.
     AI reviewers: group by surface (api/cli/db/docs/tests). -->

-

## Acceptance criteria mirror

<!-- Mirror of the linked issue's `- [ ]` acceptance criteria, for the
     reviewer. -->

- [ ]

## Test plan

<!-- What was run locally: the
     commands (this repository has no CI; see AGENTS.md "Validation"). -->

-

## Changelog entry

<!-- Add one line under `## Unreleased` in `CHANGELOG.md` with one of these
     labels, OR apply the `changelog-skip` label to this PR for a no-impact
     change (e.g., comment typo). The PR title must start with `[patch]`,
     `[minor]`, or `[major]` matching the highest-tier label below.

       [BREAKING]  -> [major]   incompatible API, data, or operator change
       [FEATURE]   -> [minor]   new capability (additive)
       [FIX]       -> [patch]   bug fix or compatibility repair
       [INTERNAL]  -> [patch]   tests, CI, refactor, docs
       [SECURITY]  -> [patch]   vulnerability fix or hardening
-->

- [LABEL] one-line description matching the line added to CHANGELOG.md
