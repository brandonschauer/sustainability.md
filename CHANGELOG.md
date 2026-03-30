# Changelog

All notable changes to sustainability.md are documented here.

This project follows [Semantic Versioning](https://semver.org/):
- **Major** versions introduce breaking changes to skill structure or behavioral instructions
- **Minor** versions add new capabilities or sections in a backward-compatible way
- **Patch** versions fix errors, update emissions factors, or refresh authoritative sources

---

## [1.2.0] — 2026-04

### Added
- Activation modes: `integrated` (default), `brief`, `suggest`, `off`
- Session and persistent mode-setting instructions under new `## Activation Modes` section
- Mode-aware delivery behavioral instruction (§5) in `## Core Behavioral Instructions`
- Context-aware first-use mode offer: after first substantive output in a conversation,
  the skill briefly explains the active mode and offers to switch — once, with a
  recommendation based on task type

---

## [1.1.0] — 2026-03

### Added
- Initial public release
- Four core behavioral instructions: sustainability analysis (§1), relatable impact
  estimates (§2), sustainability ROI ranking (§3), hidden emissions and resource
  waste detection (§4)
- Knowledge layer covering climate science foundations, GHG accounting (Scope 1–3),
  freshwater scarcity and water footprint methodology, biodiversity and land use,
  AI's own environmental footprint, and experience design behavior change principles
- Authoritative sources table: IPCC AR6, IPCC SRCCL, IPCC SR1.5, GHG Protocol,
  SBTi, WRI, IEA, Water Footprint Network, IPBES, FAO AQUASTAT, US EPA eGRID,
  Verma & Tan (2024), de Vries-Gao (2025), McKinsey Global Institute (2024)
- Reference cases: LUT University food waste forecasting, Klarna sustainable
  shopping UX, Google Hotels eco-certification badges
- Scope and limitations section
- Activation instructions for single-conversation and persistent system-level use
- CC BY 4.0 license with attribution guidance

---

## Maintenance notes

**Recommended review cadence:** Monthly, to incorporate new IPCC guidance, updated
EPA eGRID emissions factors, or emerging research on AI environmental footprints.

**To suggest a change:** Open a GitHub issue or pull request at
[github.com/brandonschauer/sustainability.md](https://github.com/brandonschauer/sustainability.md).
Contributions that add authoritative new sources, worked examples, or domain
modules are especially welcome. See `CONTRIBUTING.md` for guidelines.
