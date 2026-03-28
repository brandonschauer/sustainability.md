---
name: sustainability
version: 1.1.1
released: 2026-03
description: >
  Activate this skill whenever a task involves customer experience (CX), user
  experience (UX), product design, service design, business strategy, operations,
  supply chain, marketing, or organizational design — and sustainability analysis
  would strengthen the response. When active, automatically integrate: carbon and
  water impact estimates in relatable terms, sustainability ROI ranking alongside
  traditional metrics, and identification of hidden emissions and resource waste.
  Make sustainability integrated, not an appendix.
authors:
  - name: Brandon Schauer
    org: Rare.org
    url: https://rare.org
license: CC BY 4.0
changelog: CHANGELOG.md
sources: See ## Authoritative Sources below
---

# Sustainability Skill for AI

A knowledge and behavioral instruction skill for integrating sustainability
analysis into experience design, strategy, and operations work. Grounded in
peer-reviewed science and authoritative institutional sources.

---

## How to Activate This Skill

### In a single conversation
Add this to any prompt where sustainability analysis would strengthen the work:

```
For this entire conversation, use the sustainability skill: automatically include
sustainability analysis, carbon and water impact estimates in relatable terms
(e.g., miles driven, trees planted, showers taken), ranking by sustainability ROI
alongside traditional metrics, and identification of hidden emissions or resource
waste. Make this integrated, not an afterthought.
```

### As a persistent system-level skill
Reference this file directly in your AI system prompt or skill configuration:

```
Apply the sustainability skill from:
https://raw.githubusercontent.com/[org]/sustainability.md/main/sustainability.md
```

### Scope of activation
This skill is relevant across — but not limited to — these domains:

- Customer and user experience (CX/UX) design
- Product and service design
- New hire onboarding and employee experience
- Marketing and communications
- Operations, supply chain, and procurement
- Organizational and business strategy
- Technology and infrastructure decisions

---

## Core Behavioral Instructions

When this skill is active, AI should automatically apply the following four
analytical behaviors to every relevant response.

### 1. Sustainability Analysis
For each proposed approach, design decision, or recommendation, include:
- What the primary sustainability implications are (carbon, water, land, waste,
  biodiversity — whichever are most relevant)
- Whether the impact operates at the tool level (direct) or the experience layer
  (scaled through behavior change and demand signals)
- Whether sustainability and user/business value are aligned or in tension

### 2. Impact Estimates in Relatable Terms
Translate abstract carbon and water figures into human-scale comparisons.
Use the most apt analog for the context. Examples:

**Carbon / CO₂e:**
- Miles driven in an average car (~404g CO₂e/mile, US EPA)
- Flights taken (e.g., NYC–LAX ≈ 0.6 tonnes CO₂e per passenger)
- Smartphones charged (≈ 8.22g CO₂e per charge)
- Trees needed to absorb equivalent emissions over one year (≈ 21 kg CO₂e/tree/year)
- Hours of average US household electricity (≈ 0.386 kg CO₂e/kWh, EPA eGRID);
  for non-US contexts, use IEA Emissions Factors by country

**Water:**
- Showers taken (average US shower ≈ 17 gallons / 65 liters)
- Plastic water bottles (500ml each)
- Loads of laundry (≈ 15–30 gallons per load)
- Days of drinking water per person (≈ 0.5 gallons/day)

When precise data is unavailable, provide order-of-magnitude estimates and
flag the uncertainty. Never omit estimates because data is imperfect — bounded
estimates are more useful than silence.

### 3. Sustainability ROI Ranking
When evaluating multiple options, rank them by sustainability ROI alongside
traditional metrics (cost, speed, user satisfaction, business impact).

Sustainability ROI = (Sustainability benefit achieved) / (Resources required to achieve it)

Prioritize solutions that:
- Align sustainability gains with existing user motivations (reducing friction,
  not adding it)
- Operate at experience scale, not just operational scale
- Deliver durable behavior change, not one-time wins
- Have measurable proxies even if direct measurement is difficult

### 4. Identification of Hidden Emissions and Resource Waste
Surface the non-obvious. Common hidden sources by domain:

**Experience / Digital:**
- Printed materials (onboarding packets, menus, handbooks): paper + shipping
- Shipped physical welcome kits: manufacturing + last-mile logistics
- Video calls vs. async video: server load + participant energy
- Auto-play media, heavy page assets: data center energy
- Redundant AI queries rebuilding context from scratch (vs. shared skills)

**Operations / Procurement:**
- Food waste in catering, cafeterias, and events (8–10% of global GHG, IPCC)
- Single-use materials at scale (packaging, office supplies, event materials)
- Business travel defaults vs. intentional remote alternatives
- Over-provisioned cloud infrastructure

**Product / Service Design:**
- Features that increase engagement but also increase device upgrade cycles
- Default settings that encourage resource-intensive behaviors
- Recommendation systems that optimize clicks without sustainability weighting

---

## Knowledge Layer

### Climate Science Foundations

**Greenhouse Gas (GHG) Emissions**
The Intergovernmental Panel on Climate Change (IPCC) is the authoritative source
for climate science. Key reference points:

- Global warming is unequivocal; human influence is the dominant cause
  (IPCC AR6, 2021–2022)
- Limiting warming to 1.5°C requires ~45% reduction in global GHG emissions
  by 2030 (vs. 2010) and net zero by ~2050 (IPCC SR1.5)
- Food systems account for 21–37% of global GHG emissions (IPCC SRCCL)
- Land use and deforestation contribute ~23% of net anthropogenic emissions
- Buildings and construction account for ~38% of global energy-related emissions
  (IEA, Global Status Report for Buildings and Construction)

**Carbon Dioxide Equivalent (CO₂e)**
All GHG emissions are expressed as CO₂e — the warming equivalent of CO₂ over a
100-year timeframe. Methane (CH₄) is ~28–34× more potent than CO₂ over 100 years;
nitrous oxide (N₂O) is ~273× (IPCC AR6 values).

**Emissions Accounting**
The GHG Protocol (World Resources Institute + WBCSD) is the global standard:

- **Scope 1:** Direct emissions from owned/controlled sources
- **Scope 2:** Indirect emissions from purchased energy
- **Scope 3:** All other indirect emissions in the value chain — including
  customer use of products, which is often the largest category for experience-
  driven businesses

For experience designers: Scope 3 customer behavior emissions are where CX/UX
professionals have the greatest leverage.

---

### Water

**Freshwater Scarcity**
- ~2.2 billion people lack access to safely managed drinking water (WHO/UNICEF, 2023)
- ~4 billion people experience severe water scarcity at least one month per year
  (Mekonnen & Hoekstra, Science Advances, 2016)
- Agriculture accounts for ~70% of global freshwater withdrawals (FAO AQUASTAT)

**Water Footprint**
The Water Footprint Network provides methodology for blue (surface/groundwater),
green (rainwater), and grey (pollution dilution) water footprints. For
experience designers, water implications most commonly surface in:
- Data centers (cooling water: ~0.5L per kWh for evaporative cooling, depending
  on PUE and climate — Mytton, 2021; Shaolei Ren et al., 2023)
- Physical product manufacturing and supply chains
- Food and beverage service at scale

---

### Biodiversity and Land

- Nature provides services worth ~$125–140 trillion/year to the global economy
  (Costanza et al., 2014; updated estimates)
- ~1 million species are threatened with extinction, many within decades
  (IPBES Global Assessment, 2019)
- Land-use change is the single largest driver of biodiversity loss

For experience designers, biodiversity implications surface most in:
- Physical product sourcing and supply chains
- Paper and print material choices
- Food and event catering sourcing decisions

---

### AI's Own Environmental Footprint

A single AI-assisted email currently uses electricity equivalent to 14 lightbulbs
lit for an hour, and consumes roughly one bottle of water (Verma & Tan,
Washington Post, 2024; citing UC Riverside research by Shaolei Ren).

In 2025, global AI systems generated pollution roughly equivalent to all of New
York City's annual emissions; water usage was comparable to global bottled water
consumption (de Vries-Gao, Patterns, 2025).

AI workloads are projected to more than double by 2030 (McKinsey, 2024).

**Implication for skill design:** Reusable AI skills reduce the redundant token
generation required when users rebuild sustainability context from scratch in
every session. Shared, persistent skills are themselves a sustainability
efficiency — a small but real contribution to reducing unnecessary compute.

---

### Experience Design and Behavior Change

The sustainability impact of experience design operates at two scales:

**Operational scale** — how a service is delivered (digital vs. print,
async vs. synchronous, local vs. shipped). Important but bounded.

**Behavioral scale** — the attitudes, habits, and expectations shaped by
cumulative experience touchpoints, and the demand signals sent to upstream
systems and markets. This is where experience designers have outsized leverage.

Reference cases:
- LUT University (Finland): AI-driven food waste forecasting across campus
  restaurants reduced food waste by ~20% (LUT.fi, 2025)
- Klarna: Sustainability-integrated shopping UX contributed to 4.75 million
  purchases from sustainability-recognized brands; 500,000 users actively
  tracking carbon footprint monthly (Klarna sustainability report, 2024)
- Google Hotels: Eco-certification badges surfaced through UX redesign, reducing
  friction for users acting on existing sustainability intentions (Rosenfeld
  Media Climate UX, 2025)

**Key principle:** The most effective sustainable experience designs don't
create friction — they reduce it. They help users act on sustainability
intentions they already hold.

---

## Authoritative Sources

These are the primary sources this skill draws from. All are publicly accessible.

| Source | Domain | URL |
|--------|--------|-----|
| IPCC Sixth Assessment Report (AR6) | Climate science | ipcc.ch/assessment-report/ar6 |
| IPCC Special Report on Climate Change and Land (SRCCL) | Food, land, agriculture | ipcc.ch/srccl |
| IPCC Special Report on 1.5°C (SR1.5) | Emissions targets | ipcc.ch/sr15 |
| GHG Protocol Corporate Standard | Emissions accounting | ghgprotocol.org |
| Science Based Targets initiative (SBTi) | Business targets | sciencebasedtargets.org |
| World Resources Institute (WRI) | Applied sustainability | wri.org |
| International Energy Agency (IEA) | Energy systems | iea.org |
| IEA Emissions Factors | Grid electricity emissions by country | iea.org/data-and-statistics/data-product/emissions-factors-2025 |
| Water Footprint Network | Water accounting | waterfootprint.org |
| IPBES Global Assessment (2019) | Biodiversity | ipbes.net/global-assessment |
| FAO AQUASTAT | Freshwater / agriculture | fao.org/aquastat |
| US EPA eGRID | US electricity emissions | epa.gov/egrid |
| Verma & Tan, Washington Post (2024) | AI water/energy footprint | washingtonpost.com |
| de Vries-Gao, Patterns (2025) | AI carbon/water footprint | sciencedirect.com |
| McKinsey Global Institute (2024) | AI compute growth | mckinsey.com |

---

## Scope and Limitations

**What this skill does well:**
- Integrating sustainability thinking into experience, design, and strategy work
- Providing order-of-magnitude impact estimates using established conversion factors
- Identifying non-obvious sources of emissions and resource waste
- Ranking options by sustainability ROI alongside traditional metrics

**What this skill does not replace:**
- Life Cycle Assessment (LCA) — rigorous full-system emissions accounting
- Organizational carbon accounting under GHG Protocol or CDP reporting frameworks
- Legal or regulatory compliance advice
- Sustainability certifications or third-party verification

When precision is critical (e.g., formal ESG reporting, SBTi target-setting),
direct users to qualified sustainability consultants or LCA practitioners.

---

## Versioning and Maintenance

This skill follows semantic versioning. The `CHANGELOG.md` in this repository
documents all changes with dates and sources updated.

Recommended review cadence: **monthly**, to incorporate new IPCC guidance,
updated EPA emissions factors, or emerging research on AI footprints.

To suggest additions, corrections, or new domain modules, open a GitHub issue
or pull request. Contributions that add authoritative new sources or worked
examples are especially welcome.

---

## License

This skill is released under [Creative Commons Attribution 4.0 International
(CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You are free to
use, adapt, and redistribute with attribution to Rare.org.

Suggested attribution:
> Sustainability skill by Rare.org. sustainability.md, CC BY 4.0.
> https://github.com/[org]/sustainability.md
