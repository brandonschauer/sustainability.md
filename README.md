# sustainability.md

An open AI skill for integrating sustainability into experience design,
strategy, and operations.

<https://sustainability.md>

Most sustainability tooling asks you to go somewhere else and start a
different task. This one doesn't. It rides along inside CX and UX work,
journey maps, prioritization calls, event plans, RFPs and roadmaps — and
speaks up only when it has something worth the interruption.

It triggers on the work, not the word. You never have to say
"sustainability."

## Before / after

You ask for a meal-kit onboarding journey. You get touchpoints, drop-off
risks, and a retention plan.

With sustainability.md you get the same thing, plus one line where it counts:

> **Hidden emissions —** the printed recipe cards in every box run ≈ 4,000
> miles of driving a year across a 10k subscriber base (US EPA). Moving them
> in-app is the single highest-ROI change on this map, and it removes a
> reprint cost too.

One insight. Cited. Next to the decision it affects. Then it gets out of
the way.

## Install

### Claude Code plugin

```
/plugin marketplace add brandonschauer/sustainability.md
```
```
/plugin install sustainability@sustainability-md
```

Send them as two separate prompts, then restart Claude Code so the skill
loads.

In the Claude Code desktop app, type the same two commands into the prompt
box, or use the **+** button → **Plugins** → **Add plugin** to browse
marketplaces.

### Anywhere else — copy and paste

The skill is a plain Markdown file. Paste
[`sustainability.md`](sustainability.md) into a ChatGPT Custom GPT, a Gemini
Gem, a Claude Project, or your assistant's custom instructions. No install,
no account, nothing to configure. That fallback is the point.

You can also drop
[`plugins/sustainability/skills/sustainability/`](plugins/sustainability/skills/sustainability/)
into `~/.claude/skills/` to use the packaged skill without the plugin.

## Commands

| Command | What it does |
|---|---|
| `/sustainability` | Set the intensity: `integrated` (default), `deep`, `brief`, `suggest`, `off` |
| `/sustainability-review` | Scan a doc, design artifact, plan or diff for hidden emissions and the 1–2 highest-impact opportunities |

Plugin skills are namespaced, so these appear as
`/sustainability:sustainability` and `/sustainability:sustainability-review`
in the `/` menu.

`/sustainability-review` takes a path or `diff`; with no argument it reviews
the current working diff.

## How it behaves

Four behaviors, delivered as nudges rather than reports:

1. **Inline insight** — the one consequential implication, next to the
   recommendation it concerns.
2. **One relatable number, cited** — an inseparable pair. "Several hundred
   miles of driving (US EPA)." Never a bare percentage, never an uncited
   figure.
3. **ROI ranking** — sustainability as one column among your own criteria,
   never the widest.
4. **Hidden emissions, labeled** — the non-obvious sources: shipped kits,
   event food waste, over-provisioned infrastructure.

And one rule above all of them: **the core task comes first.** Sustainability
stays around a quarter of a response or less, and spends its budget on the
one or two highest-impact insights. Silence in the other sections is correct
behavior, not a gap. A skill that takes over your session gets uninstalled;
a proportionate nudge that survives a hundred sessions does far more good.

## What's in this repo

```
sustainability.md                        the open skill file — paste this anywhere
index.html                               the landing page served at sustainability.md
CHANGELOG.md                             version history

.claude-plugin/marketplace.json          the plugin marketplace catalog
plugins/sustainability/
  .claude-plugin/plugin.json             the plugin manifest
  skills/sustainability/
    SKILL.md                             the skill (auto-triggers)
    references/knowledge.md              factors, sources, hidden-emissions catalog
  skills/sustainability-review/
    SKILL.md                             the on-demand review pass
```

The knowledge layer holds the conversion factors, reference cases and the
authoritative source table behind every citation. It is reviewed monthly.

> **Version note.** The packaged plugin ships skill **v1.4.x**, rebuilt
> through three evaluation rounds against no-skill baselines. The root
> [`sustainability.md`](sustainability.md) is still the **v1.1.1** original.
> Converging the two — so the paste-in file is generated from the same source
> as the plugin — is in progress. Until then, the plugin is the current one.

## Scope

Order-of-magnitude support for design and strategy thinking — not Life Cycle
Assessment, not GHG Protocol accounting, not compliance advice. When precision
is critical (formal ESG reporting, SBTi targets), it says so and points to
qualified practitioners.

## Contributing

Issues and pull requests welcome — corrections to emission factors, new
reference cases, and hidden-emissions patterns from your own domain are the
most useful contributions. Factor changes should cite a named source.

## License

CC BY 4.0 — Brandon Schauer / Rare.org. Use it, adapt it, ship it; keep the
attribution.
