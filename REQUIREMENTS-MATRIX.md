# Cross-repository requirements and Rust parity matrix — initial evidence-bound extraction

**Checked:** 10-17-2026 (America/New_York). **Completeness: UNKNOWN; no global PASS.** This is an incrementally expandable cross-repository register, not a claim to have recovered every historical request. Distinguish CURRENT SPEC, OBSERVED CODE, OPEN AUDIT, OWNER-ACCEPTED and UNKNOWN. None of the rows below is independently classified as a newly recovered direct owner instruction solely from repository prose. This file carries **no personal account/transaction data**. Consult [AUDIT-LEDGER.md](AUDIT-LEDGER.md) for actual default refs, actions, CI failures, local tooling blockers and resumption.

## Evidence anchors

- Governing: `RustyNuts/GOAL.md` SHA `546d66b16d3a29ad9d66973554382278a21b5397`; Toe-Tickling GUIDEBOOK v1.2.2 SHA `45bdd5dce12eaf8cb74a22e0868a64852d85ed94`.
- MRI README SHA `f26fadb4d13a3f6b62aa036f85de6df515810abd`: https://github.com/Cucklord420/MRI-Drive-Maker/blob/main/README.md ; AGENTS SHA `004cb000400ebbcba6902eb7180b61d96d96450d`.
- Money PRODUCT_SPEC SHA `20ebf76175f00b27b535d0baf8a62060b4666774`, ROADMAP SHA `92d9898386c74872189e0837c9a4b9c8d2dc26fc`, AGENTS SHA `85d8dc2500370aac2421c9dd73ce52d2932dae69`; see https://github.com/Cucklord420/money-project/blob/main/docs/PRODUCT_SPEC.md .
- Car README SHA `80e6dafc6c6092995b78b2f93044dfc4a9b04bbe`; https://github.com/Cucklord420/car/blob/main/README.md .
- ChatGPT export README SHA `9c29a4c1e49d776cef67646b2cae25f5902ed706`; https://github.com/Cucklord420/chatgpt-projects-export/blob/main/README.md .
- Tech migration portfolio (historical 10-15-2026 checkpoint, not automatically current acceptance) SHA `a7100a6f446e108c471e95561fd1289ce27f77dc`; https://github.com/Cucklord420/tech-project/blob/main/docs/current/Rust_Migration_Portfolio_2026-10-15.md .
- Discord Theme README SHA `baccdaeb7c691dfa9d1a1f22a593697c942ed919`; NepetaMirror README SHA `2858772e2f3d2fd20a941f44f715e12e374fd67a`; ClearVision-v6 README SHA `e4cd4e4968d5e12388e00a618fdea957f21b2292`; discord-plus README SHA `00ba2b679e243e62eb08880acf3eb632f68487fc`.
- uYouPlus original `scripts/build_checks.py`, active Rust validators `rust/build-inputs/src/main.rs` and `src/bin/ipa.rs`, tests and workflows: https://github.com/Cucklord420/uYouPlus/tree/main/rust/build-inputs . Draft PR #9's Source validation passed at revision `0c3de00c3ff10714d67bb555594bb07133516d18`; no published device parity.
- Odysseus audit README SHA `0958c42c714c4dfa1ceb6147295e83c9c2480c11`; https://github.com/Cucklord420/odysseus-local-audit/blob/main/README.md .

All features below require documented OS/target/toolchain/feature configurations; source v. current ref; original input/output and side effects; real fixture and exit/status data; failure semantics; regression invalidation and three distinct verification families. **No row becomes PASS merely from text or CI on an unrelated ref.**

## MRI-Drive-Maker — current README / original PowerShell contracts

| ID | CURRENT SPEC / independent oracle needed | Candidate Rust work or actual safety gate | Status at this checkpoint |
| --- | --- | --- | --- |
| MRI-SEL-01 | Explicitly enumerate removable USB disk models, hardware serials, disk numbers; reject ambiguous/duplicate/unverified identity | Rust disk-selection/identity helpers vs PowerShell, Windows disposable device tests | UNVERIFIED / physical-device BLOCKED |
| MRI-SEL-02 | One-time exact `ERASE n,n` confirmation only for selected batch; never bleed into continuous watcher | Original PowerShell script and Rust selection / batch guard comparison | UNVERIFIED / destructive operations NOT AUTHORIZED |
| MRI-SEL-03 | Reject source/application/system/boot/non-USB/offline/write-protected targets, and target identity changed while queued | Simulated selection + race/removal, actual Windows identity just before write | UNVERIFIED / real device BLOCKED |
| MRI-SRC-01 | Source directory's contents go directly to USB root, not one nested folder; ISO or ZIP supported | Original source preparation and Rust manifest/path/contents helpers | UNVERIFIED |
| MRI-SRC-02 | Reject empty source, unsafe paths, FAT32-too-large files, unknown mounts, source links/junctions and source mutation | Rust manifest, path-safety, original PowerShell differential and Windows junction checks | UNVERIFIED; PR #35 Windows fixture CI failed at older head |
| MRI-WRITE-01 | Partition target MBR/active FAT32 up to 32,000,000,000 bytes; never write elsewhere; verify files SHA-256 after flush | PowerShell actual device writer remains; candidate Rust identity and receipt checks insufficient | NOT PORTED END-TO-END / physical BLOCKED |
| MRI-WRITE-02 | Failed/interrupted/cancelled builds never create new READY receipt; no marker/reports added to USB | Differential READY/FAILED and receipts/side effects | UNVERIFIED |
| MRI-BATCH-01 | Support 1–30 concurrency slots, default new config 4, saved limits retained; no implied 30-drive speed claim | Rust config/arrival guards partial; Windows multiple disposable USB tests needed | UNVERIFIED / hardware BLOCKED |
| MRI-BATCH-02 | Q cancellation stops unfinished builds; queue identity survives unplug/replug safely | Rust cancellation and tracking PRs, differential simulated and real races | UNVERIFIED |
| MRI-WATCH-01 | Advanced registration/automatic watcher ignores unregistered media; rejects unexpected existing files even in erase mode | Original watcher vs Rust candidate, real insert/removal/restart tests | UNVERIFIED |
| MRI-WATCH-02 | Verified unchanged watcher media may report ALREADY_READY without recopy; failed/changed media must not falsely pass | Source and receipt hashes, side-effect oracle | UNVERIFIED |
| MRI-PKG-01 | Extracted v0.3.0 download launches using actual START-MRI-DRIVE-MAKER.cmd, independent of checkout, admin as documented | Rust source-release generator + original launcher; offline Windows unpack/launch/install | UNVERIFIED / Windows BLOCKED |

No test in this session erased or wrote a physical USB. Existing partial Rust helper code is not a replacement for actual PowerShell disk operations.

## Money project — PRODUCT_SPEC, ROADMAP, AGENTS (fictional fixtures only)

| ID | CURRENT SPEC / oracle | Candidate test / Rust implementation | Status |
| --- | --- | --- | --- |
| MONEY-01 | A matched internal transfer must not count as income or spending | Rust finance-fixtures against synthetic transfer double entry; eventual app ledger | CURRENT SPEC, application UNIMPLEMENTED/UNVERIFIED |
| MONEY-02 | Card purchase counts once as spending; card payment not a second spend | Original spec acceptance #2; synthetic cycle in Rust fixture | CURRENT SPEC, application UNVERIFIED |
| MONEY-03 | Refund adjusts original category and retains purchase link | Original spec acceptance #3; synthetic refund event | CURRENT SPEC, application UNVERIFIED |
| MONEY-04 | Unlinked, unknown, stale, manual accounts remain visible; never map missing balance to zero | Spec acceptance #4 + AGENTS privacy/status | CURRENT SPEC, application UNVERIFIED |
| MONEY-05 | Dashboard totals drill down exactly to contributing records; staging/import preview and source fields are preserved | Spec acceptance #5; source-ID/stable-key reconciler | CURRENT SPEC, application UNVERIFIED |
| MONEY-06 | Debt APR, minimum, due date, promotional/deferred deadline and recurring bills show freshness/coverage gaps | Debt/Bills/Accounts views from PRODUCT_SPEC | CURRENT SPEC, application UNVERIFIED |
| MONEY-07 | All critical dates use America/New_York and MM-DD-YYYY; daily/monthly/yearly/custom filters supported | Spec acceptance #6 and interaction constraints | CURRENT SPEC, application UNVERIFIED |
| MONEY-08 | Every comparison or planned purchase exposes total cost of ownership and cash floors | Spec acceptance #7, dashboard and goals view | CURRENT SPEC, application UNVERIFIED |
| MONEY-09 | Export is sanitized; no actual account/transaction/raw credentials in repo or debug logs | AGENTS + negative fixture guarding; privacy review before any release | CURRENT SPEC, candidate guard CI only |
| MONEY-10 | No live money movement, autonomous trading, tax filing, bank credentials or estimates passed off as verified | Non-goals in PRODUCT_SPEC; negative integration checks | CURRENT SPEC, NEGATIVE REQUIREMENT UNVERIFIED |
| MONEY-11 | Data interface choice not yet settled: Excel, Sheets or local web app; don't invent chosen backend | ROADMAP Phase 1 explicitly undecided | OPEN PRODUCT DECISION, not an engineering PASS |

The repository's present Rust source provides guards and fictional fixture checks; **there is no evidenced full installed finance tracker**.

## Car — owner project research, frontend and privacy boundaries

| ID | CURRENT SPEC / oracle | Candidate Rust implementation / test | Status |
| --- | --- | --- | --- |
| CAR-01 | AWD Tesla shortlist and all hard fit, ventilated-seat, one-pedal, NACS and complete-TCO gates must remain user-visible; unknown quotes ≠ pass | `data/filters.json`, shortlist/dashboard original `app.js`, Rust dashboard-core | UNVERIFIED / source freshness |
| CAR-02 | Exact ZIP and exact-vehicle insurance/TCO evidence needed before a lease is financially viable | Worksheet/filter data provenance; no fabricated availability or insurance quotes | UNVERIFIED / external quotes |
| CAR-03 | GitHub Pages artifact must include only explicitly allowlisted public data and frontend assets; never publish private project-context, archive or checks | Pages staging workflow, Rust site audit and actual deployed artifact hash/directory listing | UNVERIFIED / deployment not established |
| CAR-04 | Browser dashboard filtering, interactive controls, DOM, responsive behavior, accessibility, data error handling and client-side integrations match original | Headless browser JS-vs-Rust/WASM differential and shipped Pages launch | UNVERIFIED / actual browser & Pages tests |

## ChatGPT export and Odysseus — private data integrity, delivery and restoration

| ID | CURRENT SPEC / oracle | Candidate test / Rust implementation | Status |
| --- | --- | --- | --- |
| EXP-01 | Preserve each recorded historical archive byte with independent SHA-256/source evidence; don't equate old notes with actual bytes | Existing manifests, Rust split-archive and nested ZIP verifier vs Python | UNVERIFIED for actual private assets |
| EXP-02 | Detect missing, duplicate, tampered, malformed or symlinked archive members without arbitrary extraction or overwrite | Rust read-only archive verifier and security regression CI on final refs | UNVERIFIED end-to-end |
| EXP-03 | Verify all requested ChatGPT data classes and recoverable Odysseus import, not just backed-up project files | Current MIGRATION-STATUS, isolated restored databases and real app login | NOT DONE / real restore unavailable |
| EXP-04 | Private data stays private (memory, transcript, image, credentials, account assets); publicly tracked CI uses synthetic inputs only | Privacy audit of source, reports, logs and artifacts; safe fixture tests | UNVERIFIED / negative requirement |
| ODYS-01 | `odysseus-local-audit` is a docs/templates record, NOT a backup or current live service | Docs safety Rust checks; actual host restore tests remain separate | DOCUMENTATION SCOPE; live restoration NOT VERIFIED |

## Original-format preservation and guidebook integrity

| ID | Existing required interface / oracle | Rust role and independent test | Status |
| --- | --- | --- | --- |
| UYOU-PLAT-01 | Python input/IPA safety behavior remains differential oracle; Objective-C/Logos iOS hooks and Theos work on supported devices | Partial Rust safety helper, actual built signed IPA install/launch parity | UNVERIFIED / iOS device BLOCKED |
| NEPETA-01 | Original upstream mirror packages/index and third-party rights must remain byte/format compatible | Rust read-only verifier only, full repo integrity baseline | UNVERIFIED; no package rewrite authorized |
| CSS-01 | Archived discord-plus theme CSS/asset behavior and license remain unchanged | No Rust rewrite implied; CSS must render in Discord | FORMAT-BOUND / in-scope change UNKNOWN |
| CSS-02 | ClearVision-v6 SCSS/CSS and themed visual output must remain compatible | Only optional build tooling candidate, byte-identical CSS + visual regression | FORMAT-BOUND / UNVERIFIED |
| CSS-03 | Discord-Theme overrides keep working as actual Vencord CSS; README's placeholder raw URL is not deployable until grounded | Competing open documentation PRs, functional Vencord load comparison | OPEN DOCS BUG, UNVERIFIED |
| TECH-01 | Existing Fedora original maintenance/rollback, sanitization, exact error/no-leak behavior remains the oracle for proposed Rust ports | rust/diagnostics-core vs original Python, isolated Fedora host verification | UNVERIFIED / privileged host BLOCKED |
| TECH-02 | Technical plans are portable and host-replaceable; real backup/restore matters, not solely docs or mock CI | Current master and read-only tests; isolated running service restore | UNVERIFIED |
| DOCS-01 | fedora-pain and odysseus-local-audit documentation guard behavior must remain consistent on current refs | Existing Rust docs-safety modules, original historic Python checks | UNVERIFIED at final ref |
| GUIDE-02 | Guidebook Rust builder, adoption and independent auditor preserve canonical IDs, evolution, sources and generated views | Toe-Tickling Cargo build/check/audit+original golden baselines, tests and CI | UNVERIFIED parity; policy protection issue #15 remains |
| GOAL-01 | Every authorized historical owner requirement included; all desired ports verified one-to-one before global DONE | This ledger, authoritative GOAL, actual original/runtime+history and final CI for every row | NOT DONE; matrix incomplete by design |

## Reconciliation / expansion rules

1. Each row is currently **CURRENT SPEC** or **OBSERVED BEHAVIOR** as indicated. For owner-originated historical requirements, add immutable issue/PR/comment/commit URL and timestamp, acceptance/supersession authority, and reason. Do not silently convert an AI-proposed fix into an owner decision.
2. Split a row into per-input, per-platform, per-side-effect variants before testing when meaningful. Store exact original and new revisions, command, fixture SHA, deterministic expected outputs, execution result, and the last validation timestamp. An unknown fixture is not a test PASS.
3. Reverify all affected rows after updating Rust, original, dependencies, toolchains, data, tests or guidebook. The current list is explicitly **not** the complete denominator, and no comprehensive coverage claim is authorized.
4. Never check financial data or private archive contents into this file; quote only existing sanitised specs and their source refs.
