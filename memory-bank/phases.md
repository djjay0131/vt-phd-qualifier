# Phase Lifecycle

**Last Updated:** 2026-02-20

This file serves as the **coordination hub** for tracking project phases and deliverables.

**Design Document:** [construction/design/qualifier-design.md](../construction/design/qualifier-design.md) -- comprehensive design covering all phases.
**Requirements:** [construction/requirements/qualifier-requirements.md](../construction/requirements/qualifier-requirements.md) -- 50+ requirements, 29 acceptance criteria.

---

## Phase Registry

| Phase | Status | Sprint | Design Ready | Quality Gate | Key Deliverables |
|-------|--------|--------|-------------|-------------|------------------|
| 0: Project Setup | Complete | Pre-sprint | Yes | N/A | Repo, memory-bank, agents, LaTeX template, CI/CD |
| 1: Paper Selection | Complete | [Sprint 1](../construction/sprints/sprint-01-paper-selection.md) | Yes | Gate 1 ✓ PASSED | 6 selected papers, annotations, theme matrix, BibTeX |
| 2: Literature Review | In Progress | [Sprint 2](../construction/sprints/sprint-02-literature-review.md) | Yes | Gate 2 (6 criteria) | ~3 page thematic synthesis |
| 3: Research Proposal | Not Started | [Sprint 3](../construction/sprints/sprint-03-proposal-and-completion.md) | Yes | Gate 3 (4 criteria) | ~1 page proposal from gap analysis |
| 4: Paper Completion | Not Started | [Sprint 3](../construction/sprints/sprint-03-proposal-and-completion.md) | Yes | Gate 4 (9 criteria) | Full 5-6 page IEEE paper, published |
| 5: Presentation | Not Started | [Sprint 4](../construction/sprints/sprint-04-presentation.md) | Yes | Gate 5 (5 criteria) | 15-min oral presentation |

### Status Legend

- **Not Started**: Phase not yet begun
- **In Progress**: Active work underway
- **Review**: Awaiting review or feedback
- **Complete**: Phase fully finished

---

## Phase Details

### Phase 0: Project Setup

- **Objective**: Set up project structure, LaTeX template, and CI/CD pipeline
- **Key Deliverables**: Repository, memory-bank, agents, proposal template, GitHub Actions
- **Completion Date**: 2026-02-20
- **Notes**: Adapted from construction-ai-proposal project. IEEE conference format.

### Phase 1: Paper Selection

- **Objective**: Select all 6 papers, read and annotate, build theme matrix
- **Sprint**: [Sprint 1: Paper Selection and Reading](../construction/sprints/sprint-01-paper-selection.md) (6 tasks)
- **Quality Gate**: Gate 1 -- 6 papers selected, 3+ from reading lists, all annotated, theme matrix populated, BibTeX complete
- **Key Deliverables**:
  - 6 papers selected (3+ from reading lists)
  - All papers read and annotated (`files/annotations/`)
  - Paper-to-theme matrix (`files/theme-matrix.md`)
  - Complete `references.bib` entries
- **Status**: Complete — Gate 1 PASSED (2026-02-21)
- **Papers Selected**:
  1. Empirical Standards for SE Research (Ralph et al., 2021)
  2. Open Problems in Mechanistic Interpretability (Sharkey et al., 2025)
  3. Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025)
  4. Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025)
  5. The Denario Project (Villaescusa-Navarro et al., 2025)
  6. KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025)

### Phase 2: Literature Review

- **Objective**: Write ~3 page thematic synthesis of all 6 papers
- **Sprint**: [Sprint 2: Literature Review Writing](../construction/sprints/sprint-02-literature-review.md) (10 tasks)
- **Quality Gate**: Gate 2 -- all 5 subsections drafted, all 6 papers cited 2+ times, 3+ synthesis patterns used, 2-3 gaps identified, ~3 pages, clean compilation
- **Key Deliverables**:
  - Literature assessment organized by theme (5 subsections)
  - Gap analysis identifying open problems
  - All 6 papers cited meaningfully
- **Status**: Not Started

### Phase 3: Research Proposal

- **Objective**: Write ~1 page research proposal extending the surveyed work
- **Sprint**: [Sprint 3: Research Proposal & Paper Completion](../construction/sprints/sprint-03-proposal-and-completion.md) (Tasks 1-4)
- **Quality Gate**: Gate 3 -- problem references gaps, approach is concrete, contributions map to gaps, ~1 page
- **Key Deliverables**:
  - Problem statement grounded in literature gaps
  - Proposed approach and methodology
  - Expected contributions
- **Status**: Not Started

### Phase 4: Paper Completion

- **Objective**: Complete full paper with introduction, abstract, conclusion, and polish
- **Sprint**: [Sprint 3: Research Proposal & Paper Completion](../construction/sprints/sprint-03-proposal-and-completion.md) (Tasks 5-12)
- **Quality Gate**: Gate 4 -- all sections complete, 150-200 word abstract, 5-6 pages, all citations resolve, coherent argument arc, published to GitHub Pages
- **Key Deliverables**:
  - Introduction (~0.5-0.75 pages)
  - Abstract (~150-200 words)
  - Conclusion
  - Full paper: 5-6 pages, IEEE format
  - Published to GitHub Pages
- **Status**: Not Started

### Phase 5: Presentation

- **Objective**: Prepare 15-minute oral presentation
- **Sprint**: [Sprint 4: Presentation Preparation](../construction/sprints/sprint-04-presentation.md) (14 tasks)
- **Quality Gate**: Gate 5 -- 13-14 slides complete, rehearsal fits in 15 min, 3+ backup Q&A slides, narrative matches paper
- **Key Deliverables**:
  - Presentation slides (14 slides, 15 min + 5 min Q&A)
  - Backup slides for anticipated questions
  - Speaker notes and rehearsal
- **Status**: Not Started

---

## Sprint-to-Phase Mapping

| Sprint | Phases Covered | Tasks | Quality Gates |
|--------|---------------|-------|---------------|
| Sprint 1 | Phase 1 | 6 tasks | Gate 1 |
| Sprint 2 | Phase 2 | 10 tasks | Gate 2 |
| Sprint 3 | Phases 3 + 4 | 12 tasks | Gates 3 + 4 |
| Sprint 4 | Phase 5 | 14 tasks | Gate 5 |

---

## Document Structure (Current)

```text
vt-phd-qualifier/
├── README.md
├── CLAUDE.md
├── .github/workflows/build-and-publish-pdf.yml
├── .claude/agents/
├── memory-bank/
├── construction/
│   ├── README.md
│   ├── requirements/
│   │   └── qualifier-requirements.md
│   ├── design/
│   │   └── qualifier-design.md
│   └── sprints/
│       ├── sprint-01-paper-selection.md
│       ├── sprint-02-literature-review.md
│       ├── sprint-03-proposal-and-completion.md
│       └── sprint-04-presentation.md
├── files/                     # Reference papers
│   ├── Agentic_Knowledge_Graphs_for_Research_Progression.pdf
│   ├── Research4Agents (4).pdf
│   └── paperstoreview/        # Candidate papers for selection
└── proposal/
    ├── main.tex               # IEEE conference paper
    ├── references.bib
    └── sections/
        ├── 01-abstract.tex
        ├── 02-introduction.tex
        ├── 03-literature-review.tex
        ├── 04-research-proposal.tex
        └── 05-conclusion.tex
```

---

## Cross-Reference Index

### Memory-Bank File Purposes

| File | Primary Purpose | Update Frequency |
|------|-----------------|------------------|
| projectbrief.md | Qualifier requirements & objectives | Rarely |
| productContext.md | Research area context | Occasionally |
| techContext.md | LaTeX setup & tools | As needed |
| systemPatterns.md | Paper structure & writing patterns | As approach evolves |
| activeContext.md | Current work state | Every session |
| progress.md | Task tracking | After each milestone |
| phases.md | Phase coordination | On phase changes |
| architecturalDecisions.md | Key decisions | When decisions made |

---

## Notes

- Update this file whenever phase status changes
- Check this file at session start for current status
- Sprint docs in `construction/sprints/` contain detailed task breakdowns and acceptance criteria
- Quality gates must pass before advancing to the next sprint
- References do NOT count toward the 5-6 page limit
