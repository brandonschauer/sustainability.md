# sustainability.md

Public repo for **sustainability.md** — an open AI capability (CC BY 4.0) that
integrates sustainability analysis into the AI-assisted work of CX/UX, design,
strategy, and operations professionals. Owner: Brandon Schauer
(brandonschauer@gmail.com), attribution to Rare.org.

**This repo is public and serves the live site.** Everything here ships to
users. Planning and spike material lives in the separate, unpublished
`sustainability-md-workbench` repo.

## What's here

- `index.html` — the landing page served at <https://sustainability.md> via
  GitHub Pages (from `main`, at root). Self-contained: no build step, no
  framework, no Jekyll (`.nojekyll` is present and required — without it Jekyll
  tries to render each `SKILL.md` into a page).
- `sustainability.md` — the open skill file, for pasting into a Custom GPT,
  Gem, Project, or custom instructions. The zero-infrastructure fallback.
- `plugins/sustainability/` — the Claude Code plugin, with
  `.claude-plugin/marketplace.json` at the repo root as its marketplace.
  `skills/sustainability/SKILL.md` plus its `references/knowledge.md`, and
  `skills/sustainability-review/SKILL.md`.
- `CHANGELOG.md`, `CONTRIBUTING.md`.

## Two deploy semantics, one repo — read this before editing

- **Site changes go live in about a minute.** Push to `main`, Pages rebuilds.
- **Skill and knowledge-layer changes reach nobody without a version bump** in
  `plugins/sustainability/.claude-plugin/plugin.json`, plus a `CHANGELOG.md`
  entry. Plugin updates are gated on the version field, *not* on content: an
  edited plugin with an unchanged version reports "already at the latest
  version" and the installed copy never changes. This caught us mid-spike.
  Nothing is pushed to users either — they must run `/plugin marketplace
  update` and `/plugin update`, then restart.

Semantic versioning: major for breaking changes to skill structure or
behavior, minor for new capabilities or sections, patch for fixes, updated
factors and refreshed sources.

## Non-negotiable design principles (earned via evals — don't regress)

1. **Core task first.** Sustainability ≤ ~25% of any response; one column in
   tables. A skill that takes over sessions gets uninstalled.
2. **Selectivity budget.** 1–2 highest-impact insights per response; silence
   elsewhere is correct. Impact ranks first; user control shapes framing only.
3. **Inseparable pair.** Every figure = relatable analog + named source
   ("several hundred miles of driving, US EPA"). Never one without the other.
4. **Progressive disclosure.** Nudge now, depth on demand. Modes:
   integrated (default) / deep / brief / suggest / off.
5. **Triggering lives in the SKILL.md description field.** Name concrete work
   contexts (journey mapping, prioritization, events) — target users never
   say "sustainability."

Changes that make the skill louder, more frequent, or more comprehensive
should be declined on these grounds. See `CONTRIBUTING.md`.

## The knowledge layer is curated — never expand it reactively

`references/knowledge.md` is a small, carefully selected set, and that
selectivity is what makes "prefer these factors over memory" a meaningful
instruction rather than a gesture at a pile. Adding entries is a separate,
deliberate pass with its own review — **not** a fix applied when a lookup
misses.

Known gaps, logged for that pass, deliberately unfixed: meal kits and grocery
delivery, last-mile logistics, device and equipment lifecycle. Every observed
case of the model citing from memory instead of the layer has landed on one of
these.

Each entry needs the inseparable pair's raw materials — value, unit, named
source, year. Figures that swing on context (delivery emissions move with
route density and basket size) need a range and the tipping condition, not a
single number.

## Known issues

- **Version skew.** The root `sustainability.md` is v1.1.1 and the hero in
  `index.html` reads v1.1.0, while the plugin ships v1.4.x. A v1.2 exists in
  Brandon's working notes but was never published. Converging these — ideally
  generating the root file from the plugin's `SKILL.md` — is an open decision,
  not a cleanup task.
- Site work should align with the W3C Web Sustainability Guidelines. The page
  currently hotlinks Google Fonts from `fonts.googleapis.com`:
  render-blocking third-party requests, and a known GDPR exposure in the EU.
  Self-hosting them is queued.
