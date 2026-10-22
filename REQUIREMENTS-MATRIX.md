# RustyNuts public requirements and parity matrix

**Evidence checkpoint:** 10-17-2026  
**Privacy correction:** 10-21-2026  
**Scope:** Public repositories and reusable, non-sensitive acceptance rules only.

The previous matrix combined public requirements with non-public project inventory, commits, paths and vulnerabilities. Those entries were removed from the current public version. Detailed requirements for private software must be maintained within its own access-controlled repository.

| Gate | Requirement | Evidence before completion |
|---|---|---|
| REQ-001 | Inventory active public entrypoints and supported platforms | Versioned public source and executable/manifest references |
| REQ-002 | Preserve original-versus-Rust behavior | Independent golden-master fixtures and real entrypoint comparisons |
| REQ-003 | Cover safety and negative cases | Path traversal, symlink/junction, missing/invalid input and rollback tests |
| REQ-004 | Preserve platform and package behavior | Exact platform CI, build/release artifact checks, signature/format/license compatibility |
| REQ-005 | Avoid release/deployment overclaims | Explicit TESTED / MERGED / DEPLOYED / RESTORED distinctions |
| REQ-006 | Prevent public/private information crossover | Check target visibility, permission, secret scan and provenance before each publication |

Public repository-specific evidence should be recorded on that repository's Issues/PRs. For general public duplicate tracking see [#31](https://github.com/Cucklord420/RustyNuts/issues/31). Earlier file revisions remain in Git history; this limits current default-branch disclosure rather than purporting to erase it.
