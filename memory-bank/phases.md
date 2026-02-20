# Phase Lifecycle

**Last Updated:** 2026-02-20

This file serves as the **coordination hub** for tracking project phases and deliverables.

---

## Phase Registry

| Phase | Status | Key Deliverables | Target Date |
|-------|--------|------------------|-------------|
| 0: Project Setup | Complete | Repo, memory-bank, agents, LaTeX template, CI/CD | 2026-02-20 |
| 1: Paper Selection | In Progress | 6 selected papers, thematic outline | TBD |
| 2: Literature Review | Not Started | ~3 page synthesis of 6 papers | TBD |
| 3: Research Proposal | Not Started | ~1 page proposal extending surveyed work | TBD |
| 4: Paper Completion | Not Started | Full 5-6 page IEEE paper, polished | TBD |
| 5: Presentation | Not Started | 15-min oral presentation | TBD |

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

- **Objective**: Select all 6 papers and create thematic outline
- **Target**: TBD
- **Key Deliverables**:
  - 6 papers selected (3+ from reading lists)
  - All papers read and annotated
  - Thematic outline for literature review
  - Complete `references.bib` entries
- **Status**: In Progress (2/6 papers uploaded)
- **Papers Selected**:
  1. Agentic Knowledge Graphs for Research Progression
  2. Research4Agents
  3-6. TBD

### Phase 2: Literature Review

- **Objective**: Write ~3 page synthesis of all 6 papers
- **Target**: TBD
- **Key Deliverables**:
  - Literature assessment organized by theme
  - Gap analysis identifying open problems
  - All 6 papers cited meaningfully
- **Status**: Not Started

### Phase 3: Research Proposal

- **Objective**: Write ~1 page research proposal extending the surveyed work
- **Target**: TBD
- **Key Deliverables**:
  - Problem statement grounded in literature gaps
  - Proposed approach and methodology
  - Expected contributions
- **Status**: Not Started

### Phase 4: Paper Completion

- **Objective**: Complete full paper with introduction, abstract, conclusion, and polish
- **Target**: TBD
- **Key Deliverables**:
  - Introduction (~0.5-0.75 pages)
  - Abstract (~150-200 words)
  - Conclusion
  - Full paper: 5-6 pages, IEEE format
  - Published to GitHub Pages
- **Status**: Not Started

### Phase 5: Presentation

- **Objective**: Prepare 15-minute oral presentation
- **Target**: TBD
- **Key Deliverables**:
  - Presentation slides (15 min + 5 min Q&A)
  - High-level takeaways, research overview, future directions
- **Status**: Not Started

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
├── files/                     # Reference papers
│   ├── Agentic_Knowledge_Graphs_for_Research_Progression.pdf
│   └── Research4Agents (4).pdf
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
- References do NOT count toward the 5-6 page limit
