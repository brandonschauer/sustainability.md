---
name: sustainability-review
description: >
  Scan a design artifact, document, plan, or code diff for hidden emissions and
  the one or two highest-impact sustainability opportunities in it. Use when the
  user asks to review something for sustainability, environmental impact, hidden
  emissions, or carbon and water footprint, or invokes /sustainability-review.
  This is the on-demand deep pass; the ambient nudges live in the sustainability
  skill.
argument-hint: "[path or 'diff' — defaults to the current diff]"
disable-model-invocation: true
license: CC BY 4.0 — Brandon Schauer / Rare.org · https://sustainability.md
---

# Sustainability review

Scan one artifact for environmental impact the author cannot see. This is the
dial-up pass the main skill offers — the user asked for it, so depth is welcome
here in a way it never is by default.

## What to scan

`$ARGUMENTS` names the target: a file path, a directory, "diff", or nothing.
With nothing or "diff", review the working diff (`git diff HEAD`, falling back
to `git diff` and untracked files). Read the artifact before judging it.

Works on whatever the user actually makes: journey maps, service blueprints,
onboarding flows, event and offsite plans, RFPs and procurement docs, roadmaps
and prioritization tables, marketing plans, and code diffs. For a code diff,
review what the code *causes in the world* — shipped kits, print jobs, travel,
over-provisioned infrastructure, defaults that shape millions of user actions —
not its own style.

## The selectivity budget still applies

Report the **one or two highest-impact** findings, not everything you noticed.
This pass earns depth by being right about what matters, not by being long. A
list of eight findings is the failure mode: it reads as an audit nobody asked
for and buries the lever that mattered. Rank by size of impact first; if the
biggest lever is outside the user's control, name it in one line and pair it
with the strongest lever they do hold.

If the artifact has no meaningful footprint, say `No material footprint here.`
and stop. That is a real and common answer — do not manufacture a finding.

## Format

One block per finding:

`<location>: <tag> <what> — <the number, analog, source>. <what to do instead>.`

Tags:

- `hidden:` a footprint the artifact never names — shipped kits, printed
  collateral, catering waste, business-travel defaults, idle infrastructure.
- `scale:` a default or design choice that multiplies across every user, so a
  small per-use figure becomes the dominant term.
- `lever:` a change with high sustainability ROI (benefit ÷ effort) the author
  is already positioned to make.
- `lock-in:` a decision that is cheap to change now and expensive later —
  vendor, venue, material, or infrastructure commitments.

**Every figure ships as an inseparable pair: a relatable analog AND a named
source** ("≈ 4,000 miles of driving, US EPA"). Never one without the other —
a bare percentage is not relatable, an uncited number is not credible. Pull
factors from `references/knowledge.md` in the sustainability skill; prefer them
over memory. Bounded estimates beat silence — flag uncertainty as a range.

## Close

End with one line naming the single highest-ROI move:
`Highest sustainability ROI: <X>.`

Then offer the dial-up in one clause — the full ROI breakdown, the wider
hidden-emissions catalog, or the sources behind the figures.

## Boundaries

Order-of-magnitude support for design and strategy decisions — not Life Cycle
Assessment, GHG Protocol accounting, or compliance advice. When precision is
critical (formal ESG reporting, SBTi targets), say so and point to qualified
LCA practitioners. Lists findings; does not rewrite the artifact unless asked.
