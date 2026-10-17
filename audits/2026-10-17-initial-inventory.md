# Initial cross-repository Rust parity audit — 10-17-2026

**State: IN PROGRESS / NOT DONE.** This is a private, resumable evidence checkpoint, **not** a completion receipt, verified parity matrix, or an assertion that every history source was searched. It covers authenticated default-branch tree inventories and selected source/CI/PR reads. Recorded in America/New_York. Keep this file in the PRIVATE RustyNuts repository; never copy raw private inventory into the public Toe-Tickling guidebook.

## Task and governing inputs

- Full owner goal: `RustyNuts/GOAL.md`, blob `546d66b16d3a29ad9d66973554382278a21b5397`, main commit `f04a929716b6707a63c02dcfebaf5e6384555eec`.
- Guidebook: `Toe-Tickling/AGENTS.md` blob `5407f0bcf6dd092033ba80399b02519c13c1a998`; generated `GUIDEBOOK.md` blob `45bdd5dce12eaf8cb74a22e0868a64852d85ed94`, v1.2.2 (10-16-2026); main commit `4f519c3ea1ed120d36aefea014fbf31bc0593304`. The documented intake sequence (GUIDEBOOK, README, RULEBOOK, SELF_CHECKS, EVOLUTION, ADOPTION, PROVENANCE, SCENARIOS, CONTRIBUTING) was retrieved; some registry and source module material has not been independently semantically reconciled line-by-line.
- Primary Rust references directly accessed: https://doc.rust-lang.org/stable/book/ch11-00-testing.html ; https://doc.rust-lang.org/cargo/guide/continuous-integration.html ; https://doc.rust-lang.org/releases.html . Rust release notes list 1.99.1 as released 10-15-2026. No claim that all task-specific Rust reference chapters were consulted.
- External actions in this checkpoint: GitHub READ operations, plus an isolated branch and this private audit file. No production edits, default-branch code edits, merge, deployment, disk operation, purchase, or credentials used.

## Exact accessible default-branch inventory

GitHub repository enumeration returned **14** repositories in one page (page_size 100), with no second page evidenced or needed for the current result count. Each corresponding recursive Git tree was returned without the API's truncation flag. This is **tree inventory, not full content/history inspection**.

| Repository | HEAD SHA (exact) | Tree files | Rust files | Initial classification / evidence gap |
| --- | --- | ---: | ---: | --- |
| NepetaMirror | `20b9dab1a3127ebfeeb9068376c49145047df80b` | 414 | 1 | Mirror integrity Rust tool; end-user use/asset equivalence not demonstrated |
| discord-plus | `e8bbb172315f45fe5f1099390fc4133db036310b` | 38 | 0 | Archived CSS/theme; review upstream scope before any migration |
| ClearVision-v6 | `1eac93750a6d8d1f35bae562201d49d3aa64bb99` | 148 | 0 | SCSS/theme; no unsupported blanket Rust rewrite |
| uYouPlus | `20e9461115a7bb87532b60fd90f3469a12bce62a` | 69 | 2 | Rust validation parts; iOS sign/install/launch not tested |
| fedora-pain | `8fd379b6feb623679c45c9279b03648011b7cfa0` | 8 | 1 | Rust docs/privacy guard; project not established as full app |
| Discord-Theme | `52f1f7d5522b95b3f79cdb7379137fa337ad3e6a` | 7 | 0 | CSS/theme; no evidenced Rust port requirement |
| tech-project | `e133bbaedff557b984bad684ab8b0be9ce9df64c` | 99 | 19 | Fedora Python-to-Rust operations partial; real host/rollback untested |
| chatgpt-projects-export | `8649569f808eac4b07d1d66a7681d34f65400c43` | 1,641 | 25 | Export/archive Rust tools partial; actual backup and restore unverified |
| money-project | `5194f42a8eb43ead29721b90ef6210cd72c9ec8d` | 23 | 2 | Fictional finance guard tests; real application parity unproven |
| car | `6b396d3612f6451a45df04282b6e40bf6c167f7d` | 131 | 5 | Dashboard Rust pieces; browser JS interactions still relevant |
| odysseus-local-audit | `9c0104bcaec469a06787b7bc8920937293954599` | 12 | 1 | Docs/privacy verification; real restore unverified |
| MRI-Drive-Maker | `58677cd30cc85c641ecb411328cd3fcf73e7805e` | 186 | 8 | Rust components and PowerShell production path; physical USB and boot parity unverified |
| Toe-Tickling | `4f519c3ea1ed120d36aefea014fbf31bc0593304` | 66 | 9 | Rust builder/auditor and 1.2.2 guide; model adoption/legacy parity unverified |
| RustyNuts | `f04a929716b6707a63c02dcfebaf5e6384555eec` | 3 | 0 | Goal and documentation, not a Rust port |

Notes: The counts are default-branch *file paths*, not lines or tests. The 1,641-file archive tree is a private repository and does not imply the original export is complete. Third-party/style-only projects require explicit scope classification rather than invented feature obligations. Scope needs reconciliation with forks, licenses, owner history and target runtime. All 14 default-branch commits were individually resolved from GitHub's commit endpoint.

## Source evidence and concurrent branches

- `MRI-Drive-Maker/README.md` at default branch documents the actual Windows `START-MRI-DRIVE-MAKER.cmd` launcher, destructive FAT32 USB preparation, configurable 1–30 parallel workers, independent source-file SHA-256 checks, watcher registration, virtual-disk tests, and the explicit warning that **READY does not establish MRI bootability**. Original upstream is JStone21/MRI-Creation, cited there at `aa7bdc528eb95952be3c95710e277025b3eea5be`. Source: https://github.com/Cucklord420/MRI-Drive-Maker/blob/main/README.md
- `chatgpt-projects-export/README.md` explicitly says its account backup and Odysseus migration are incomplete, with real restore unverified. Source: https://github.com/Cucklord420/chatgpt-projects-export/blob/main/README.md
- Prior scoped audit: https://github.com/Cucklord420/tech-project/issues/35 (10-16-2026). Its 13-repo enumeration preceded RustyNuts; treat its technical findings as leads, not this session's executed tests or globally proven parity.
- At observation time: **23 open MRI-Drive-Maker PRs, 12 open tech-project PRs, 5 open chatgpt-projects-export PRs, 5 open Toe-Tickling PRs, 4 open uYouPlus PRs, 6 open car PRs**. GitHub PR lists were retrieved; overlapping branches and unpublished agent work must not be overwritten. Recheck before integration. Example specific PRs: MRI #26 arrival tracker, MRI #27 existing-media receipt guard, Toe-Tickling #20 timeout regression. Their PR descriptions and diffs are NOT independent proof of correctness.
- Toe-Tickling issue #15 documents absence of enforceable main branch protection and the connector's lack of admin branch-ruleset write capability. This remains **NOT DONE / administrative access blocker** unless later API evidence proves otherwise. https://github.com/Cucklord420/Toe-Tickling/issues/15

## Representative incomplete traceability rows (not the complete denominator)

| ID | Source requirement / original evidence | Rust counterpart / target | Verification now | Status |
| --- | --- | --- | --- | --- |
| MRI-001 | Windows launcher and complete erase/copy/READY workflow, README | Production PowerShell plus partial Rust components | No physical launch or removable-device execution in this session | UNVERIFIED |
| MRI-002 | USB identity, explicit erase scope, no user-data loss, README and AGENTS | Existing safety implementation and PRs | Static PR/README inspection only; hardware and races untested | UNVERIFIED |
| MRI-003 | Folder/ISO/ZIP provenance, FAT32 and copy-byte/hash semantics | Rust manifest/release tools plus original source path | Default-branch manifest CI successful for that workflow only; no complete original-vs-Rust workflow parity | PARTIAL |
| MRI-004 | Watcher registration, ALREADY_READY, concurrency/cancellation | Original PowerShell + open Rust tracker PRs | No authenticated physical tests; no installation/first-run test | UNVERIFIED |
| TECH-001 | Fedora maintenance, diagnostics, rollback, self-hosted project docs | Python originals + Rust projection components | CI for offline Fedora tooling successful on recorded HEAD; no real privileged host test | PARTIAL |
| EXP-001 | Lossless account export and backup and successful Odysseus restore, README | Rust archive/verifier/wrapper | Synthetic CI success; original user archive and isolated restore unverified | PARTIAL |
| CAR-001 | Live browser dashboard parity with source and filters | Rust server-side tools + browser interface | Source CI observed at earlier revisions, browser interaction parity not executed | UNVERIFIED |
| UYOU-001 | Actual signed app working on supported iOS | Rust source validators alongside upstream iOS build code | Source validation CI observed; install and iOS device not tested | UNVERIFIED |
| GUIDE-001 | Policy 1.2.2 generated consistency and verification metadata, AGENTS | Rust CLI and independent Rust auditor | Main-head Rule book audit CI reports success, run 38917894076, but no local or model-behavior test | PARTIAL |
| GLOBAL-001 | Every real owner requirement across original GitHub history, issues/PRs/comments/releases/branches | Per-project feature and requirement matrix | Full source/issue/PR/comment/history traversal NOT performed | NOT DONE |
| GLOBAL-002 | End-to-end full parity for every applicable original-vs-Rust interface | Rust ports in all actually in-scope repos | No complete denominator, no three-method or three-cycle validation, no full installed-artifact tests | NOT DONE |

Do not convert any `PARTIAL` row to `PASS` based solely on source existence or one CI workflow. The table is deliberately incomplete; expand it with uniquely sourced rows and meaningful variants before calculating project completion.

## Observed workflow outcomes — NOT tests run by this session

For the following exact default HEADs, GitHub Actions listed a completed successful workflow: MRI manifest run `38857654527`; tech offline Fedora run `38857361910`; ChatGPT export Odysseus wrapper run `38858099003`; Toe-Tickling rule audit run `38917894076`; uYouPlus source validation run `38798251603`; NepetaMirror integrity run `38755430664`; money-project private tooling run `38755828461`; fedora-pain documentation run `38752521016`; odysseus-local-audit documentation run `38752536603`. This does not prove those repos' **entire** CI matrices, installability or Rust parity. The car dashboard workflow shown was on an earlier commit, not necessarily the current HEAD.

## Environment, tool-access, failure log

- Authenticated GitHub connector reads, repository listing, tree/commit URLs, file reads, PR reads, and isolated branch writes available.
- Local container: `rustc` was absent; `git ls-remote https://github.com/Cucklord420/Toe-Tickling.git HEAD` failed with `Could not resolve host: github.com`. Therefore no local `cargo fmt`, Clippy, compile, parity oracle execution, Windows installer launch, physical USB test, iOS app test, or actual restore was executed. Attempts: 1 local toolchain probe, 1 network/Git resolution probe, no repeated blind retries. Equivalent read-only evidence was obtained through the authorized GitHub connector; this cannot substitute for execution.
- No direct local worktree, dirty-state view, unpublished agent branch, production machine, USB hardware, signed iOS app, or approved private account archive bytes were available.
- No local 100-run test, fuzzing, mutation test, three clean validation cycles, branch merge or deployment took place. Do not claim them.

## Resumption protocol and next independently actionable work

1. Reload current RustyNuts GOAL and Toe-Tickling AGENTS/guide, diff their current revisions against the blobs above and recheck private ledger privacy.
2. Refresh **14+** accessible repo inventory, PR/CI heads, branch protection and agent changes. Do not assume the currently observed count stays fixed.
3. Enumerate and reconcile every repository's original-owner requirements from docs, GitHub issues/comments, PR reviews and releases/history. Preserve authority, supersession chronology and original sources in full private requirement rows, then deduce actual port scope.
4. Prioritize critical data/USB safety, user-data preservation and true runtime equivalence. Review current MRI PR branches without merging duplicate or incomplete work; run original and Rust in Windows CI using synthetic media, then separately on owner-approved disposable physical media. Never erase an unidentified USB.
5. Install pinned Rust toolchain in a supported authorized test environment; execute documented Cargo checks, separately mechanical/behavioral/adversarial tests, three clean post-final-edit cycles and real artifact installation. Record **exact** commit, commands, output/exit codes, seeds and run counts. Treat CI artifacts and all untouched requirements as pending.
6. Address Toe-Tickling branch-ruleset admin blocker through authorized account settings when capability exists; do not bypass. Any change to canonical rule sources must regenerate outputs and run the guide's Rust validators; avoid redundant policy prose.

**Completion gate:** none of the incomplete rows or repositories has been designated globally DONE here. Task status remains **NOT DONE — historical requirements and independently executed real-world parity are unverified; local Rust test runtime unavailable; some hardware/admin prerequisites inaccessible.** Reassess each limitation independently on the next actual execution, not by implying background activity.


## Verified subsequent work: Windows MRI junction regression (10-17-2026)

- Selected specific gap after inspecting original `MRI.Batch.psm1` (`Get-MRIManifest`, `Assert-MRIContentsSafe`), draft PR #27 Rust source and its existing tests: no real Windows junction fixture was present in that Rust manifest regression suite. Original intentionally rejects reparse points; this is a concrete case missing from the new Rust test suite, not proof of an exploitable production defect.
- Created isolated MRI branch `audit/windows-junction-manifest-regression-20261017` from PR #27 head `a6f430239f659fa7757a9a9b666a070e75c02484`. Added a test-only Windows fixture in **verified real path** `rust/mri-manifest/src/tests.rs`: make an NTFS directory junction to disposable outside data; check Windows reparse metadata; test fail-closed linked-root/child and read-only receipt preflight; verify outside data unchanged. No actual USB, production code or PowerShell path modified.
- First test commit `62e6288c823213a187de65033a1cd644af90bcd0`, blob `cddfc288a4d4905cd353b10d526708867a942d97`; opened draft stacked [MRI PR #35](https://github.com/Cucklord420/MRI-Drive-Maker/pull/35), targeting `migration/rust-contents-safe-receipt-20261016`, not main. Verified PR changed only `rust/mri-manifest/src/tests.rs`.
- GitHub Actions Windows manifest job `117316612963` on the first commit compiled the test and ran 9 Rust tests: 8 passed, **1 failed** before reaching assertions because `cmd.exe` rejected the single prequoted `mklink /J` command string (`The filename, directory name, or volume label syntax is incorrect.`). No formatting, Clippy, or differential test ran after that failure. Evidence: [workflow run 39005363246](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39005363246).
- Corrected test harness command quoting by passing `mklink`, `/J`, and two path operands as distinct child-process arguments, commit `6d336a64da54511a8a209a6856ef40c1c957367e`; confirmed exact readback blob `99bce6f25b401370006d41bd6de2c84ac5b82a25`. This is a documented recovery from an actual failure, not a production code change.
- Post-correction Windows CI was observed **in progress**: run [39005474678](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39005474678) (manifest), with other workflows queued/in progress. Do not turn this into PASS without checking results on final exact commit. No local Rust or native Windows execution available, no three clean validation cycles, no physical USB/bootability or exhaustive original-vs-Rust parity. **STATUS: OPEN/UNVERIFIED.**


### Evidence update — final MRI test-only revision (10-17-2026)

- Final tested branch commit `05e2781f38bc0ad49a143b130d5cafe308d3d261`, readback blob `7f92a2af85c23ca8469729021ebc03f8ccfb2932`, corrects only rustfmt on the verified test. PR #35 remains draft and stacked on #27; no production rewrite.
- Independent GitHub-hosted Windows CI manifests on that exact commit: [run 39005548914](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39005548914) and [run 39005552816, attempt 1](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39005552816), both **complete success**. Each passed actual Rust unit tests including Windows junction fixture, rustfmt, strict Clippy, binary compilation, and three distinct original-PowerShell comparison suites (400 manifest + 600 matching + 780 contents-safe cases). These are 2 completed validation cycles, not 3.
- A third deliberate Windows manifest job run was accepted by the GitHub Actions API on workflow run `39005552816`, attempt 2, job `117317734694`. At the latest review it was in progress; its eventual outcome must be checked before raising the run count. On final SHA the separate Rust path-safety, USB-selection, release-package, and PowerShell static-analysis workflow outcomes had completed successfully; the PowerShell startup/virtual-disk workflow was still running.
- Initial failure logs and corrected source remain in the earlier evidence section. This demonstrates recovery from test harness quoting and formatting failures; it does **not** demonstrate physical removable USB safety/bootability, actual 30-drive workflow, user-proprietary media, or all historical requirements. No device or user data was touched. **MRI overall: NOT DONE; regression PR: verification pending final workflow/third cycle.**


### Verified final-run closeout for the isolated junction regression (10-17-2026)

- **Final exact SHA:** `05e2781f38bc0ad49a143b130d5cafe308d3d261`; unchanged MRI PR #35 branch on readback. Draft PR remained stacked on MRI PR #27.
- **Three complete clean Windows manifest/parity validation cycles:** [39005548914](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39005548914) attempt 1, [39005552816](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39005552816) attempt 1, and [39005552816](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39005552816) attempt 2, job `117317734694`: all `completed/success`. Each completed Rust unit cases (including actual Windows junction creation and rejection), format check, strict Clippy, compilation, 400 original manifest differential cases, 600 final manifest matching cases, and 780 read-only receipt-safety differential cases. These are three **runs** of the same fixture suites, not independent new scenario counts. Earlier failed revisions stay failed in historical record.
- **All seven applicable Actions runs on that final SHA:** completed success, including PowerShell startup/safety on owned VHDs, Rust USB selection, path safety, release packaging and Python byte parity, PowerShell static analysis, and two manifest push/PR runs; the separately rerun job also succeeded. No physical removable USB or real MRI boot tests performed.
- Finding `MRI-JUNCTION-REGRESSION-001`: missing explicit Windows junction safety regression in pending receipt port. **TEST COVERAGE FIX VERIFIED** by final-sha GitHub Windows CI and original-source review, **NOT evidence of any production exploit or full migration parity**. RustyNuts global completion and MRI device/workflow parity are still NOT DONE.
