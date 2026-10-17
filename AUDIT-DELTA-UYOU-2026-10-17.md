# RustyNuts resumable audit delta — 10-17-2026

**Status: NOT DONE / PARTIAL.** Private connected-GitHub task record. This is a supplement to the existing `AUDIT-CHECKPOINT-2026-10-17.md`, not a replacement. No background execution or whole-repository feature parity is claimed.

## Authority, current baseline and scope

- RustyNuts goal read: `GOAL.md` blob `546d66b16d3a29ad9d66973554382278a21b5397`; Toe-Tickling main `4f519c3ea1ed120d36aefea014fbf31bc0593304`, guidebook 1.2.2, `AGENTS.md` read in full and mandatory guidebook reading sequence completed.
- Authenticated GitHub owner `Cucklord420`. Repository inventory: 14 accessible repositories, one archived; inventory/initial matrix already in the preceding checkpoint. Distinguish default-branch state from concurrent PR heads.
- uYouPlus default `main` baseline `20e9461115a7bb87532b60fd90f3469a12bce62a`. Third-party iOS/Theos code and existing Python original deliberately untouched.
- Official documentation checked on 10-17-2026: https://doc.rust-lang.org/stable/book/ch11-01-writing-tests.html , https://doc.rust-lang.org/cargo/guide/continuous-integration.html , https://docs.rs/zip/8.6.0/zip/write/struct.ZipWriter.html , https://docs.rs/zip/8.6.0/zip/write/type.SimpleFileOptions.html . Rust `zip` 8.6.0 `start_file` refuses duplicate names, requiring genuine malformed fixtures.
- Available execution: authenticated GitHub code/CI APIs. Local `cargo`/`rustc` unavailable, no native iOS runtime or test-device access, no local dirty working-tree visibility. CI results refer to an Ubuntu GitHub-hosted runner, not an end-user device.

## Verified investigation and changes

1. Historical failure: [uYouPlus CI run 38858741097](https://github.com/Cucklord420/uYouPlus/actions/runs/38858741097) on PR #4: Rust test command `cargo test --manifest-path rust/build-inputs/Cargo.toml` failed during dependency selection because `zip = "^0.6.6"` was yanked. The 38 original Python regressions passed. Source `rust/build-inputs/Cargo.toml` and `rust/build-inputs/src/bin/ipa.rs` read at exact baseline.
2. Created isolated branch `fix/rust-zip-yanked-dependency-20261017` from `20e946...`, updated `zip` to 8.6.0 with `deflate` only and updated Rust synthetic fixture option type. Commits `622aff5c0008b2c3808ddbcc924fb4d4f2e15418` and `4a69ae270702af52344b3ad32e3923e69acd0baa`. GitHub readback and compare verified two changed source paths.
3. Initial run [39005113420](https://github.com/Cucklord420/uYouPlus/actions/runs/39005113420) compiled the updated crate but **FAILED** two Rust tests: ZIP 8.6.0 rejects duplicate fixture filenames at generation time (`InvalidArchive("Duplicate filename: Payload/YouTube.app/Info.plist")`). This was a real behavioral API difference, not permission to delete the negative tests.
4. Root-cause correction: altered only Rust test fixture helper to generate a distinct same-length ZIP filename, then patch both ZIP name records to the deliberate duplicate after ZipWriter finish. Kept both malformed-file rejection and original-Python differential tests intact. Commit `0c3de00c3ff10714d67bb555594bb07133516d18`.
5. Latest [CI run 39005239208](https://github.com/Cucklord420/uYouPlus/actions/runs/39005239208) on that commit: **SUCCESS**. Run contains Python original security regression tests, Rust unit and differential tests, build shell syntax and Theos source layout checks. This is one validated final-head CI cycle; not three clean cycles, not full IPA app build, and not actual iOS install/launch.
6. [Draft PR #9](https://github.com/Cucklord420/uYouPlus/pull/9) holds only the isolated ZIP dependency and fixture changes; **OPEN, NOT MERGED**. Simultaneously, independent [PR #8](https://github.com/Cucklord420/uYouPlus/pull/8) on another branch changes `zip` 0.6.6 -> 0.6.5; its own [CI run 39005006392](https://github.com/Cucklord420/uYouPlus/actions/runs/39005006392) succeeded. These are alternative concurrent repairs: review both, avoid blind combining or merging, preserve both histories.

## Requirements / parity evidence — incremental rows, not complete denominator

| ID | Acceptance condition / original oracle | Rust path/revision | Test evidence / side effects | Status |
|---|---|---|---|---|
| UYOU-001 | Rust build-input crate resolves dependencies and runs its tests | `rust/build-inputs/Cargo.toml` at `0c3de00...` | Run 39005239208 SUCCESS; no user IPA changed | **PASS** only for this PR-head Ubuntu CI dependency resolution |
| UYOU-002 | Existing original-Python input-validation examples retain acceptance behavior | `rust/build-inputs/src/main.rs` unchanged | Run 39005239208 Rust/Python tests passed; selected fixture coverage, not every URL variant | **PASS** for existing workflow cases; broader parity **UNVERIFIED** |
| UYOU-003 | Malformed IPA paths, duplicate entries and hash mismatch rejected safely; original Python behavior retained | `rust/build-inputs/src/bin/ipa.rs` at `0c3de00...` | Failed cycle above caused fixture repair; final run 39005239208 passed; source unmodified except test code | **PASS** for exercised fixture cases; adversarial completeness **UNVERIFIED** |
| UYOU-004 | End-to-end signed IPA creation, install, launch, integration, all upstream iOS/user-visible features parity | Original `Makefile`, `build.sh`, `Sources`, `Tweaks`, runtime dependencies; Rust partial helper only | No real iOS IPA build/install or physical-device runtime observed | **NOT DONE / UNVERIFIED** |
| UYOU-005 | Final-head fmt, strict Clippy, release build, feature/platform matrix and three clean cycles | Rust ZIP crate at `0c3de00...` | Workflow does not execute every gate; one final-head successful workflow cycle observed | **NOT DONE / UNVERIFIED** |
| ALL-001 | Exhaustive accepted owner-history matrix across every authorized repository, every Rust port/workflow | GOAL.md | Prior checkpoint covers inventory and a handful of summary rows only | **NOT DONE** |

## Continuing work and blockers

- Verify exact current branch heads and overlapping PR statuses before every further edit. PR #8 and PR #9 solve the same initial symptom in different ways; no implicit merge authorization or clean-head claim.
- More exhaustive original-vs-Rust differential fixtures, failed/partial ZIP handling, fuzzing, format/Clippy, release packaging, physical iOS install/launch, and original iOS functionality remain open. Do not count a passing Rust helper as one-to-one parity for the complete application.
- Other independent projects: historical owner requirements/issues/history, initial build/oracle, final-revision CI and hardware/supported-platform checks still to be examined and traced. The prior inventory is a snapshot, not proof of completion.
- The private checkpoint and this delta constitute verified remote writes only if they remain readable at the stated path. Neither is a live scheduler or an authorization to rewrite third-party upstream projects.

**Review condition:** mark global `NOT DONE` until every applicable requirement has independent original oracle, implementation, fully verified real-user workflow, reproducible tests, final-head CI, and historical provenance with no unknown or blocked applicable row.
