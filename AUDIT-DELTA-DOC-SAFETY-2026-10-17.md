# RustyNuts private audit delta — Rust documentation-safety symlink-parent repair

**Date:** 10-17-2026 America/New_York. **Global status:** NOT DONE. This is a concrete repair/evidence addendum to the primary `AUDIT-CHECKPOINT-2026-10-17.md` and the earlier `AUDIT-DELTA-UYOU-2026-10-17.md`; it does not supersede or imply complete feature parity.

## Source and reproduction

The default-branch Rust code in `Cucklord420/odysseus-local-audit` and `Cucklord420/fedora-pain` both had identical `tools/docs-safety/src/main.rs` blob `5c6a0cde549d706b931537de82c0d52f4b9058a0`. The guard used `file.is_symlink()` for CHECK 07 and skipped reading only if that **leaf** was a symlink. If a *tracked child file* remains in the Git index after its parent folder is replaced by a symlink, the leaf is still a readable regular file; following it dereferences the parent and violates the intended refusal to follow tracked links. This matters to repository privacy scanning; no actual private paths or files were accessed or disclosed.

Official Rust reference consulted 10-17-2026: https://doc.rust-lang.org/std/fs/fn.symlink_metadata.html and https://doc.rust-lang.org/std/fs/ . `symlink_metadata` obtains metadata without following the final named symlink, and checking every path prefix exposes a linked parent.

## Exact changes and validation

| Requirement / repository | Baseline main | New branch/commit | Regression evidence | Result |
|---|---|---|---|---|
| ODYSSEUS-DOC-001: reject tracked file paths through linked parents | `9c0104bcaec469a06787b7bc8920937293954599` | `fix/rust-audit-symlinked-parents-20261017`, `7c61c7f2d61b1d45ffbd34a090340a7e61c285d9` | [PR #7](https://github.com/Cucklord420/odysseus-local-audit/pull/7), [final-head CI run 39005560752](https://github.com/Cucklord420/odysseus-local-audit/actions/runs/39005560752) | **PASS:** six Rust tests including real disposable Git fixture, repo self-audit passed. Unmerged. |
| FEDORA-DOC-001: same symlink safety behavior | `8fd379b6feb623679c45c9279b03648011b7cfa0` | `fix/rust-doc-symlinked-parents-20261017`, `78771d42117c59d8103c4665043f87074b7c3760` | [PR #8](https://github.com/Cucklord420/fedora-pain/pull/8), [final-head CI run 39005621401](https://github.com/Cucklord420/fedora-pain/actions/runs/39005621401) | **PASS:** Rust tests and repo self-audit on exact PR head. Unmerged. |
| DOC-GLOBAL-001: three final-edit clean cycles, independent semantic/adversarial/native platform review | Both branches | Same above | One clean successful GitHub Actions run per final head; new adversarial fixture and static review | **NOT DONE:** no two additional clean repeats, no independent Windows/macOS execution, hostile concurrent link swapping not proven safe. |
| ALL-GLOBAL-001: full historical owner requirements and actual app parity | RustyNuts GOAL.md | No replacement | Inventory, selected source and CI only | **NOT DONE** until every applicable row passes. |

The change is strictly Rust code/tests: helper `contains_symlink_component` incrementally checks each relative path component via `fs::symlink_metadata`; the existing CHECK 07 path rejection and no-dereference behavior apply to a parent as well as a leaf. A real synthetic fixture creates a Git repository, stages a normal `nested/tracked.md`, verifies clean audit, moves the directory and replaces its path with a symlink, verifies leaf is still a regular readable file, then verifies CHECK 07. One source file changed in each repo, with identical new blob `96261a46a832fa2e6c2e271a797a3a399093a5fe`.

## Scope constraints and concurrent PRs

- `fedora-pain` also has PR #7 concerning Git environment redirection (an independent attack path); do **not** overwrite or squash away its context-isolation checks. `odysseus-local-audit` has PR #4 concerning `.yaml` workflow coverage; likewise preserve both requirements. Neither of those other PRs is represented as merged.
- Source/final code was verified through authenticated GitHub readback and real Ubuntu workflow logs, not local Rust compilation. These proposed repairs are open **draft** PRs, not live production installs, releases or deployed validators.
- The parent symlink guard is path-check based and therefore not race-proof against a hostile actor swapping filesystem links between metadata check and the subsequent open. Do not claim a TOCTOU-resistant capability model.
- Further historical-owner requirements, staged-index content verification, native operating-system runs, real Odysseus restore, and comprehensive project parity remain unverified. Retain NOT DONE until fully evidenced.
