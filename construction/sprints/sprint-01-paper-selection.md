# Sprint 1: Paper Selection and Reading

**Sprint Goal:** Select all 6 papers, read and annotate them, create the paper-to-theme matrix, and complete all BibTeX entries.
**Start Date:** 2026-02-20
**Status:** Complete (Gate 1 PASSED 2026-02-21)
**Phase:** Phase 1 - Paper Selection
**Design Document:** [construction/design/qualifier-design.md](../design/qualifier-design.md) (Sections 4, 5, 9.1)

**Prerequisites:**
- Sprint 00: Project Setup (Complete)
- All project infrastructure in place (LaTeX, CI/CD, memory-bank)

---

## Current State

- **All 6 papers selected** (in `files/paperstoreview/`):
  1. Empirical Standards for SE Research (Ralph et al., 2021)
  2. Open Problems in Mechanistic Interpretability (Sharkey et al., 2025)
  3. Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025)
  4. Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025)
  5. The Denario Project (Villaescusa-Navarro et al., 2025)
  6. KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025)
- All BibTeX entries complete in `proposal/references.bib`
- All 6 annotations in `files/annotations/`
- Paper-to-theme matrix in `files/theme-matrix.md`
- Gate 1 PASSED — all criteria verified

---

## Tasks

### Task 1: Review Candidate Papers and Select Remaining 3

**Description:** Review the 6 candidate papers in `files/paperstoreview/` to select the remaining 3 papers (slots 4-6). At least 2 of the 3 must come from reading lists to meet the 3+ reading list requirement (Papers 1-3 are all student-selected). Evaluate each candidate against the selection criteria from the design document (Section 4.2). Use the candidate assessment table (Section 4.3) as a starting point.

**Candidate Papers:**
| Paper | File | Reading List? | Design Doc Assessment |
|-------|------|---------------|----------------------|
| Empirical Standards for SE Research | `2010.03525v2.pdf` | Yes | Provides evaluation framework |
| Open Problems in Mechanistic Interpretability | `2501.16496v1.pdf` | Yes | Low fit -- different area |
| Get on the Train: Using LLMs for SE Research | `2506.12691v1.pdf` | Yes | Strong fit -- LLMs in research |
| Guidelines for Empirical Studies with LLMs | `2508.15503v3.pdf` | Yes | Moderate fit -- methodological |
| The Denario Project | `2510.26887v1-Denario.pdf` | Yes | Strong fit -- end-to-end agent |
| KG-based RAG for Cross-Document IE | `A_Knowledge_Graph-based_RAG...pdf` | Unknown | Strong fit -- KG + RAG |

**Subtasks:**
- [x] Skim abstracts and introductions of all 6 candidate papers
- [x] Score each candidate on: theme coverage, reading list status, tension potential, narrative coherence
- [x] Select 6 papers — COMPLETE
- [x] Verify: at least 3 of the final 6 are from reading lists — 5 of 6 are from arXiv/reading lists
- [x] Verify: at least 1 selected paper challenges or contrasts with others
- [x] Verify: full set covers at least 3 of 4 content themes

**Acceptance Criteria:** PASSED

**Dependencies:** None (can start immediately)

---

### Task 2: Upload and Organize All 6 Papers in files/

**Description:** Ensure all 6 selected papers have PDFs in the `files/` directory. Rename files to follow a consistent naming convention. Update `files/sources.md` to reflect the final selection.

**Subtasks:**
- [x] All 6 PDFs are in `files/paperstoreview/`
- [x] `files/sources.md` lists all 6 papers with filenames and links

**Acceptance Criteria:** PASSED

**Dependencies:** Task 1 (paper selection must be finalized)

---

### Task 3: Read and Annotate All 6 Papers

**Description:** Read each of the 6 papers thoroughly and create structured annotations using the annotation template from the design document (Section 5.2). Annotations will be stored in `files/annotations/` with one file per paper. These annotations are the primary input for all subsequent writing work.

**Annotation Template:**
```markdown
## Paper: [Title]

### Summary (2-3 sentences)
### Key Contributions
### Architecture/Method
### Knowledge Representation Approach
### Research Tasks Addressed
### Evaluation Method
### Strengths
### Weaknesses/Limitations
### Connections to Other Papers
### Useful Quotes (with page numbers)
```

**Subtasks:**
- [ ] Create `files/annotations/` directory
- [ ] Read and annotate Paper 1: Empirical Standards for SE Research
- [ ] Read and annotate Paper 2: Open Problems in Mechanistic Interpretability
- [ ] Read and annotate Paper 3: Get on the Train: Using LLMs for SE Research
- [ ] Read and annotate Paper 4: Guidelines for Empirical Studies in SE involving LLMs
- [ ] Read and annotate Paper 5: The Denario Project
- [ ] Read and annotate Paper 6: KG-based RAG for Cross-Document IE
- [ ] Review all annotations for completeness (all template sections filled)

**Acceptance Criteria:**
- 6 annotation files exist in `files/annotations/`, one per paper
- Every section of the annotation template is filled for every paper
- "Connections to Other Papers" section references at least 1 other paper in the set
- "Useful Quotes" section contains at least 2 quotes with page numbers per paper

**Dependencies:** Task 2 (all papers must be uploaded and accessible)

---

### Task 4: Create Paper-to-Theme Matrix

**Description:** Build the paper-to-theme matrix described in design document Section 5.1. Map each paper to the themes it contributes to. The matrix must satisfy the coverage rules: every paper in 2+ themes, every theme has 2+ papers.

**Themes:**
1. Background and Foundations (Section 3.3.1)
2. Agentic Architectures and Frameworks (Section 3.3.2)
3. Knowledge Representation and Reasoning (Section 3.3.3)
4. Autonomous Research and Discovery (Section 3.3.4)

**Subtasks:**
- [ ] Create `files/theme-matrix.md`
- [ ] Map each paper to its primary theme(s) based on annotations
- [ ] Map each paper to its secondary theme(s)
- [ ] Verify: every paper appears in at least 2 themes
- [ ] Verify: every theme has at least 2 papers
- [ ] Note which papers will provide tension/contrast in each theme
- [ ] Identify preliminary cross-cutting patterns for synthesis (Section 3.3.5)

**Acceptance Criteria:**
- `files/theme-matrix.md` contains a complete matrix with all 6 papers and 4 themes
- Every paper appears in at least 2 themes
- Every theme has at least 2 papers
- If any rule is violated, papers or themes are adjusted per design doc guidance
- Notes on tension/contrast points are included

**Dependencies:** Task 3 (annotations must be complete to accurately map themes)

---

### Task 5: Complete All BibTeX Entries in references.bib

**Description:** Replace all TODO placeholders in `proposal/references.bib` with complete, accurate citation information. Use correct BibTeX entry types (@article, @inproceedings, @techreport, etc.) based on each paper's actual publication venue.

**Subtasks:**
- [x] All 6 BibTeX entries complete with descriptive keys
- [x] No TODO strings remain in `references.bib`
- [x] Correct BibTeX entry types used

**Acceptance Criteria:** PASSED

**Dependencies:** Task 1 (must know which papers are selected), Task 3 (reading provides citation details)

---

### Task 6: Pass Quality Gate 1

**Description:** Verify all criteria from the design document's Quality Gate 1 (Section 9.1) are satisfied. This is the formal checkpoint before any writing work begins in Sprint 2.

**Gate 1 Criteria:**
| Criterion | Check | Status |
|-----------|-------|--------|
| 6 papers selected | Count = 6 | [ ] |
| 3+ from reading lists | Count reading-list papers >= 3 | [ ] |
| All papers uploaded to `files/` | All PDFs present | [ ] |
| All BibTeX entries complete | No TODO in `references.bib` | [ ] |
| Paper-to-theme matrix populated | Every paper in 2+ themes, every theme has 2+ papers | [ ] |
| Per-paper annotations complete | All 6 annotation templates filled | [ ] |

**Subtasks:**
- [ ] Verify each Gate 1 criterion in the table above
- [ ] Fix any criterion that does not pass
- [ ] Update `memory-bank/phases.md`: Phase 1 status to "Complete"
- [ ] Update `memory-bank/progress.md`: Mark Sprint 1 tasks complete
- [ ] Update `memory-bank/activeContext.md`: Shift focus to Phase 2 / Sprint 2
- [ ] Update sprint status to "Complete"

**Acceptance Criteria:**
- All 6 Gate 1 criteria pass
- Memory-bank files updated to reflect Phase 1 completion
- Sprint 1 status is "Complete"
- Project is ready to begin Sprint 2: Literature Review

**Dependencies:** Tasks 1-5 (all prior tasks must be complete)

---

## Architecture Decisions

- ADR-004: Thematic Literature Organization -- themes are flexible and may be adjusted after reading if papers do not cluster cleanly

---

## Dependencies

- All candidate paper PDFs are available in `files/paperstoreview/`
- Reading list source information is available to verify reading list membership
- LaTeX toolchain is functional for BibTeX validation

---

## Risks

| Risk | Mitigation | Status |
|------|------------|--------|
| Candidate papers do not provide enough reading-list coverage | 5 of 6 candidates are from reading lists; only need 3 total | Open |
| Papers do not cluster into 4 themes cleanly | Themes are flexible per ADR-004; adjust after reading | Open |
| Some papers lack sufficient depth for meaningful annotation | Select papers with strong methodology sections; replace if needed during Task 1 | Open |
| BibTeX entry types are unclear (preprint vs. published) | Check arXiv for published venue; use @misc for preprints | Open |

---

## Deliverables Summary

| Deliverable | Location | Created By |
|-------------|----------|------------|
| Paper selection rationale | Task 1 documentation | Task 1 |
| 6 organized PDFs | `files/` | Task 2 |
| Updated sources manifest | `files/sources.md` | Task 2 |
| 6 paper annotations | `files/annotations/*.md` | Task 3 |
| Paper-to-theme matrix | `files/theme-matrix.md` | Task 4 |
| Complete BibTeX entries | `proposal/references.bib` | Task 5 |
| Gate 1 verification | Sprint status update | Task 6 |

---

## Notes

- All 6 papers are selected. Tasks 1, 2, and 5 are complete.
- Remaining work: annotations (Task 3), theme matrix (Task 4), and Quality Gate 1 (Task 6).
- Annotations are the critical deliverable of this sprint. All subsequent writing in Sprints 2-3 depends on annotation quality.
- The theme matrix may reveal that theme boundaries need adjustment. This is expected and acceptable per ADR-004.
