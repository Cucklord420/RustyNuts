# RustyNuts audit checkpoint

**Status:** NOT DONE / PARTIAL. This ledger records observed facts from the 10-17-2026 America/New_York run. It is not evidence of global requirement coverage, full port parity, shipping or active background execution.

## Authority and guidebook receipts

- Governing source: `GOAL.md` on RustyNuts main, Git blob SHA `546d66b16d3a29ad9d66973554382278a21b5397`, fetched and read in full.
- Guidebook: Toe-Tickling `AGENTS.md` blob `5407f0bcf6dd092033ba80399b02519c13c1a998`; `GUIDEBOOK.md` v1.2.2 blob `45bdd5dce12eaf8cb74a22e0868a64852d85ed94`. Read integrated guide in bounded slices, and read README, RULEBOOK sections in guide, SELF_CHECKS, EVOLUTION, ADOPTION, PROVENANCE, SCENARIOS, CONTRIBUTING and policy source order. Canonical typed register `policy/rules.json` was fetched as a whole but not exhaustively semantically reviewed in source form.
- Rules used: AUTH-002, ENG-001..020, EVO-021..028, AUD-001..020, PLAY-006..010, and typed AUTH-01, EVID-04, EXEC-01..08, SAFE-01..06, ENG-01, ENG-07, AUD-01..08 as applicable.
- Official documents consulted: Rust Book testing chapter (https://doc.rust-lang.org/book/ch11-00-testing.html); Cargo yank semantics (https://doc.rust-lang.org/cargo/commands/cargo-yank.html); source of zip v9.0.4 at https://github.com/zip-rs/zip2/tree/v9.0.4. ZIP 9.0.4 declares rust-version 1.88; the uYouPlus project has no tracked rust-toolchain or Cargo.lock at the inspected default branch.
- Environment: GitHub connector supports authenticated reads and branch/file/PR writes. The isolated local container has no `cargo`/`rustc`, and GitHub.com DNS cannot be resolved. No native local build, install, real IPA launch, hardware or cross-repository full tests ran in this run.

## Repository inventory: authorized owner account (14 discovered, all default Git trees indexed, none truncated)

Each line is a default-branch HEAD observed in this run, **not** an exhaustive file or history review. A CI green result on another ref does not validate these heads.

| Repository | Default HEAD observed | Initial scope/evidence |
| --- | --- | --- |
| NepetaMirror | `20b9dab1a3127ebfeeb9068376c49145047df80b` | Public mirror; tree inventoried; original/archive/history/runtime unverified |
| discord-plus | `e8bbb172315f45fe5f1099390fc4133db036310b` | Archived inherited CSS fork; no rewrite authorized by inventory alone |
| ClearVision-v6 | `1eac93750a6d8d1f35bae562201d49d3aa64bb99` | Inherited SCSS fork; relevant scope requires further review |
| uYouPlus | `20e9461115a7bb87532b60fd90f3469a12bce62a` | Inherited iOS project, Rust input/IPA validators, confirmed dependency blocker; see below |
| fedora-pain | `8fd379b6feb623679c45c9279b03648011b7cfa0` | Private Rust docs-safety utility; runtime unverified |
| Discord-Theme | `52f1f7d5522b95b3f79cdb7379137fa337ad3e6a` | Public CSS theme; runtime unverified |
| tech-project | `e133bbaedff557b984bad684ab8b0be9ce9df64c` | Private Rust diagnostics and inherited scripts; paired real workflows unverified |
| chatgpt-projects-export | `8649569f808eac4b07d1d66a7681d34f65400c43` | Private archive, large historical context; not comprehensively read or rebuilt |
| money-project | `5194f42a8eb43ead29721b90ef6210cd72c9ec8d` | Private Rust finance fixtures and sensitive-file guard; app parity unverified |
| car | `6b396d3612f6451a45df04282b6e40bf6c167f7d` | Private JS frontend plus Rust dashboard/site audit; browser/end-to-end unverified |
| odysseus-local-audit | `9c0104bcaec469a06787b7bc8920937293954599` | Private Rust docs-safety utility; real restore unverified |
| MRI-Drive-Maker | `58677cd30cc85c641ecb411328cd3fcf73e7805e` | Public PowerShell original + multiple partial Rust modules; physical USB and real Windows parity unverified |
| Toe-Tickling | `4f519c3ea1ed120d36aefea014fbf31bc0593304` | Public Rust guidebook CLI; policy v1.2.2 read, compiler/adoption checks not locally executed |
| RustyNuts | `e07f045c5159d790c812eae4e8c8df0542eb3607` | Private specification and this checkpoint; not an executable port |

## Initial traceability (INCOMPLETE — no row implicitly PASS)

| ID | Requirement / oracle | Implementation / evidence | State |
| --- | --- | --- | --- |
| UYOU-001 | Rust input validation accepts/rejects actual original Python CLI cases | `uYouPlus/scripts/build_checks.py`; `rust/build-inputs/src/main.rs` has actual Python-command differential tests; existing CI step blocked by ZIP resolver before these Rust tests | UNTESTED at final patch |
| UYOU-002 | Rust IPA security verifier preserves original Python behavior and rejects unsafe archives | `rust/build-inputs/src/bin/ipa.rs`, actual ZIP version upgrade in draft PR #10; tests exist but were not executed on patch | UNTESTED at final patch |
| UYOU-003 | ZIP dependencies must resolve in clean GitHub Actions runner | CI run https://github.com/Cucklord420/uYouPlus/actions/runs/38858741097 failed at Rust step: `zip = "^0.6.6"`, yanked; proposed minimal correction uses zip 9.0.4 | FAIL on prior PR #4; PR #10 ZIP9 compiled but fixture tests FAILED; PR #9 CI PASSED on its separate revision |
| UYOU-004 | Actual complete Theos/iOS IPA build, install and launch | Original Makefile, scripts and workflow inspected, physical launch unavailable | BLOCKED/UNVERIFIED |
| MRI-001 | MRI original PowerShell vs Rust feature and side-effect parity, delivery, 30-drive workflow | Original launcher and Rust files indexed; selected published CI runs green on other refs; no actual Windows or 30-drive device exercise in this run | UNVERIFIED |
| CAR-001 | Rust dashboard helper vs actual JS frontend and installed site behavior | Public source/Rust tree indexed; published CI passing on a different ref; no browser or release test in this run | UNVERIFIED |
| GUIDE-001 | Current guidebook source/render integrity, tests and model adoption | Version 1.2.2 loaded; selected published CI success on another ref; no local CLI runner or live-model adoption test this run | UNVERIFIED |
| GLOBAL-001 | All historical owner requirements reconciled per repository | Only repo lists, trees, selected files, CI/PRs collected; historical full issues/PRs/comments/history unread | NOT DONE |
| GLOBAL-002 | All intended Rust ports reach one-to-one parity and real end-to-end installed usability | No original-vs-Rust comprehensive differential execution or actual shipped launch across every repo | NOT DONE |

**No complete feature denominator has yet been established.** Expand each row by mode/target/original command, accepted owner requirement, dated source, revision, fixtures, outputs and side effects. Do not report an approximate parity percentage.

## Verified repair attempt (uYouPlus, isolated)

- Existing uYouPlus open PRs #4, #5, #6, #7 inspected; left unchanged. Branch `fix/rust-zip9-yanked-dependency-20261017` created from `20e9461115a7bb87532b60fd90f3469a12bce62a`.
- Commit `d5349d8d0cf271056847ed55f41812f6cba83c04` changes `rust/build-inputs/Cargo.toml` to `zip = { version = "9.0.4", default-features = false, features = ["deflate"] }`.
- Commit `37f0d7d893dc97278ad58c05ac7cf61a3443b09b` adapts `ZipFile::name()` from a direct string to `ZipResult<Cow<str>>` and swaps test fixture `FileOptions` for `SimpleFileOptions`.
- Both file contents were independently read back, hashes matched; GitHub compare: exactly two files, four additions and four deletions, no other files, two commits, base not advanced as of check. Superseded, closed (not merged) draft PR: https://github.com/Cucklord420/uYouPlus/pull/10 . Separate, still-open PR #9: https://github.com/Cucklord420/uYouPlus/pull/9
- The source API adaptation compiled on GitHub Actions in CI run 39005206451, but **two IPA tests FAILED** because ZipWriter 9 rejects duplicate synthetic fixture names during fixture creation. A distinct concurrent PR #9 instead updated to ZIP 8.6.0 and built malformed duplicate-name test inputs via controlled raw archive mutation; its Source validation job 117316245730 completed SUCCESS, including original Python/Rust differential tests. PR #9 is not merged, not installed, and not verified on a real iOS device. Preserve the original Python comparator and do not equate this single green CI cycle with global parity.

## Resumption constraints / prerequisites

1. Re-read current RustyNuts GOAL.md, Toe-Tickling AGENTS.md + full intake, this ledger, and refreshed branch heads, issue/PR activity and actions before editing.
2. Check PR #10 source validation. Resolve real dependency/API problems if failure. Repeated cycles and behavior diff cannot be claimed unless actually run. Do not merge without required gates/authorization.
3. Extract and reconcile historical owner requirements across each of the 14 authorized repositories (issues/PRs/comments/history, archived real user context where permitted, avoiding sensitive public disclosure); expand traceability beyond this initial sample.
4. Continue independent original-vs-Rust fixtures and executable packaging checks; real Windows/iOS/physical USB/service checks remain NOT DONE until access exists.
5. Toe-Tickling policy changes require editing canonical sources and regenerating/running its Rust CLI; no derived policy files should be edited solely to fake a green check.
6. Refresh all results against actual final revisions and keep every unavailable/unproven feature NOT DONE. This one chat session does not schedule ongoing execution.

## Concurrent repair reconciliation (same run, after original checkpoint)

- Existing concurrent PRs #8 and #9 opened while this audit was running. PR #8 changed the dependency to zip 0.6.5 and its Source validation passed; PR #9 changed it to zip 8.6.0, updated malformed ZIP fixture generation without disabling its regression, and its Source validation passed: https://github.com/Cucklord420/uYouPlus/actions/runs/39005239208 .
- Our ZIP9 draft PR #10 demonstrated a real green compile but red test run at https://github.com/Cucklord420/uYouPlus/actions/runs/39005206451 . It was commented and closed without merge to eliminate duplicate work. Source branch/commits remain inspectable, but should not be treated as a completed fix.
- Verification on PR #9: test job 117316245730 reports source validation success; this is one GitHub CI run, not three independent clean passes, not an iOS build or launch, and not proof that the historical owner requirements are fully captured.
- Due to multiple concurrent agents, fresh PR/branch inspection is a precondition for any later edits or integration. Avoid separate equivalent patches.
