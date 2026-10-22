# RustyNuts public audit ledger

**Original evidence checkpoint:** 10-17-2026  
**Privacy correction:** 10-21-2026  
**Status:** PARTIAL — NOT CERTIFIED COMPLETE

The former cross-repository ledger mixed public and private source inventories, revision hashes, operational details and defects. The current public file no longer contains that sensitive inventory. This is a public-only coordination index; private work belongs in appropriately access-controlled repository Issues, PRs and evidence records.

## Public evidence rules

- Verify exact repository visibility before copying source or discussion content into a different repository.
- Follow public issue coordination in [#31](https://github.com/Cucklord420/RustyNuts/issues/31); avoid duplicate Issues/PRs and retain independently necessary negative tests.
- Require original-entrypoint functional parity, stable schemas, security regression coverage, platform packaging, real workflows when safe and justified, and exact-head CI.
- Distinguish merged source from deployed software; a Draft PR or CI success is not real-device verification.
- Never put secrets, private security findings, non-public repository names or other internal system context in a public tracker.

Earlier Git history and third-party copies may remain accessible; current-content redaction does not erase them.
