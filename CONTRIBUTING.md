# Contributing to Order Hail Mary

This canon is a **living document**. It is not a finished product dropped from on high. It is a public standard under continuous stress-test: argued with, forked, cited, corrected, and improved by anyone willing to do the work in the open.

If you found a flaw, a missing citation, a protocol that fails independent-failure-domain analysis, or a practice that works in the real world — **you are the update process.**

---

## The Spirit of Contribution

These texts exist because the original promise of decentralized systems was strip-mined by casino culture. Contributions that rebuild that promise are welcome. Contributions that smuggle casino dynamics back in will be rejected without ceremony.

**We want:** clearer threat models, better engineering, honest field reports, stronger privacy architecture, offline-first designs, and critique that makes the documents harder to dismiss.

**We do not want:** token pitches, guaranteed-return language, influencer marketing, governance theater, or “partnerships” that are really exit liquidity.

---

## Ways to Contribute (Pick Your Depth)

You do not need to be a protocol engineer. Different kinds of work keep the document alive.

| Path | Who it's for | What you do | Where |
|---|---|---|---|
| **Read & argue** | Anyone | Open an issue with a precise objection or question | [Issues](https://github.com/AlexBTC420/order-hail-mary/issues) |
| **Correct the record** | Domain experts | Fix facts, add citations, flag overclaims | Issue or PR |
| **Strengthen a protocol** | Builders / operators | Propose design notes, threat models, or standing-order refinements for SIGNAL–COUNCIL | PR to `docs/` |
| **Field report** | Practitioners | Document real mesh, self-custody, offline archive, local AI, or council practice | Issue with label `field-report` |
| **Translate / mirror** | Communities | Translate or host offline copies; link back here | Issue + mirror URL |
| **Implementation** | Engineers | Ship offline-first, open-source tools that embody a protocol | PR or linked repo |
| **Editorial clarity** | Writers | Tighten language without changing meaning; fix typos | PR |
| **Governance of the text** | Maintainers & community | Propose process changes to how the living document evolves | Issue with label `process` |

---

## How the Living Document Evolves

```text
idea / critique
      │
      ▼
 GitHub Issue  ──►  discussion (public, archived)
      │
      ▼
 Pull Request  ──►  review against the gates below
      │
      ▼
 merge to main  ──►  CHANGELOG entry  ──►  document is updated
```

1. **Main branch is the current canon.** What is on `main` is the public text.
2. **Every material change is visible.** No silent rewrites of commitments.
3. **Changelog is mandatory** for substantive edits (see [CHANGELOG.md](CHANGELOG.md)).
4. **Covenant clauses are hard to change.** Anything that weakens “never promise profit,” transparency of allocations, or the scam/infrastructure distinction requires explicit community discussion and a clear rationale in the PR.
5. **Forkability is a feature.** If maintainers go wrong, fork. That is the design — not a threat to it.

### Document status labels

Used in the README and changelog:

| Status | Meaning |
|---|---|
| **Draft** | Not yet considered canon; open for rough input |
| **Published (living)** | Public canon; open to revision under this process |
| **Stable section** | Unlikely to change without strong evidence |
| **Contested** | Active disagreement; do not treat as settled |
| **Deprecated** | Superseded; kept for history |

---

## Before You Open Anything

1. Read [README.md](README.md) — especially the **crypto scam vs. decentralized infrastructure** section.
2. Read the document you want to change:
   - [Document I — Decentralized Sovereignty](docs/01-decentralized-sovereignty.md)
   - [Document II — Order Hail Mary](docs/02-order-hail-mary.md)
3. Search [existing issues](https://github.com/AlexBTC420/order-hail-mary/issues) so you don’t duplicate work.
4. Prefer **one idea per issue/PR**. Small, reviewable changes beat manifesto rewrites.

---

## Opening an Issue

Use issues for discussion before (or instead of) large PRs.

### Good issues

- “Part I understates X; here is a source and a proposed paragraph.”
- “Protocol SIGNAL should mention delay-tolerant networking (RFC 4838); reason: …”
- “This sentence overclaims. Soften to: …”
- Field report: “We ran a neighborhood mesh for 6 months; standing order worked / failed as follows…”

### Issue template (copy/paste)

```markdown
## Which document?
- [ ] Document I — Decentralized Sovereignty
- [ ] Document II — Order Hail Mary
- [ ] README / meta
- [ ] New document proposal

## Section / line (if known)
...

## What is wrong, missing, or improvable?
...

## Proposed change (optional but preferred)
...

## Evidence / references
...

## Integrity check
- [ ] This does not promise financial returns
- [ ] This does not promote a token sale or casino dynamic
- [ ] This improves independent failure domains, clarity, or honesty
```

### Labels we use (or will use)

| Label | Purpose |
|---|---|
| `critique` | Challenge to claims or framing |
| `citation-needed` | Fact or threat model needs sources |
| `protocol:signal` … `protocol:council` | Scoped to a protocol |
| `field-report` | Real-world practice report |
| `editorial` | Clarity / typo / structure |
| `process` | How the living document is governed |
| `out-of-scope` | Casino / marketing / token pitches |

---

## Opening a Pull Request

### Workflow

```bash
# 1. Fork the repository on GitHub, then:
git clone https://github.com/<you>/order-hail-mary.git
cd order-hail-mary
git remote add upstream https://github.com/AlexBTC420/order-hail-mary.git

# 2. Create a branch
git checkout -b fix/protocol-signal-dtn

# 3. Edit the living text (prefer Markdown sources in docs/)
#    - docs/01-decentralized-sovereignty.md
#    - docs/02-order-hail-mary.md
#    - README.md when the front door must stay consistent

# 4. Record the change
#    Add a dated entry under [Unreleased] in CHANGELOG.md

# 5. Commit with a clear message
git add -p
git commit -m "docs: strengthen SIGNAL with delay-tolerant networking note"

# 6. Push and open a PR against main
git push -u origin HEAD
```

### PR checklist (maintainers and authors)

- [ ] Change is scoped; unrelated drive-bys removed
- [ ] `CHANGELOG.md` updated under **Unreleased** if the change is material
- [ ] No profit promises, token launches, or investment framing
- [ ] Claims that sound empirical either have citations or are labeled as thesis / research goal
- [ ] Scam vs. infrastructure distinction is preserved or sharpened
- [ ] PDF (`docs/02-order-hail-mary.pdf`) noted as stale if Markdown canon diverged (PDF may lag; Markdown is authoritative)
- [ ] Linked issues referenced (`Fixes #12`, `Discusses #7`)

### Commit message style (preferred)

```
docs: <short imperative summary>
fix: <factual correction>
meta: <process, README, contributing>
feat: <new protocol note, appendix, or tool>
chore: <typos, formatting only>
```

Examples:

- `docs: add Carrington-event references to threat model`
- `fix: correct overclaim about stablecoin freezes`
- `meta: expand contributing field-report path`

---

## Editorial Gates (What Gets Merged)

Every material PR is reviewed against these gates. Fail any hard gate → no merge.

### Hard gates (automatic reject)

1. **No investment solicitation.** No returns, yields, “early,” or price narratives.
2. **No hidden extraction.** No design that depends on asymmetric team exits dressed as community.
3. **No anti-sovereignty bait-and-switch.** Closed control planes sold as decentralization.
4. **No lawless violence framing.** Resilience ≠ insurgency cosplay. This is continuity of civilization, complementary to legitimate continuity of government.
5. **No silent covenant edits.** Weakening Document I’s covenant requires explicit callout and discussion.

### Soft gates (quality bar)

1. **Independent failure domains.** Does the proposal survive “same building / same power / same authority / same permission”?
2. **Falsifiability.** Can a reader tell what would prove the claim wrong?
3. **Offline-first preference.** Peacetime utility is the drill; paper-only hopes are weak.
4. **Attribution.** Credit prior art; cite standards, papers, RFCs, historical events.
5. **Tone.** Professional, reasonable, scientifically grounded. Revolutionary in stakes, not in crank volume.

---

## Field Reports (Especially Valuable)

The doctrine is worthless if it only works on paper. Field reports are first-class contributions.

### Suggested structure

```markdown
## Protocol(s)
SIGNAL / LEDGER / NAME / LIBRARY / MIND / COUNCIL

## Context
Location type (urban/rural), scale, duration, constraints

## What you did
Standing orders actually executed

## What worked
...

## What failed
...

## Suggested text change (optional)
Quote from docs/ + proposed revision

## Artifacts
Links to open code, configs, offline pack manifests (no doxxing)
```

Open as an issue with title: `Field report: <protocol> — <one-line outcome>`.

---

## Proposing a New Canon Document

Documents beyond I and II are welcome when they:

1. Extend the canon without contradicting the three ideals and seven pillars without justification,
2. Are infrastructure-first (not product marketing),
3. Include a threat model or falsifiable claims,
4. Carry the same covenant spirit.

Process: open an issue titled `Proposal: Document III — <title>`, discuss, then PR a draft under `docs/drafts/`. Drafts are not canon until the README canon table is updated and the draft is moved to a numbered path.

---

## Translations and Mirrors

- Translations: PR to `docs/i18n/<lang>/` with a note on who translated and how to report errors.
- Offline mirrors: open an issue with the public URL or distribution method. Mirrors should not reframe the text as investment material.
- PDF lag: Markdown on `main` is authoritative. PDFs may trail; help regenerating them is welcome.

---

## Code of Conduct (Lightweight)

1. **Attack claims, not people.**
2. **No brigading, doxxing, or harassment.**
3. **No scam promotion** — even “ironically.”
4. **Assume good faith once; require evidence always.**
5. Maintainers may close issues that are spam, token shilling, or bad-faith noise.

---

## Maintainer Notes

- Prefer merging incremental truth over perfect consensus theater.
- When contested, mark the section **Contested** in the changelog rather than papering over dissent.
- Keep the front-door README synchronized with any covenant or scam/infrastructure wording changes.
- Never sell the repo, the doctrine, or contributor goodwill as a token.

---

## Quick Start (Minimum Viable Contribution)

1. Star/fork if you want a local copy.
2. Open one issue with one precise improvement.
3. Or fix one typo / one missing citation via PR + changelog line.
4. Or file one field report from something you actually ran.

That is enough. Living documents grow from many small honest edits, not one messianic rewrite.

---

## Questions?

Open an issue with label `process` or start a discussion on the PR that confuses you.  
Argue with the text. Fork it if we fail you. That is not a threat to this project — **that is the design.**

*Sovereignty is not granted. It is built — together, in the open, or not at all.*
