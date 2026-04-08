# Source Tree Analysis — Major 72 Studio (Pre-Development)

> Generated: 2026-04-08 | Scan Level: Quick | Status: Pre-Development Planning

---

## Repository Structure

```
Studio-Music/                          # Project root
├── README.md                          # Repository README
│
├── docs/                              # Project knowledge base
│   ├── index.md                       # Master documentation index (AI entry point)
│   ├── strategic-framework.md         # Full strategic vision and market analysis
│   ├── technical-specs.md             # Actionable technical specifications (SPEC-01 to SPEC-06)
│   ├── gap-analysis.md                # Gap analysis, priorities, and recommended next steps
│   ├── project-overview.md            # Project overview and quick reference
│   ├── source-tree-analysis.md        # This file — annotated directory tree
│   ├── project-scan-report.json       # Workflow state file
│   └── Summary_Eddie's What...docx    # Original vision document (placeholder)
│
├── design-artifacts/                  # Design phase outputs (empty — awaiting population)
│   ├── A-Product-Brief/               # Product brief deliverables
│   ├── B-Trigger-Map/                 # User psychology / trigger mapping
│   ├── C-UX-Scenarios/                # UX scenario outlines
│   ├── D-Design-System/               # Design system components and tokens
│   └── E-Development/                 # Development-phase design artifacts
│
├── _bmad-output/                      # BMad workflow outputs (empty — awaiting population)
│   ├── planning-artifacts/            # PRDs, architecture docs, epics
│   ├── implementation-artifacts/      # Story files, sprint plans
│   └── test-artifacts/                # Test plans, QA artifacts
│
├── _bmad/                             # BMad Builder tooling (do not edit manually)
│   ├── _config/                       # Agent/skill manifests
│   ├── bmm/                           # BMad Main Module — config.yaml lives here
│   ├── bmb/                           # BMad Builder Module
│   ├── cis/                           # Creative Innovation Suite
│   ├── core/                          # Core skills (brainstorming, reviews, etc.)
│   ├── gds/                           # Game Dev Suite (installed but not primary)
│   ├── tea/                           # Test Engineering Architecture
│   └── wds/                           # Web Design Suite
│
├── .claude/                           # Claude Code configuration
│   └── skills/                        # Installed skill definitions
│
├── .agents/                           # Agent configuration
└── .gemini/                           # Gemini configuration
```

## Critical Folders

| Folder | Purpose | Current State |
|---|---|---|
| `docs/` | Central knowledge base — all strategic and technical documentation | **Active** — 4 documents |
| `design-artifacts/` | Phased design outputs (Product Brief → Trigger Map → UX → Design System → Dev) | **Empty** — scaffolded |
| `_bmad-output/` | BMad workflow outputs (planning, implementation, test artifacts) | **Empty** — scaffolded |
| `_bmad/` | BMad Builder tooling — skills, agents, workflows | **Installed** — do not edit |

## Entry Points

- **Documentation entry:** `docs/index.md`
- **Strategic vision:** `docs/strategic-framework.md`
- **Technical planning:** `docs/technical-specs.md`
- **BMad configuration:** `_bmad/bmm/config.yaml`

## Notes

- This is a **pre-development** project — no source code, no application entry points
- The `design-artifacts/` folder follows a phased design methodology (A through E)
- Multiple AI tooling frameworks are installed (BMad, Claude, Gemini)
- The project targets a web-based music production platform but has not yet entered development
