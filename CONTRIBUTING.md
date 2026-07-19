# Contributing to sustainability.md

Thanks for being here. This is an open capability (CC BY 4.0) and it gets
better with contributions from people who do the work it's meant to support —
CX and UX practitioners, service designers, strategists, operations and
procurement people.

## What's most useful

**Worked examples.** A real decision where sustainability analysis changed the
outcome, with enough detail to be instructive. These are the hardest thing to
write and the most valuable thing to receive.

**Hidden-emissions patterns from your domain.** The catalog covers experience
and digital, operations and procurement, and product and service design. If
your field has a footprint the catalog misses — healthcare, logistics,
education, live events — that's a gap worth naming, even as an issue rather
than a pull request.

**Corrections.** A factor that's out of date, a source that's been superseded,
a figure that doesn't survive scrutiny. Corrections are always welcome and
always get priority.

**Trigger misses.** Cases where the skill should have activated and didn't, or
activated when it shouldn't have. Include the prompt you used. Triggering is
driven by the `description` field, and real-world misses are the only reliable
way to tune it.

## Two things to know before proposing new reference material

**The knowledge layer is deliberately small.** `references/knowledge.md` is a
curated set, not a collection. Its selectivity is the point: the skill tells
the model to prefer these factors over its own memory, and that instruction
only means something if the set is tight enough to be worth preferring.
Additions are reviewed as a considered curation pass, so a well-argued issue
proposing an addition is often more useful than a pull request adding one.

**Every figure needs its pair.** The skill never ships a number without both a
relatable analog and a named source — "≈4,000 miles of driving (US EPA)" — so
a proposed factor needs value, unit, named source and year. Figures that swing
on context (delivery emissions, for instance, move with route density and
basket size) need a range and the condition that moves them, not a single
number. A confident-looking figure with hidden variance is worse than no
figure.

## The design principles are load-bearing

Several behaviors in `SKILL.md` look like they could be relaxed and can't.
They came from evaluation rounds against no-skill baselines, and each one
fixes an observed failure:

1. **The core task comes first.** Sustainability content stays at roughly a
   quarter of a response or less. A skill that takes over sessions gets
   uninstalled, and does no good at all after that.
2. **The selectivity budget.** One or two insights per response, not one per
   section. Silence in the remaining sections is correct behavior.
3. **The inseparable pair.** Analog and source travel together, always.
4. **Progressive disclosure.** Nudge now, depth on request.
5. **Triggering lives in the description field**, and names concrete work
   contexts — journey mapping, prioritization, events — because the people who
   most need this never search for "sustainability."

Proposals that make the skill louder, more frequent, or more comprehensive
will usually be declined on these grounds. Proposals that make it sharper,
better sourced, or better targeted are the ones to send.

## Practicalities

- **Issues** for anything you're unsure about, and for all knowledge-layer
  additions. Lower effort for you, and it's where the useful discussion happens.
- **Pull requests** for corrections, typos, broken links, and documentation.
- Changes to the skill or knowledge layer need a version bump in
  `plugins/sustainability/.claude-plugin/plugin.json` and a `CHANGELOG.md`
  entry. Without the bump, installed users never receive the change — plugin
  updates are gated on the version field, not on content.
- Semantic versioning: **major** for breaking changes to skill structure or
  behavior, **minor** for new capabilities or sections, **patch** for fixes,
  updated factors and refreshed sources.

## License

Contributions are accepted under CC BY 4.0, with attribution to Rare.org. By
opening a pull request you agree your contribution may be distributed under
that license.
