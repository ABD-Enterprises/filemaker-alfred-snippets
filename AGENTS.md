# Agent instructions: filemaker-alfred-snippets

<!-- fleet-core:begin (generated: edit the fleet source, not this block) -->
## Fleet core

Applies to new work after a repository adopts this baseline; do not retroactively invalidate in-flight work under its existing contract. It is generated from one source; repository-specific rules go outside the markers.

### Evidence
- Read live state before stating it: fetch the remote, read the default branch, run the command. A number or an "X is missing" taken from a doc or a stale checkout is a claim to verify. A figure in a doc carries its date and how it was read.
- Find the root cause before proposing a remedy. For an unreachable or hung host, check its network interface and the previous boot's log before blaming memory.
- Give one account of a fact. If two places disagree, fix or flag one.
- Say plainly what you did not verify.

### Changes
- One bounded task per change request. Stay in scope: no drive-by edits and no agent scratch files committed.
- Agent-authored code changes follow SureForge: one bounded work contract, supervised run and validation, independent review, then delivery. The operator may invoke a headless coder adapter; the interactive editor need not be the process coder. An unsupported route remains blocked; do not silently bypass it.
- An exception requires an explicit dated repository-specific rule outside this block naming its scope, reason, validation and delivery route. Limit exceptions to non-code work, read-only mirrors or archived repositories, and bounded pilot restrictions. An exception never relaxes review, protection or an explicit run contract; preserve stricter rules, including human-start requirements.
- Run the repository's validation (named below) before pushing. Inside a supervised run, its contract and delivery process govern commits and publication. For a permitted exception, commit, push a branch (never the default branch) and open the change request yourself within the limits below.
- Generated-policy checks establish instruction consistency; they do not establish runtime enforcement or OS confinement.
- A change request merges when a fresh-context review of the exact head has no unresolved P0 or P1 findings and every required check is green. A new commit needs a new review; a clean automatic merge of the base branch keeps the review.
- At most three open non-draft change requests per repository. While the fleet backlog check reports a backlog, finish and land existing work and start nothing new.
- Fix a finding that takes minutes in the current change; fold the rest into an existing tracking issue. A session closes at least as many issues as it opens on its own initiative; tickets the owner asks for in chat are separate.

### Safety
- Never print, log or commit tokens, passwords or keys. Use the credential helper the repository names.
- One writer per checkout: separate worktrees for separate writers. Do not force-push, rebase or delete a branch another session may own.
- Private repositories run CI on self-hosted runners only. A job that must not share a host (for example signing) runs on a dedicated self-hosted runner group, never on a GitHub-hosted runner without the owner's approval.
- Ask the owner only for a step no agent can do or for a spend or legal commitment; decide and record everything else.

### Layout
- AGENTS.md is the canonical agent file; where a CLAUDE.md exists it only imports it. Keep this file under 200 lines.
- Name this repository's validation command, merge rule and changelog rule outside the markers. Rules kept outside the repository are not visible here: if a task seems to need one, ask rather than guess.
- Rules any adopter needs live in SureForge and in this core; rules that name a machine, account or model live in the operator's own configuration repository, from which each tool's settings are meant to be generated so every agent on every machine follows the same rules.
- Shared skills are installed per machine from the fleet skills hub. Name the ones this repository expects below.

### Forge: GitHub
- Prefer REST (`gh api repos/OWNER/REPO/...`) to GraphQL for single reads: the rate-limit pools are shared by every session on the account.
- Required checks and review rules are branch protection or rulesets; read them with `gh api`. Review-thread resolution needs GraphQL.
<!-- fleet-core:end -->

## Repository-specific

- Public repository: the files are world-readable, and so is anything an agent writes into the repository, including issues, pull requests and comments. Keep customer, tenant and internal-host names, private paths and personal data out of all of it. A scan of the tracked files found no home paths or user names (2026-10-21).
- What it is: Alfred text-expansion snippets for Claris FileMaker calculations (`;fm` triggers). There is no application code.
- Layout: `data/FileMaker_Functions_Alfred_Snippets.csv` is the source (columns `Name,Keyword,Snippet,Category`; 360 rows, some snippets span several quoted lines); `FileMaker_Functions.alfredsnippets` is the generated Alfred bundle (a zip of one JSON file per snippet); `docs/` holds INSTALL, USAGE and CONTRIBUTING; `README.md` and `SECURITY.md` are at the root.
- Validation: none exists, and there is no CI. For a change to the CSV, check by hand that every keyword is unique, starts with `;fm` and is lowercase (the rules in `docs/CONTRIBUTING.md`). This one-liner does it from the repository root: `python3 -c "import csv;r=list(csv.DictReader(open('data/FileMaker_Functions_Alfred_Snippets.csv')));k=[x['Keyword'] for x in r];assert len(k)==len(set(k)) and all(x.startswith(';fm') and x==x.lower() for x in k);print(len(k),'ok')"`.
- Merge: the fleet core's merge rule applies, and with no CI the independent review of the exact head is the whole gate. GitHub enforces only the organization ruleset "ABD default branch baseline" (rules: no branch deletion, no non-fast-forward push); the default branch has no required status checks or required reviews (read 2026-10-21).
- Changelog: `CHANGELOG.md` at the root is the ledger the pull request template points at. Add one line under `## Unreleased`, in the matching section (`### [FEATURE]`, `### [FIX]`, `### [INTERNAL]` and so on), replacing the `- None.` line if it is the first entry. `docs/CHANGELOG.md` is an older, separate file with one `v1.0.0` entry; leave it alone.
- Bundle and source: contributors change only the CSV; a maintainer regenerates the bundle by importing the CSV into an Alfred collection and exporting it (`docs/CONTRIBUTING.md`), which needs Alfred and cannot be done here. As of 2026-10-21 the bundle matches the CSV exactly (name, keyword and text of all 360 snippets, compared by script). If you change the CSV, say in the pull request that the bundle is now out of date; do not hand-edit the zip.
- Documented examples can be wrong: `README.md` and `docs/INSTALL.md` say `;fmlet` expands to `Let ( [] ; )`, and `docs/USAGE.md` shows another form, while the CSV expands it to a multi-line `Let ( [ var = value ] ; result )`. The CSV is the truth; check any expansion you quote against it.

### Safety

- Never import or open the bundle on the owner's Mac. Double-clicking or running `open` on `FileMaker_Functions.alfredsnippets` imports 360 snippets into the real Alfred setup, where `;fm` triggers expand in any app and may collide with keywords the owner already has. Installation is the owner's step (`docs/INSTALL.md`). To inspect the bundle, unzip a copy into a temporary directory (`unzip -q` into an empty folder) and read the JSON; do not run anything from it.
- Snippet text is typed into the owner's FileMaker calculations and other editors. Keep snippets to plain FileMaker syntax; do not add Alfred dynamic placeholders (such as clipboard, date or cursor tokens) or any text that runs on expansion. None exist today (checked across all 360 snippets).
- Do not add anything personal to a snippet or to the docs: no real field, table, file, customer or server names, and no credentials. Use generic placeholders such as `table`, `field`, `id`.
- `SECURITY.md`, `.github/PULL_REQUEST_TEMPLATE.md` and `internal/operator-notes/README.md` still carry wording from the retired ORC tooling (validation isolation, Planner runs). They are not agent instructions; do not follow them. Do not store secrets or machine-local paths in `internal/operator-notes/`.
- The Alfred setting named in `docs/INSTALL.md` ("Automatically expand snippets by keyword") was not checked against a current Alfred; treat the menu path as unverified.

### Skills
- This repository expects no hub skills.
