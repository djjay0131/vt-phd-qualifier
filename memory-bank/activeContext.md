# Active Context

**Last Updated:** 2026-02-24

## Current Work Phase

**Sprint 3: Research Proposal & Paper Completion** (Phases 3-4)

Sprint 3 Tasks 1-5 complete. Research proposal and introduction written. Gate 3 passed (page count deferred to polish). Next: Conclusion (Task 6).

## Current State

**Project Status:**

- Sprint 1 COMPLETE — Gate 1 PASSED (2026-02-21)
- Sprint 2 COMPLETE — Gate 2 PASSED (2026-02-23)
- Sprint 3 Tasks 1-5 COMPLETE — Proposal, Gate 3, and Introduction done (2026-02-24)
- Introduction in `proposal/sections/02-introduction.tex` (~0.5 pages, all 6 papers cited)
- Literature review in `proposal/sections/03-literature-review.tex` (~2 pages)
- Research proposal in `proposal/sections/04-research-proposal.tex` (~1.5 pages)
- Proposal: "agentic knowledge graphs for research progression" — provenance-first, three-layer architecture
- KG is primary substrate but provenance-enforcement patterns generalize across representations
- Remaining sections: conclusion, abstract still have TODO placeholders
- Gate 3 passed (6/7, page count flag deferred to polish phase Task 9)

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

**Sprint 3 Tasks** (see `construction/sprints/sprint-03-proposal-and-completion.md`):

1. ~~Write research proposal~~ — DONE (Tasks 1-3)
2. ~~Pass Quality Gate 3~~ — PASSED with page count deferred (Task 4)
3. ~~Write introduction~~ — DONE (Task 5)
4. Write conclusion (Task 6)
5. Write abstract (150-200 words) (Task 7)
6. Polish, verify, publish (Tasks 8-12)
7. Pass Quality Gate 4

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
- Check Sprint 3 task list for current progress
- Priority: Conclusion (Task 6), then Abstract (Task 7)
- Proposal aligned with `files/Agentic_Knowledge_Graphs_for_Research_Progression.pdf`
- Three-layer architecture: Knowledge Representation, Automation/Extraction, Agentic Orchestration
- KGs as primary substrate; provenance patterns generalize across representations
- Design doc Section 3.5 has content plan for conclusion
- Writing order is STRICT: ~~Proposal~~ -> ~~Introduction~~ -> Conclusion -> Abstract -> Polish
