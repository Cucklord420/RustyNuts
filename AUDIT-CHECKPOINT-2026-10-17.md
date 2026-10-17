# RustyNuts — 10-17-2026 GitHub discovery checkpoint

**Status: IN PROGRESS / NOT DONE.** This file records only work actually performed in one connected GitHub audit pass; it is NOT an executed global Rust-port parity audit. Timezone for the observation date: America/New_York. No work is promised outside the active goal/session.

## Task/authority
- Complete governing task read from `GOAL.md` blob `546d66b16d3a29ad9d66973554382278a21b5397` in `RustyNuts/main`.
- Toe-Tickling `AGENTS.md` blob `5407f0bcf6dd092033ba80399b02519c13c1a998`; main HEAD `4f519c3ea1ed120d36aefea014fbf31bc0593304`; policy version **1.2.2** (`GUIDEBOOK.md` blob `45bdd5dce12eaf8cb74a22e0868a64852d85ed94`).
- Intake documents fetched and read: `AGENTS.md`, `GUIDEBOOK.md` in bounded sections, `README.md`, `RULEBOOK.md`, `docs/SELF_CHECKS.md`, `docs/EVOLUTION.md`, `docs/ADOPTION.md`, `docs/PROVENANCE.md`, `docs/SCENARIOS.md`, `CONTRIBUTING.md` and `policy.json`. Not a full independent semantic policy audit; canonical `policy/rules.json` contents were not individually audited.
- Applicable gates: ENG-001/002/003/006/007/010/015–020, EXEC-008–012, AUD-001–020, EVO-021/022/026. Generated guide files are not canonical edits.
- Official documentation actually consulted on 10-17-2026: [Rust Book testing](https://doc.rust-lang.org/stable/book/ch11-00-testing.html), [Cargo CI](https://doc.rust-lang.org/cargo/guide/continuous-integration.html), [release notes](https://doc.rust-lang.org/releases.html). Official releases show Rust **1.99.1** dated 10-15-2026; Toe-Tickling pins `1.99.1`, MRI manifest declares edition `2021`.

## Enumerated repository baseline

The connected account returned **14 repositories**; their recursively requested default-branch trees were all received with `truncated: false`. The counts below are present file-tree observations only, not whole-repository historical, executable, or acceptance audits. Exactly **84 open pull requests** across this snapshot, not 84 merged fixes. Changes pending in another branch do not validate main.

| Repository | HEAD commit | Files | Rust .rs | Open PRs |
|---|---|---:|---:|---:|
| [NepetaMirror](https://github.com/Cucklord420/NepetaMirror) | `20b9dab1a3127ebfeeb9068376c49145047df80b` | 414 | 1 | 5 |
| [discord-plus](https://github.com/Cucklord420/discord-plus) | `e8bbb172315f45fe5f1099390fc4133db036310b` | 38 | 0 | 0 |
| [ClearVision-v6](https://github.com/Cucklord420/ClearVision-v6) | `1eac93750a6d8d1f35bae562201d49d3aa64bb99` | 148 | 0 | 4 |
| [uYouPlus](https://github.com/Cucklord420/uYouPlus) | `20e9461115a7bb87532b60fd90f3469a12bce62a` | 69 | 2 | 4 |
| [fedora-pain](https://github.com/Cucklord420/fedora-pain) | `8fd379b6feb623679c45c9279b03648011b7cfa0` | 8 | 1 | 5 |
| [Discord-Theme](https://github.com/Cucklord420/Discord-Theme) | `52f1f7d5522b95b3f79cdb7379137fa337ad3e6a` | 7 | 0 | 6 |
| [tech-project](https://github.com/Cucklord420/tech-project) | `e133bbaedff557b984bad684ab8b0be9ce9df64c` | 99 | 19 | 12 |

| Repository | HEAD commit | Files | Rust .rs | Open PRs |
|---|---|---:|---:|---:|
| [chatgpt-projects-export](https://github.com/Cucklord420/chatgpt-projects-export) | `8649569f808eac4b07d1d66a7681d34f65400c43` | 1641 | 25 | 5 |
| [money-project](https://github.com/Cucklord420/money-project) | `5194f42a8eb43ead29721b90ef6210cd72c9ec8d` | 23 | 2 | 6 |
| [car](https://github.com/Cucklord420/car) | `6b396d3612f6451a45df04282b6e40bf6c167f7d` | 131 | 5 | 6 |
| [odysseus-local-audit](https://github.com/Cucklord420/odysseus-local-audit) | `9c0104bcaec469a06787b7bc8920937293954599` | 12 | 1 | 3 |
| [MRI-Drive-Maker](https://github.com/Cucklord420/MRI-Drive-Maker) | `58677cd30cc85c641ecb411328cd3fcf73e7805e` | 186 | 8 | 23 |
| [Toe-Tickling](https://github.com/Cucklord420/Toe-Tickling) | `4f519c3ea1ed120d36aefea014fbf31bc0593304` | 66 | 9 | 5 |
| [RustyNuts](https://github.com/Cucklord420/RustyNuts) | `f04a929716b6707a63c02dcfebaf5e6384555eec` | 3 | 0 | 0 |

## Scope classifications (preliminary, NOT full source review)

- **NepetaMirror** (`master`): Rust mirror verifier; original package contents require preservation. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **discord-plus** (`master`): Archived; confirm applicability before changing. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **ClearVision-v6** (`master`): Theme/CSS project, migration applicability not established. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **uYouPlus** (`main`): Inherited iOS build; Rust input helper; preserve upstream rights. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **fedora-pain** (`main`): Rust documentation safety utility. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **Discord-Theme** (`main`): Theme/CSS project; not automatically a Rust port. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **tech-project** (`main`): Offline diagnostics Rust port with original Fedora/Python behavior. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **chatgpt-projects-export** (`main`): Seven Cargo manifests; archive/import/restore parity not established. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **money-project** (`main`): Rust fixture and sensitive-file guard; avoid real financial material. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **car** (`main`): Rust dashboard/site checks with inherited JS webpage. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **odysseus-local-audit** (`main`): Rust doc guard; local restore must be independently validated. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **MRI-Drive-Maker** (`main`): PowerShell production launcher; partial independent Rust policies. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **Toe-Tickling** (`main`): Rust guidebook validator/generator; concurrent PRs. Requirement history and end-to-end acceptance still **UNVERIFIED**.
- **RustyNuts** (`main`): Private goal specification; no Rust executable at baseline. Requirement history and end-to-end acceptance still **UNVERIFIED**.

## Initial requirements/parity trace rows (NOT an exhaustive denominator)

| ID | Owner/spec source and intended behavior | Evidence so far | Status |
|---|---|---|---|
| MRI-001 | [MRI README](https://github.com/Cucklord420/MRI-Drive-Maker/blob/main/README.md): real Windows launcher, safe per-device confirmation, FAT32 copy/hash | Current README read; original PowerShell entrypoints present; archived VHD/CI claims apply to cited older revisions only | **NOT VERIFIED** — no current-run physical/workstation tests |
| MRI-002 | Full Rust parity with MRI original and BDE/firmware workflow | Four Rust crate manifests inventoried; 23 open PRs include ports of read-only decision helpers; production launcher remains PowerShell | **NOT DONE** — no end-to-end parity or firmware/real MRI oracle |
| EXPORT-001 | [Migration status](https://github.com/Cucklord420/chatgpt-projects-export/blob/main/MIGRATION-STATUS.md): complete archive and functional import/restore | Existing doc explicitly says complete backup and migration unverified; not tested in this session | **NOT VERIFIED** |
| TECH-001 | [tech-project README](https://github.com/Cucklord420/tech-project/blob/main/README.md): portable diagnostics and project operations | 19 Rust sources inventoried; PRs #30, #33, #34, #41–44 change original parity/validation | **NOT VERIFIED** — no live Fedora comparison |
| GUIDE-001 | [Toe-Tickling AGENTS](https://github.com/Cucklord420/Toe-Tickling/blob/main/AGENTS.md): render/check/build, stable policy IDs, model adoption | Version and files read; open PRs #17–20 and #6 exist; no local `cargo` execution | **NOT VERIFIED** |
| ALL-001 | [RustyNuts GOAL](https://github.com/Cucklord420/RustyNuts/blob/main/GOAL.md): every still-applicable historical requirement independently passing | Only repository trees plus selected READMEs/docs and sampled PR/CI evidence reviewed | **NOT DONE** — per-feature historical matrix incomplete |

Each applicable feature/requirement must eventually be entered individually with: owner citation, chronological supersession, original oracle/input, Rust path, actual tests/results/side effects, supported targets, code/CI revision, risk and blocker. These initial summary rows do not establish that all requirements have been enumerated.

## Concrete observations and outstanding work
1. Current [MRI README](https://github.com/Cucklord420/MRI-Drive-Maker/blob/main/README.md) explicitly states READY validates copied bytes but **does not prove MRI bootability**; physical USB, actual MRI payload and original BDE equivalence are absent from its historical validation. No destructive media was touched in this audit.
2. Current [MRI AGENTS.md](https://github.com/Cucklord420/MRI-Drive-Maker/blob/main/AGENTS.md) still says new Rust is *preferred*; Toe-Tickling ENG-001 makes it mandatory for new executable source. MRI PR [#31](https://github.com/Cucklord420/MRI-Drive-Maker/pull/31) already proposes to correct this; coordinate instead of duplicating.
3. Source HEADs are not pending PR heads. For example, MRI PR [#34](https://github.com/Cucklord420/MRI-Drive-Maker/pull/34) proposes dependency locking; no claim that its fix is on main.
4. GitHub Actions snapshot includes completed success runs at some PR revisions (for example MRI [run 39004730482](https://github.com/Cucklord420/MRI-Drive-Maker/actions/runs/39004730482), Toe-Tickling [run 39001877175](https://github.com/Cucklord420/Toe-Tickling/actions/runs/39001877175)), and an earlier failure on an export PR [run 38857914855](https://github.com/Cucklord420/chatgpt-projects-export/actions/runs/38857914855). No claim has been made that that failure persists on the latest head; logs/root cause not reviewed.
5. No compiler/runtime/parity validation was executed in this session. The available shell does not expose `cargo`, and `git ls-remote` over the public internet failed with `Could not resolve host: github.com`. The authenticated connector supports source/PR/CI reads and GitHub file changes, but it is not a Windows/Linux/native test runner. Local dirty working tree state is unavailable.
6. No edits were made to Rust implementations, public Toe-Tickling canonical rules, deployed software, USB drives, or live services. This private checkpoint is the only intended write. Retain external blockers as **NOT DONE** rather than treating CI, branch existence or a document as end-to-end proof.

## Continuation / invalidation sequence
1. Re-read GOAL and current guide HEAD and revision, and this checkpoint; refresh all 14 repository heads and open PRs before touching overlapping changes.
2. Obtain an actual isolated checkout/test runner with the necessary pinned Cargo toolchains and Windows/Fedora/other target facilities; do not substitute a guessed local path or test result.
3. For each project, resolve archived/forked/inherited scope, read instructions, all accepted owner history, source and original, collect real baseline oracle, populate **individual** requirement rows. Distinguish project scope from mere Rust-utility presence.
4. Triage existing PRs and failed workflows before proposing duplicate fixes; inspect exact diffs and commit-specific run logs. Protect private archive material and never put it in a public repository.
5. For each independently actionable defect: reproduce -> add meaningful Rust regression -> make reversible fix -> mechanical, behavioral, adversarial, repeated clean tests -> original-vs-Rust differential and packaged entrypoint -> inspect CI and remote state. Mark none of these as executed until genuine logs exist.
6. Retain **NOT DONE** until the full reconciled feature/history denominator is established and every applicable row has verified PASS at a final revision; revisit blockers without blind retries.

**Receipt distinction:** fourteen default-branch recursive trees fetched and structurally inventoried; source and PR reading was selective; complete history, parity, installation, real hardware and post-merge behavior were **not** inspected. This is a resumable discovery checkpoint only.
