# Active Context

**Last Updated:** 2026-03-06

## Current Work Phase

**Sprint 5: Slide Polish** — COMPLETE. All slides polished, images integrated, VT logo added. 33 pages, zero errors.

## Current State

**Project Status:**

- Sprint 1 COMPLETE — Gate 1 PASSED (2026-02-21)
- Sprint 2 COMPLETE — Gate 2 PASSED (2026-02-23)
- Sprint 3 COMPLETE — Gate 3+4 PASSED (all paper sections done, abstract written)
- Sprint 4 COMPLETE — Presentation scaffolded (20 slides, all sections present)
- Sprint 5 COMPLETE — All slides polished, images replacing TikZ, VT logo, Q&A fixed

**Slide Polish Progress (Sprint 5):** COMPLETE

- S02-S11: ✅ All polished (images, notes, layouts)
- S08: ✅ kg_research.jpg (replaced TikZ)
- S09: ✅ agentic_amnesia.jpg (updated image)
- S11: ✅ cross_cutting_gaps.jpg + two-column bullets
- S12-S20: ✅ All polished
- S13b: ✅ problem_extraction.jpg (replaced TikZ)
- S14: ✅ core_innovation.jpg (replaced TikZ)
- VT horizontal logo in frametitle top-right on every slide
- Q&A Page 1 split into two frames (overflow fixed)
- Print-ready PDFs: main_print.pdf, main-notes_print.pdf
- Final: 33 pages, zero errors, zero overfull warnings

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
4. ~~Write conclusion~~ — DONE (Task 6)
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
- Priority: Abstract (Task 7), then polish (Tasks 8-12)
- Proposal aligned with `files/Agentic_Knowledge_Graphs_for_Research_Progression.pdf`
- Three-layer architecture: Knowledge Representation, Automation/Extraction, Agentic Orchestration
- KGs as primary substrate; provenance patterns generalize across representations
- Writing order is STRICT: ~~Proposal~~ -> ~~Introduction~~ -> ~~Conclusion~~ -> Abstract -> Polish
