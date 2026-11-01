# Changelog

This file is the operator-facing release ledger. Every pull request adds one
line under `## Unreleased` with one of the allowed section labels, or
applies the `changelog-skip` label for a purely no-impact change.

Allowed entry labels:

- `[BREAKING]` - incompatible API, data, deployment, or operator change.
- `[FEATURE]` - new user-visible or operator-visible capability.
- `[FIX]` - bug fix or compatibility repair.
- `[INTERNAL]` - tests, CI, docs, refactors, generated artifacts, or process.
- `[SECURITY]` - vulnerability fix, security control, or hardening change.

PR title prefix matches the highest-tier label added:
`[BREAKING]` -> `[major]`, `[FEATURE]` -> `[minor]`, others -> `[patch]`.

## Unreleased

### [BREAKING]

- None.

### [FEATURE]

- None.

### [FIX]

- Docs: the README, `docs/USAGE.md`, `docs/INSTALL.md` and `docs/CONTRIBUTING.md` now quote only triggers and expansions that exist in the collection (10 of the 16 documented triggers did not exist), and retired ORC wording is removed from `SECURITY.md`, the pull request template and `internal/operator-notes/README.md` (#2).

### [INTERNAL]

- Refresh the generated fleet core; preserve repository-specific instructions.

- Add `AGENTS.md` (fleet agent-file standard) and a `CLAUDE.md` that imports it.

### [SECURITY]

- None.
