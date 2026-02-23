# Active Context

**Last Updated:** 2026-02-21

## Current Work Phase

**Sprint 2: Literature Review Writing** (Phase 2)

Sprint 1 is complete — Gate 1 passed. All 6 papers selected, read, annotated, theme matrix built, BibTeX complete. Now beginning Sprint 2: write the ~3 page thematic literature review in `proposal/sections/03-literature-review.tex`.

## Current State

**Project Status:**

- Sprint 1 COMPLETE — Gate 1 PASSED (2026-02-21)
- All 6 papers selected, annotated (`files/annotations/`), theme matrix built (`files/theme-matrix.md`)
- All BibTeX entries complete in `references.bib`
- LaTeX proposal structure in place; section files have TODO placeholders
- Beginning Sprint 2: literature review writing

**Construction Artifacts:**
- Requirements: 50+ functional requirements, 29 acceptance criteria, risk register, verification plan
- Design: Paper architecture, section-by-section content plan, thematic mapping, 5 quality gates
- Sprint 1: Paper Selection and Reading (6 tasks, Quality Gate 1)
- Sprint 2: Literature Review Writing (10 tasks, Quality Gate 2)
- Sprint 3: Research Proposal & Paper Completion (12 tasks, Quality Gates 3-4)
- Sprint 4: Presentation Preparation (14 tasks, Quality Gate 5)

**Paper Selection (6/6 — Complete):**

1. Empirical Standards for Software Engineering Research (Ralph et al., 2021)
2. Open Problems in Mechanistic Interpretability (Sharkey et al., 2025)
3. Get on the Train or be Left on the Station: Using LLMs for SE Research (Trinkenreich et al., 2025)
4. Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025)
5. The Denario Project: Deep Knowledge AI Agents for Scientific Discovery (Villaescusa-Navarro et al., 2025)
6. A Knowledge Graph-based RAG for Cross-Document Information Extraction (Suryawanshi et al., 2025)

## Immediate Next Steps

**Sprint 2 Tasks** (see `construction/sprints/sprint-02-literature-review.md`):

1. Read the Sprint 2 sprint doc for the full task breakdown
2. Begin writing `proposal/sections/03-literature-review.tex` — thematic synthesis (~3 pages)
3. Use `files/annotations/` and `files/theme-matrix.md` as primary inputs
4. Follow theme order from theme matrix: T1 Foundations → T2 Architectures → T3 Knowledge Rep → T4 Autonomous Research
5. Pass Quality Gate 2 when draft is complete

## Recent Decisions

### Decision 1: Documentation Structure
- **Date:** 2026-02-20
- **Decision:** Adopt memory-bank + construction folder from construction-ai-proposal
- **Rationale:** Proven structure for maintaining context across sessions

### Decision 2: IEEE LaTeX with Modular Sections
- **Date:** 2026-02-20
- **Decision:** Use modular LaTeX section files (same pattern as construction-ai-proposal)
- **Rationale:** Easier to edit individual sections, proven workflow

### Decision 3: GitHub Actions CI/CD
- **Date:** 2026-02-20
- **Decision:** Automated PDF build + GitHub Pages deployment on push to main
- **Rationale:** Easy sharing, automated build verification, public URL for committee

### Decision 4: Construction Planning Approach
- **Date:** 2026-02-20
- **Decision:** Created comprehensive requirements, design, and sprint docs covering the full project lifecycle
- **Rationale:** Provides structured execution path with quality gates between phases

## Key Patterns and Preferences

### Writing Patterns
- Synthesize papers by theme, not one-by-one summaries
- Every claim backed by citation
- Research proposal flows from gap analysis
- Write abstract last

### Documentation Patterns
- Update activeContext.md after every significant change
- Keep progress.md current with task completion
- Follow sprint task lists for execution order

## Open Questions

1. **Presentation tool** - Which tool to use for slides? (Deferred to Sprint 4)

## Reference Materials

- Memory Bank: `memory-bank/`
- Construction Requirements: `construction/requirements/qualifier-requirements.md`
- Construction Design: `construction/design/qualifier-design.md`
- Sprint 1 (current): `construction/sprints/sprint-01-paper-selection.md`
- Qualifier Requirements: https://chbrown13.github.io/qualifier.html
- Proposal Source: `proposal/sections/`
- Reference Papers: `files/`

## Notes for Next Session

- Read ALL memory-bank files on context reset
- Check Sprint 1 task list for current progress
- Priority: select remaining papers (Task 1) then read and annotate (Task 3)
- Design doc Section 4.3 has candidate paper assessment to guide selection
