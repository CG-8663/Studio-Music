# Project Overview — Major 72 Studio

> Generated: 2026-04-08 | Status: Pre-Development Planning Phase

---

## Executive Summary

**Major 72 Studio** (working title: **Signal Foundry**) is a professional-AI hybrid music production platform designed to bridge the gap between generic AI music generators and traditional manual studio production. The platform encodes professional creative judgment — specifically that of lead producer **Eddie Wilson** — into selectable "Creative Modes" that guide AI-assisted music creation from rough demo to release-ready output, and from digital production to live stage performance.

The project is currently in the **strategic planning and requirements definition phase**. No source code has been written. The repository contains strategic documentation, technical specifications, and scaffolding for the BMad Builder design-to-development workflow.

---

## Quick Reference

| Attribute | Value |
|---|---|
| **Project Name** | Major 72 Studio (Signal Foundry) |
| **Project Type** | Pre-development planning project |
| **Repository Type** | Monolith |
| **Target Platform** | Cloud-native web application (GAW — Generative Audio Workstation) |
| **Lead Producer** | Eddie Wilson |
| **Current Phase** | Strategic planning / requirements definition |
| **Tech Stack** | Not yet determined (see gap-analysis.md, GAP-1) |
| **AI Tooling** | BMad Builder, Claude Code, Gemini |

---

## Target Architecture (Future State)

The platform is planned as a 6-layer system:

1. **Core Production Engine** — Stem separation, automated mixing/mastering
2. **Creative Mode Architecture** — Producer taste profiles and band style templates
3. **Live Integration Layer** — Score generation, click tracks, SoundBetter marketplace
4. **Consumer Personalization** — Custom songs for emotional milestones
5. **Blockchain Royalty Infrastructure** — Smart contracts, provenance, automated payouts
6. **Marketplace & Licensing** — Producer Mode marketplace, sync licensing

See [Technical Specs](./technical-specs.md) for detailed breakdowns.

---

## Repository Structure

| Folder | Purpose |
|---|---|
| `docs/` | Project knowledge base — strategic, technical, and gap analysis documents |
| `design-artifacts/` | Phased design outputs (Product Brief → UX → Design System → Development) |
| `_bmad-output/` | BMad workflow artifacts (planning, implementation, testing) |
| `_bmad/` | BMad Builder tooling installation |

See [Source Tree Analysis](./source-tree-analysis.md) for detailed annotated tree.

---

## Key Documents

| Document | Description |
|---|---|
| [Strategic Framework](./strategic-framework.md) | Full market analysis, competitive positioning, vision |
| [Technical Specs](./technical-specs.md) | Actionable specs with task checklists (SPEC-01 to SPEC-06) |
| [Gap Analysis](./gap-analysis.md) | 8 identified gaps, priority matrix, recommended next steps |
| [Source Tree](./source-tree-analysis.md) | Annotated directory structure |

---

## Key Stakeholders

| Role | Person | Responsibility |
|---|---|---|
| Lead Producer / Music Director | Eddie Wilson | Creative Mode calibration, aesthetic judgment, system architecture |
| Platform Target Users | Independent artists, producers, hobbyists | Upload demos, use Creative Modes, hire session musicians |
| Consumer Target Users | General public | Personalized songs for milestones (weddings, memorials) |

---

## Competitive Landscape

| Competitor | What They Do | What Major 72 Adds |
|---|---|---|
| LANDR | AI mastering + distribution | Full creation layer + live integration |
| Suno / Boomy | Fast AI generation | Professional aesthetic guidance |
| Moises.ai | Stem separation + practice | Full production destination |
| SoundBetter | Human session musician marketplace | AI pre-production + direct integration |

---

## Recommended Next Steps

1. Create a **Product Brief** using BMad's `bmad-product-brief` skill
2. Define the **MVP scope** (Core Engine + Eddie Signature Mode)
3. Model **unit economics** (GPU cost per track)
4. Run **user validation** interviews (3 personas, 10-15 interviews)
5. Create a **Solution Architecture** document
6. Build a **proof of concept** (upload → separate → apply mode → export)
