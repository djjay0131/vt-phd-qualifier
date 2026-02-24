# Sprint 2: Literature Review Writing

**Sprint Goal:** Write the ~3 page literature assessment (Section III) organized by theme, synthesizing all 6 papers.
**Phase:** Phase 2 - Literature Review
**Start Date:** 2026-02-23
**Status:** Complete — Gate 2 PASSED (2026-02-23)

**Prerequisites:**
- Sprint 1 complete (Quality Gate 1 passed)
- All 6 paper annotations finalized
- Paper-to-theme matrix populated
- All BibTeX entries complete in `proposal/references.bib`

**Design Reference:** [construction/design/qualifier-design.md](../design/qualifier-design.md) -- Sections 3.3, 5.3, 8.1, 9.2

**Output File:** `proposal/sections/03-literature-review.tex`

---

## Input Artifacts (from Sprint 1)

| Artifact | Location | Required State |
|----------|----------|----------------|
| Paper annotations (6) | TBD (annotation files) | All 6 templates filled per Section 5.2 of design doc |
| Paper-to-theme matrix | TBD | Every paper in 2+ themes, every theme has 2+ papers |
| BibTeX entries | `proposal/references.bib` | All 6 entries complete, no TODOs |
| LaTeX section file | `proposal/sections/03-literature-review.tex` | Has subsection structure with TODO placeholders |

---

## Writing Dependency Order

Tasks must be completed in the following order. Tasks marked as parallelizable may be worked on simultaneously.

```
Task 1: Review Inputs & Plan
    |
    v
Task 2: Background & Foundations (3.3.1)
    |
    +---> Task 3: Agentic Architectures (3.3.2)  --+
    |                                               |  (parallel)
    +---> Task 4: Knowledge Representation (3.3.3) -+
    |
    v
Task 5: Autonomous Research (3.3.4)   [depends on Tasks 3 & 4]
    |
    v
Task 6: Synthesis & Gap Analysis (3.3.5)   [depends on Tasks 2-5]
    |
    v
Task 7: Compilation & Page Count Check
    |
    v
Task 8: Synthesis Pattern Audit
    |
    v
Task 9: Citation Coverage Audit
    |
    v
Task 10: Quality Gate 2 Validation
```

---

## Tasks

### Task 1: Review Input Artifacts and Plan Subsection Content

**Description:** Before writing, review all 6 paper annotations and the paper-to-theme matrix. For each subsection, identify which papers contribute, what synthesis patterns apply, and draft a paragraph-level outline.

- [ ] Review all 6 paper annotations
- [ ] Review paper-to-theme matrix
- [ ] For each subsection (3.3.1 through 3.3.5), list which papers contribute
- [ ] Identify at least 3 synthesis patterns to use across the section (Agreement, Contrast, Extension, Tension, Gap, Cluster)
- [ ] Draft a paragraph-level outline for each subsection noting which papers appear where

**Acceptance Criteria:**
- Every paper is assigned to at least 2 subsections
- Every subsection has at least 2 papers assigned
- At least 3 distinct synthesis patterns are planned for use
- Outline exists before any prose writing begins

---

### Task 2: Write Background and Foundations (Section 3.3.1, ~0.5 pages)

**Description:** Establish the shared conceptual ground all 6 papers build upon. Define foundational concepts and set up the vocabulary used throughout the review.

- [ ] Define LLM-based agents and their capabilities
- [ ] Define tool use in the context of LLM agents
- [ ] Define knowledge graphs and their role in research
- [ ] Define retrieval-augmented generation (RAG)
- [ ] Explain why these building blocks matter for research automation
- [ ] Cite all 6 papers at least once in this subsection
- [ ] Replace the TODO placeholder in `\subsection{Background and Foundations}`

**Acceptance Criteria:**
- All 4 foundational concepts defined (agents, tool use, KGs, RAG)
- All 6 papers cited at least once
- Subsection reads as context-setting, not as paper summaries
- Length approximately 0.5 pages
- Key question answered: "What does the reader need to know before understanding the surveyed work?"

---

### Task 3: Write Agentic Architectures and Frameworks (Section 3.3.2, ~0.75 pages)

**Note:** Can be written in parallel with Task 4.

**Description:** Compare and contrast how the surveyed papers design agents and multi-agent systems. Focus on architectural patterns, design trade-offs, and evaluation criteria.

- [ ] Compare architectural patterns: single-agent vs. multi-agent, role specialization, coordination mechanisms
- [ ] Identify which papers propose frameworks vs. which use existing ones
- [ ] Analyze design trade-offs: autonomy vs. control, specialization vs. generality
- [ ] Note evaluation criteria papers use for their architectures
- [ ] Use at least 1 synthesis pattern (e.g., Contrast for comparing architectural approaches)
- [ ] Replace the TODO placeholder in `\subsection{Agentic Architectures and Frameworks}`

**Acceptance Criteria:**
- At least 2 papers compared on architectural patterns
- Trade-offs explicitly stated (not just described)
- At least 1 synthesis pattern used (Contrast or Agreement recommended)
- Length approximately 0.75 pages
- Key question answered: "How do researchers structure agentic systems for research tasks, and what trade-offs do they make?"

---

### Task 4: Write Knowledge Representation and Reasoning (Section 3.3.3, ~0.75 pages)

**Note:** Can be written in parallel with Task 3.

**Description:** Examine how agents acquire, store, and reason over structured knowledge. Compare knowledge representation approaches and analyze how retrieval integrates with reasoning.

- [ ] Compare knowledge representation approaches: knowledge graphs, vector stores, hybrid
- [ ] Analyze RAG patterns and graph traversal strategies across papers
- [ ] Discuss the role of structured vs. unstructured knowledge
- [ ] Identify how knowledge representation enables or limits agent capabilities
- [ ] Use at least 1 synthesis pattern (e.g., Cluster for grouping similar approaches)
- [ ] Replace the TODO placeholder in `\subsection{Knowledge Representation and Reasoning}`

**Acceptance Criteria:**
- At least 2 papers compared on knowledge representation
- Both structured and unstructured approaches discussed
- Limitations of current approaches noted (feeds into gap analysis)
- At least 1 synthesis pattern used
- Length approximately 0.75 pages
- Key question answered: "How do agents manage the knowledge they need for research, and what are the limitations?"

---

### Task 5: Write Autonomous Research and Discovery (Section 3.3.4, ~0.5 pages)

**Dependencies:** Tasks 3 and 4 must be complete before starting this task.

**Description:** Examine the end-to-end research workflows that agents perform. Build on architectural and knowledge representation discussions from previous subsections.

- [ ] Describe research tasks agents automate: literature review, hypothesis generation, experiment design, knowledge synthesis
- [ ] Compare scope of autonomy across papers: fully autonomous vs. human-in-the-loop
- [ ] Assess how papers evaluate research quality and output
- [ ] Note which research domains are covered vs. missing
- [ ] Use at least 1 synthesis pattern (e.g., Extension or Gap)
- [ ] Replace the TODO placeholder in `\subsection{Autonomous Research and Discovery}`

**Acceptance Criteria:**
- At least 2 papers compared on research capabilities
- Autonomy spectrum discussed (not binary autonomous/not)
- Evaluation approaches noted (feeds into gap analysis)
- At least 1 synthesis pattern used
- Length approximately 0.5 pages
- Key question answered: "What can research agents actually do today, and how well do they do it?"

---

### Task 6: Write Synthesis and Gap Analysis (Section 3.3.5, ~0.5 pages)

**Dependencies:** Tasks 2, 3, 4, and 5 must ALL be complete before starting this task. This subsection is the bridge to the research proposal.

**Description:** Tie all themes together, surface cross-cutting patterns, and identify the gaps that motivate the research proposal. This is the most critical subsection -- it must make the proposal feel inevitable.

- [ ] Identify 2-3 cross-cutting themes that span multiple subsections (3.3.1-3.3.4)
- [ ] Surface tensions or contradictions between papers
- [ ] Identify 2-3 concrete, specific gaps that no paper addresses adequately
- [ ] Rank gaps by significance and tractability
- [ ] Ensure the primary gap directly motivates the planned research proposal
- [ ] Use Gap and/or Tension synthesis patterns
- [ ] Replace the TODO placeholder in `\subsection{Synthesis and Gap Analysis}`

**Acceptance Criteria:**
- 2-3 cross-cutting themes identified and discussed
- At least 1 tension or contradiction surfaced
- 2-3 concrete gaps identified (not vague hand-waving)
- Gaps ranked by significance
- Primary gap is clearly stated and will motivate the research proposal (Section IV)
- Length approximately 0.5 pages
- Key question answered: "What is missing from the current landscape, and what should be built next?"

---

### Task 7: Compilation and Page Count Verification

**Dependencies:** Tasks 2-6 complete (all subsections written).

**Description:** Compile the full LaTeX document and verify the literature review section meets page budget requirements.

- [ ] Run `latexmk` (or equivalent) to compile `proposal/main.tex`
- [ ] Verify no LaTeX errors or warnings
- [ ] Verify all `\cite{}` commands resolve (no `[?]` in output)
- [ ] Verify all `\label{}` and `\ref{}` commands resolve
- [ ] Measure literature review section page count in compiled PDF
- [ ] Confirm page count is within 2.75-3.25 pages

**Acceptance Criteria:**
- LaTeX compiles cleanly with zero errors
- No unresolved citations (`[?]`) in compiled output
- Literature review section is 2.75-3.25 pages
- If outside range: adjust content (trim Background first if over, expand Synthesis if under)

---

### Task 8: Synthesis Pattern Audit

**Dependencies:** Task 7 passes (document compiles).

**Description:** Review the written literature review to verify sufficient synthesis quality. This is not a summary paper -- every subsection must weave multiple papers together.

- [ ] Identify and count distinct synthesis patterns used across all subsections
- [ ] Verify at least 3 different patterns from: Agreement, Contrast, Extension, Tension, Gap, Cluster
- [ ] Verify no subsection reads as a standalone paper summary (independence test)
- [ ] Verify every subsection references at least 2 papers in comparative or connective language
- [ ] Flag any paragraph that discusses only a single paper without connecting to others

**Acceptance Criteria:**
- At least 3 distinct synthesis patterns used across the section
- No subsection is a single-paper summary
- Every paragraph connects multiple papers or builds on a multi-paper discussion
- Flagged issues resolved before proceeding

---

### Task 9: Citation Coverage Audit

**Dependencies:** Task 7 passes (document compiles).

**Description:** Verify that all 6 papers are cited adequately and distributed across the literature review.

- [ ] Count `\cite{}` appearances for each of the 6 papers
- [ ] Verify each paper appears in `\cite{}` at least twice across the section
- [ ] Verify each paper appears in at least 2 different subsections
- [ ] Verify Background & Foundations (3.3.1) cites all 6 papers
- [ ] Verify no paper is over-cited to the point of dominating the narrative

**Acceptance Criteria:**
- Each of the 6 papers cited at least twice
- Each paper appears in at least 2 subsections
- All 6 papers cited in Background & Foundations
- Citation distribution is balanced (no paper has more than 40% of total citations)

---

### Task 10: Quality Gate 2 Validation

**Dependencies:** Tasks 7, 8, and 9 all pass.

**Description:** Final validation against Quality Gate 2 criteria from the design document (Section 9.2). All criteria must pass before Sprint 2 is marked complete.

- [ ] **All 5 subsections drafted:** No TODO placeholders remain in `03-literature-review.tex`
- [ ] **All 6 papers cited:** Each paper appears in `\cite{}` at least twice
- [ ] **Synthesis patterns:** At least 3 different synthesis moves used
- [ ] **Gap analysis:** 2-3 concrete, specific gaps identified
- [ ] **Page count:** ~3 pages (2.75-3.25 acceptable)
- [ ] **LaTeX compiles cleanly:** No errors or warnings
- [ ] **Verification tests pass:**
  - Synthesis test: Literature review conveys landscape without reading original papers
  - Independence test: No subsection readable as standalone paper summary
  - Gap test: Gaps feel inevitable after reading subsections 3.3.1-3.3.4

**Acceptance Criteria:**
- ALL checkboxes above are checked
- Sprint status updated to Complete
- Ready to proceed to Sprint 3 (Research Proposal and Paper Completion)

---

## Architecture Decisions

- ADR-004: Thematic Literature Organization -- literature review organized by theme, not by paper

---

## Dependencies

| Dependency | Source | Status |
|------------|--------|--------|
| 6 paper annotations | Sprint 1 | Not Started |
| Paper-to-theme matrix | Sprint 1 | Not Started |
| Complete BibTeX entries | Sprint 1 / `proposal/references.bib` | Partial (2/6) |
| LaTeX section file with subsection structure | Phase 0 | Complete |
| Design document sections 3.3, 5.3, 8.1, 9.2 | `construction/design/qualifier-design.md` | Complete |

---

## Risks

| Risk | Likelihood | Impact | Mitigation | Status |
|------|-----------|--------|------------|--------|
| Papers do not cluster into themes cleanly | Medium | High | Adjust thematic subsections after reading; themes are flexible per ADR-004 | Open |
| Page budget exceeded (> 3.25 pages) | Medium | Medium | Track page count per subsection during writing; trim Background first | Open |
| Page budget underutilized (< 2.75 pages) | Low | Medium | Expand Synthesis & Gap Analysis or add a comparison table | Open |
| Subsection reads as paper summary instead of synthesis | Medium | High | Use synthesis pattern audit (Task 8); rewrite any flagged paragraphs | Open |
| Gap analysis feels forced or vague | Medium | High | Ground gaps in specific limitations noted during paper reading; gaps must be concrete and citable | Open |
| Primary gap does not naturally motivate a research proposal | Low | High | Revisit gap ranking; adjust primary gap or planned proposal direction | Open |

---

## Synthesis Patterns Reference

Use at least 3 of these patterns across the literature review:

| Pattern | Template | Example Context |
|---------|----------|-----------------|
| **Agreement** | "Both [A] and [B] demonstrate that..." | Papers converge on a finding |
| **Contrast** | "While [A] employs X, [B] takes a different approach with Y..." | Papers diverge on method |
| **Extension** | "[B] extends the work of [A] by adding..." | One paper builds on another |
| **Tension** | "[A] claims X, yet [B]'s findings suggest..." | Papers disagree |
| **Gap** | "Neither [A] nor [B] addresses..." | Identifying what is missing |
| **Cluster** | "Several approaches [A, B, C] share the pattern of..." | Multiple papers align |

---

## Sprint Exit Criteria

Sprint 2 is complete when:

1. All 10 tasks have all subtasks checked off
2. Quality Gate 2 (Task 10) passes with all criteria met
3. `proposal/sections/03-literature-review.tex` contains no TODO placeholders
4. LaTeX compiles cleanly
5. Literature review is 2.75-3.25 pages in compiled PDF

**On completion:**
- Update `memory-bank/phases.md`: Phase 2 status to "Complete"
- Update `memory-bank/progress.md`: M2 milestone to "Complete"
- Update `memory-bank/activeContext.md`: Current focus to Phase 3
- Sprint 3 (Research Proposal and Paper Completion) is ready to begin
