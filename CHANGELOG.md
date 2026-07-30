# Changelog

All material changes to the Decentralized Sovereignty canon are recorded here.

The format is inspired by [Keep a Changelog](https://keepachangelog.com/).  
**Markdown sources on `main` are the authoritative living text.** PDFs may lag.

---

## [Unreleased]

### Added

- Living-document process: full [CONTRIBUTING.md](CONTRIBUTING.md) with workflows, integrity gates, field-report format, translation/mirror path, and new-document proposal process.
- GitHub issue templates (critique, field report) and pull request template.
- `docs/drafts/` for non-canon proposals.
- Contribution footers on Documents I and II linking to process and changelog.
- Expanded README sections: living-document mechanics, contribution paths, hard gates, quick PR workflow.
- **Document III — U.S. Federal Legislative Strategy** (`docs/03-us-federal-legislative-strategy.md`): phased plan (coalition → study/pilots → authorization → appropriations → rights clarity → reauth), committee map, model legislative concepts, risk register, 90-day checklist; framed as Civil Continuity Infrastructure complementary to COG—not a crypto bill.
- Legislative kit: Hill one-pager, tracker, `docs/legislative/` index.

---

## [0.1.0] — 2026-07-30

### Added

- Initial public publication of the Decentralized Sovereignty canon.
- **Document I** — *Decentralized Sovereignty* (`docs/01-decentralized-sovereignty.md`): diagnosis, three ideals, seven pillars, ecosystem thesis, covenant, roadmap.
- **Document II** — *Order Hail Mary* (`docs/02-order-hail-mary.md` + PDF): threat model, independent failure domains principle, six protocols (SIGNAL, LEDGER, NAME, LIBRARY, MIND, COUNCIL), activation rules, address to nations.
- Professional README with explicit distinction between **crypto-scam / casino dynamics** and **decentralized infrastructure**.
- Contribution process, living-document rules, and integrity gates (`CONTRIBUTING.md`).
- Initial license was CC BY 4.0 (superseded; see Unreleased dual-license change).

### Status

| Document | Status |
|---|---|
| Document I — Decentralized Sovereignty | Published (living) |
| Document II — Order Hail Mary | Published (living) |

---

## How to add an entry

When your PR changes meaning, claims, protocols, or process:

1. Add a bullet under `## [Unreleased]`.
2. Use categories: `Added`, `Changed`, `Fixed`, `Contested`, `Deprecated`.
3. Link the PR or issue when known.
4. Maintainers may cut a dated version (`0.2.0`, etc.) when a batch of changes coheres.

Example:

```markdown
### Changed
- Protocol SIGNAL: note delay-tolerant networking as last-resort hop (`#12`)
```
