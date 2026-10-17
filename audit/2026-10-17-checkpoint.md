# RustyNuts evidence checkpoint — 10-17-2026

**Outcome: IN PROGRESS / NOT DONE.** This is a private, resumable *partial inventory and evidence ledger*, not a completed historical requirements matrix or proof of end-to-end Rust parity. No release, production installation, physical hardware test, global parity pass or full guidebook adoption is claimed.

## Governing revisions and environment

- Owner goal: `Cucklord420/RustyNuts` default `main` at `f04a929716b6707a63c02dcfebaf5e6384555eec`; complete `GOAL.md` fetched, blob `546d66b16d3a29ad9d66973554382278a21b5397`. URL: https://github.com/Cucklord420/RustyNuts/blob/main/GOAL.md
- Guide: `Cucklord420/Toe-Tickling` `main` at `4f519c3ea1ed120d36aefea014fbf31bc0593304`, policy version 1.2.2. `AGENTS.md` read, blob `5407f0bcf6dd092033ba80399b02519c13c1a998`. Full `GUIDEBOOK.md` retrieved but tool output was truncated; **complete semantic intake remains UNVERIFIED**, not passed. Retrieved README, RULEBOOK, SELF_CHECKS, EVOLUTION, ADOPTION, PROVENANCE, SCENARIOS, CONTRIBUTING, policy.json and policy/rules.json (large generated rule sources were partially displayed).
- GitHub identity: authenticated `Cucklord420`. Owner repository listing requested with page size 100; returned 14. All 14 default-branch recursive tree API results reported `truncated=false`, but tree enumeration is not source-code/historical review.
- Local terminal: `git 2.47.3`; `rustc` and `cargo` not installed; direct `git ls-remote` failed DNS resolution for github.com. GitHub connector and GitHub Actions were available. GitHub Actions success is remote evidence, not local/hardware validation.
- Only seven project READMEs and selected source/docs/PR/CI files were semantically reviewed; no claim of exhaustive review. Issues collection was fetched for all repositories (all single-page results below 100), but most issue bodies/comments and PR histories were not read.
- This ledger is stored only in the PRIVATE goal repository. Never copy private audit inventory into public Toe-Tickling.

## Repository discovery (not completion)

Default-branch commits below were resolved directly through GitHub's ref API. A tree count is not a test or audit.

| Repository | Ref / SHA | Default-tree files | Initial disposition |
| --- | --- | ---: | --- |
| NepetaMirror | master `20b9dab1a3127ebfeeb9068376c49145047df80b` | 414 | Rust verifier present; source/history parity NOT VERIFIED |
| discord-plus | master `e8bbb172315f45fe5f1099390fc4133db036310b` | 38 | Archived; in-scope maintenance authorization undecided |
| ClearVision-v6 | master `1eac93750a6d8d1f35bae562201d49d3aa64bb99` | 148 | Existing theme; scope/ownership/historical review pending |
| uYouPlus | main `20e9461115a7bb87532b60fd90f3469a12bce62a` | 69 | Rust input-check port; focused CI repair under draft PR #8 |
| fedora-pain | main `8fd379b6feb623679c45c9279b03648011b7cfa0` | 8 | Rust docs-safety verifier; full review pending |
| Discord-Theme | main `52f1f7d5522b95b3f79cdb7379137fa337ad3e6a` | 7 | Scope and original parity pending |
| tech-project | main `e133bbaedff557b984bad684ab8b0be9ce9df64c` | 99 | Fedora diagnostics Rust port; open PRs/issues; historical review pending |

| Repository | Ref / SHA | Default-tree files | Initial disposition |
| --- | --- | ---: | --- |
| chatgpt-projects-export | main `8649569f808eac4b07d1d66a7681d34f65400c43` | 1641 | Rust backup/verifier ports; actual complete backup/restore NOT VERIFIED |
| money-project | main `5194f42a8eb43ead29721b90ef6210cd72c9ec8d` | 23 | Rust finance fixtures/guard; interactive product not implemented per README |
| car | main `6b396d3612f6451a45df04282b6e40bf6c167f7d` | 131 | Rust dashboard helpers; deployed Pages not verified per README |
| odysseus-local-audit | main `9c0104bcaec469a06787b7bc8920937293954599` | 12 | Rust docs-safety checker; scope/historical review pending |
| MRI-Drive-Maker | main `58677cd30cc85c641ecb411328cd3fcf73e7805e` | 186 | Existing PowerShell tool and Rust helper ports; physical USB boot parity NOT VERIFIED |
| Toe-Tickling | main `4f519c3ea1ed120d36aefea014fbf31bc0593304` | 66 | Governing guide, Rust CLI; adoption/evolution audits open |
| RustyNuts | main `f04a929716b6707a63c02dcfebaf5e6384555eec` | 3 | Goal specification and this separate checkpoint branch |

Comparison criteria: discovered repository trees and retrieved source evidence, not percentage of feature parity.

## Seed traceability / unresolved acceptance rows

| ID | Source and expected behavior | Evidence / implementation | Status |
| --- | --- | --- | --- |
| GLOBAL-001 | All actual owner requirements and every applicable feature must be enumerated, linked to original version and independently tested, per `RustyNuts/GOAL.md` §2A, §6A and §12. | Only partial README/issues/PR coverage; cannot establish denominator. | **NOT DONE — UNKNOWN** |
| GLOBAL-002 | Every in-scope Rust port must pass mechanical, behavioral/differential, adversarial, three clean final-revision cycles and real shipped artifact tests, per GOAL §4–§7. | No complete cross-repository acceptance matrix, installations or physical/service tests. | **NOT DONE** |
| UYOU-001 | Rust input-check CI must resolve dependencies and run regressions, using `uYouPlus/rust/build-inputs/Cargo.toml`. | Existing run https://github.com/Cucklord420/uYouPlus/actions/runs/38858741097 failed to resolve yanked `zip ^0.6.6` with no Cargo.lock. Isolated draft https://github.com/Cucklord420/uYouPlus/pull/8 at `c91773ef831db08ce6ea8fe5b21956cbe5abdf11` changes required minimum to `0.6.5`. CI https://github.com/Cucklord420/uYouPlus/actions/runs/39005006392: first clean run succeeded (38 Python, 7 Rust tests); second rerun succeeded; third rerun requested and initially pending. | **REPAIR PROPOSED / partial CI PASS; not merged** |
| UYOU-002 | IPA URL/path parsing and archive safety Rust/original-Python observable parity, plus actual packaging and iOS workflow. | `rust/build-inputs/src/main.rs` and `src/bin/ipa.rs` inspected; synthetic original-language tests in CI, real IPA install and broader matrix not completed. | **NOT VERIFIED** |
| MRI-001 | Real MRI USB feature parity, destructive target identity, actual usable/bootable device workflows. | `MRI-Drive-Maker/README.md` explicitly does not claim physical MRI bootability or original BDE equivalence. Multiple unmerged Rust port PRs. | **NOT VERIFIED — real media required for final gate** |
| ARCHIVE-001 | Full account archive, native Odysseus backup, actual verified restore and parity. | `chatgpt-projects-export/README.md` explicitly says not a complete account backup or Odysseus migration and real restore unverified. | **NOT DONE** |
| MONEY-001 | Functioning auditable personal finance tracker with reconciled transfers, debts, budgets and interface. | `money-project/README.md` says interactive application not yet implemented; do not place private finance records in Git. | **NOT DONE** |
| CAR-001 | Manually deployable, safe public dashboard and verified real endpoint. | `car/README.md` says GitHub Pages has not successfully published and deployment remains unverified. | **NOT VERIFIED** |
| GUIDE-001 | Toe-Tickling rule and scenario intake, honest checker, independent model adoption, no private leakage. | Guide 1.2.2 retrieved in part; `docs/SCENARIOS.md` covers S01–S28; several overlapping open PRs and issue #15. Full intake and live adoption proof not complete. | **NOT VERIFIED** |

## Existing parallel work — do not overwrite

- MRI-Drive-Maker had 23 open PRs when sampled, including many distinct Rust policy ports.
- tech-project had 12 open PRs; Toe-Tickling had five, including dependent base branches PR #19 and #20; uYouPlus had four pre-existing PRs.
- uYouPlus draft PR #8 is separate from those branches. Do not merge it or alter another worker's branch without resolving CI/base freshness/conflicts and all gates.
- tech-project open issue #35 records additional Rust audit work. Toe-Tickling issue #15 requests branch-protection/required CI.

## Evidence classification and restart procedure

- **DISCOVERED:** all 14 repository references; complete default-branch file-path trees as returned by API.
- **READ:** authoritative full GOAL.md, guide AGENTS.md, seven selected READMEs, source for uYouPlus input Rust and manifest, selected guide docs, selected PR lists/CI logs.
- **EXECUTED remotely:** GitHub Actions uYouPlus draft PR #8; baseline and two successful runs, with third rerun pending at this checkpoint. Confirm exact attempt records again before updating PASS.
- **UNVERIFIED:** exhaustive guide intake, all historical issue/PR/comments/branch provenance, full owned-project feature matrix, cross-repo integrations, full local Rust toolchain checks, physical USB, actual Odysseus restore, Pages deployment, final release artifacts, three different verification methods for complete products.
- **NO FAKE SUCCESS:** a green PR CI does not prove whole-project parity.

At resume: reread GOAL.md and Toe-Tickling AGENTS/entire reading sequence at newly resolved commits; refresh accessible repo list/head and PRs. Fetch uYouPlus PR #8 final head/CI attempts; inspect any failures and compare clean-run counts. Recover historical requirements repo-by-repo (owner-origin vs proposals), build detailed matrix with each original oracle/revision and actual test evidence. Do not misclassify missing code, lack of hardware, third-party forks or test-coverage gaps as PASS. For unsafe/hardware projects, require disposable media and physical verification before production claims.

Sources (actual repositories and official Cargo semantics): https://github.com/Cucklord420/RustyNuts/blob/main/GOAL.md ; https://github.com/Cucklord420/Toe-Tickling ; https://doc.rust-lang.org/cargo/commands/cargo-yank.html
