# Superpowers workflow companion for RustyNuts

**Scope:** This is an execution-process companion to [GOAL.md](../GOAL.md), not a replacement for the owner's current [Toe-Tickling guidebook](https://github.com/Cucklord420/Toe-Tickling), a new global policy, a completed Rust port, or authorization to change other repositories. It applies only where relevant Superpowers skills are actually available to the current agent.

## Activation and instruction authority

1. Read the full current GOAL.md, then current Toe-Tickling AGENTS.md and its complete required intake, followed by the target repository's local/nested instructions, current owner directions, and active work. Record exact source revisions and coverage in an authorized private audit/checkpoint.
2. Discover which Superpowers skills the **current runtime** exposes. A `@Superpowers` invocation or a link in this repository does not install those skills in Codex, GitHub Actions, another agent, or a persistent runner. Do not report a skill as used without actually reading/invoking it.
3. Follow platform requirements, the user's current authorization, and applicable canonical/repository constraints. Skills supply a method, never permission to touch secrets, destructive devices, production services, releases, or other repositories. Report genuine process conflicts rather than silently bypassing a higher-priority rule.
4. Keep any real private audit receipts, conversations, credentials, and user data outside this public repository. Commit only sanitized instructions, synthetic tests, and evidence links that are suitable for publication.

## Map Superpowers to the existing RustyNuts gates

| Stage | Relevant Superpowers skill when available | Required RustyNuts evidence / decision |
| --- | --- | --- |
| Intake and design | `using-superpowers`, `brainstorming` | Recover user intent, affected historical requirements, source version and original behavior before suggesting scope. Classify a feasibility spike, bounded repair, or architectural change. A proposed design is not an accepted owner requirement. Observe the skill's actual design/approval gates; continue independent work when one path awaits a decision. |
| Implementation planning | `writing-plans`, `executing-plans` or `subagent-driven-development` | For an approved multi-step change, define affected files, original/Rust oracles, negative cases, supported targets, expected outputs, exact test commands, rollback, and completion evidence. Record the plan/ledger in a permitted location. Never claim a background executor is active without a real runner. |
| Isolation and concurrency | `using-git-worktrees` | Prefer an actual isolated worktree when supported, otherwise a fresh GitHub branch. Recheck current refs, open PRs and overlapping work; preserve others' changes. Do not force-push or merge a shared branch merely to finish a task. |
| Code and bugfix cycle | `test-driven-development`, `systematic-debugging` | Reproduce first; add a meaningful failing regression before production changes when possible; verify RED then minimal GREEN, refactor, rerun focused and full suites. Tests for new executable behavior must honor the Rust-only rule. Diagnose root causes rather than relaxing tests. |
| Independent review | `requesting-code-review`, `receiving-code-review` | Review the diff against requirement IDs, privacy, safety, original-vs-Rust semantics, target platforms and regression evidence. Fresh independent review when supported; otherwise label author self-review as weaker, not independent. Resolve critical/important findings with verified tests. |
| Acceptance and delivery | `verification-before-completion`, `finishing-a-development-branch` | Run and read final-revision mechanical, behavioral and adversarial checks; where applicable verify actual installed/packaged entrypoints, hosted CI and artifact hashes. Mark untested real-world gates UNVERIFIED/BLOCKED. A PR is not a merge, deployment, release or global DONE state. |

## Per-change procedure

1. **Intake:** Capture the target `owner/repo`, precise base/ref, permission scope, relevant source/original and prior requirement citations. Check open issues/PRs for duplicates. If the repository only contains documentation (as RustyNuts currently does), do **not** pretend it provides a runnable Cargo project or runtime tests.
2. **Design:** Use the applicable brainstorming path. For a feasibility spike, obtain agreement on the question/probe and discard throwaway output; for bounded changes, get approval of the in-chat design; for architectural changes, obtain review of the specification, then the implementation plan and execution choice. When the stage requires approval, do not treat unrelated previous approval as a substitute. While awaiting authorization, proceed only with independent read-only or already-authorized work.
3. **Plan and isolate:** State acceptance criteria and required test oracles before editing. Prefer one testable change per isolated branch/PR; avoid duplicate or conflicting changes under another active PR. Obtain fresh source and guidebook revisions before writing.
4. **Test and implement:** For real source changes, create an independently meaningful failing test where practical, confirm its expected failure, implement the smallest behavior-preserving Rust change, run focused tests and the full existing suite. Compare original and Rust behavior **and side effects** across normal, invalid, edge and failure fixtures. Documentation-only changes require review of claims, relative links, scope and remote readback; they do not invent artificial Rust test results.
5. **Verify:** Apply GOAL.md's mandatory mechanical, behavioral and adversarial passes, its repeated clean-state checks where relevant, and actual hardware/OS/signing/device tests where authorized and available. Don't substitute mock checks, unrelated CI or unmerged code for production parity. Record commands, exit status, tested commit, environment, failure details, and exact blocks.
6. **Review and deliver:** Re-read the changed files and full diff, check for personal data and conflicts, obtain independent review when supported, then re-verify after modifications. Leave integration decisions to the authorized owner: no merge, release, deployment, data erase or live mutation on the strength of a successful checklist alone.
7. **Checkpoint:** Maintain the existing requirements matrix and private evidence ledger. Classify each requirement PASS only with matching final-revision evidence; otherwise use PARTIAL, UNVERIFIED, BLOCKED, or NOT DONE. Resume from verified checkpoints and continue unrelated authorized work rather than claiming global completion.

## Platform limitations

- **Skill availability is not portable.** A repo instruction can request discovery/use of installed skills, but cannot make an agent load a ChatGPT plugin, create subagents, start a scheduler or run unattended.
- **No Git worktree access?** Use a connector-created isolated GitHub branch with reviewable commits and a PR, recording that local execution and test tooling were unavailable.
- **No test environment, hardware, credentials, approval or source oracle?** Verify what is possible without crossing that boundary, then mark the specific remaining acceptance tests blocked. Do not claim parity.
- **No independent reviewer?** Perform a separate author self-review and identify its reduced independence; do not label it an independent review.
- **Existing overlapping PR?** Compare and coordinate first. Never overwrite another agent's branch simply to claim the workflow was applied.

## Adoption checks

These checks establish whether the *process* was applied, not whether RustyNuts's global goal is complete:

- [ ] Exact current GOAL.md, guidebook and target-repository requirements were retrieved; versions and intake gaps recorded.
- [ ] Available Superpowers skills were actually invoked (or their absence explicitly recorded).
- [ ] Design scope, approvals, work isolation, existing PR overlap and test oracles were handled.
- [ ] Final diff and remote readback were verified, with actual test commands and blockers disclosed.
- [ ] Matrix/ledger retained per-requirement results, with real end-to-end parity still separately gated.

**Status of this document:** Guidance only. Adding it does not execute Rust migrations, validate 14 repositories, install skills, or turn any unresolved global parity item into PASS.
