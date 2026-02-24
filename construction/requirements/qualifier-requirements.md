# VT PhD Qualifier - Comprehensive Requirements

**Document ID:** REQ-001
**Status:** Complete
**Created:** 2026-02-20
**Last Updated:** 2026-02-20

---

## 1. Overview

This document defines the complete requirements for the Virginia Tech PhD qualifying examination. The qualifier has two deliverables: a written IEEE conference paper and an oral presentation. The research topic is **Agentic AI for Autonomous Research**, surveying 6 selected papers and proposing research extending the surveyed work.

**Source of Requirements:** https://chbrown13.github.io/qualifier.html

---

## 2. Functional Requirements

### 2.1 Paper Selection (FR-SEL)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-SEL-01 | Select exactly 6 research papers relevant to Agentic AI for Autonomous Research | Must | Partial (2/6) |
| FR-SEL-02 | At least 3 of the 6 papers must come from the provided reading lists | Must | Unknown (reading list source TBD) |
| FR-SEL-03 | Papers must form a coherent body of work that supports thematic synthesis | Must | Not Started |
| FR-SEL-04 | Papers should span the key themes: agentic architectures, knowledge representation, autonomous research, and foundations | Should | Not Started |
| FR-SEL-05 | Each paper must be available as a PDF for reading and annotation | Must | Partial (2/6 uploaded) |
| FR-SEL-06 | Complete BibTeX entries must be created for all 6 papers in `references.bib` | Must | Partial (2/6 with TODOs) |

**Current State:**
- Paper 1: Agentic Knowledge Graphs for Research Progression (selected, uploaded)
- Paper 2: Research4Agents (selected, uploaded)
- Papers 3-6: Not yet selected

### 2.2 Written Component - IEEE Conference Paper (FR-PAP)

#### 2.2.1 Abstract (FR-PAP-ABS)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-PAP-ABS-01 | Write an abstract of 150-200 words | Must | Not Started |
| FR-PAP-ABS-02 | Abstract must cover: problem area, scope of survey, key findings, proposed research direction | Must | Not Started |
| FR-PAP-ABS-03 | Abstract must be self-contained and understandable without reading the full paper | Must | Not Started |
| FR-PAP-ABS-04 | Abstract must be written LAST, after all other sections are complete | Should | Not Started |

**File:** `proposal/sections/01-abstract.tex`

#### 2.2.2 Introduction (FR-PAP-INT)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-PAP-INT-01 | Introduction must be approximately 0.5-0.75 pages | Must | Not Started |
| FR-PAP-INT-02 | Motivate the research area of agentic AI and autonomous research agents | Must | Not Started |
| FR-PAP-INT-03 | Define key terms and establish scope of the survey | Must | Not Started |
| FR-PAP-INT-04 | State the purpose of the literature survey | Must | Not Started |
| FR-PAP-INT-05 | Preview the structure of the paper (section roadmap) | Must | Not Started |
| FR-PAP-INT-06 | Connect the survey to the student's research interests | Should | Not Started |

**File:** `proposal/sections/02-introduction.tex`

#### 2.2.3 Literature Assessment (FR-PAP-LIT)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-PAP-LIT-01 | Literature assessment must be approximately 3 pages | Must | Not Started |
| FR-PAP-LIT-02 | Organize by THEME, not paper-by-paper (see ADR-004) | Must | Not Started |
| FR-PAP-LIT-03 | All 6 selected papers must be cited meaningfully (not just listed) | Must | Not Started |
| FR-PAP-LIT-04 | Identify connections between papers (shared methods, complementary ideas) | Must | Not Started |
| FR-PAP-LIT-05 | Identify tensions between papers (conflicting claims, different approaches) | Must | Not Started |
| FR-PAP-LIT-06 | Surface gaps in the literature (what no paper addresses, unsolved problems) | Must | Not Started |
| FR-PAP-LIT-07 | Gap analysis must directly set up the research proposal section | Must | Not Started |
| FR-PAP-LIT-08 | Use comparative language linking papers (e.g., "While [X] proposes..., [Y] takes a different approach...") | Should | Not Started |
| FR-PAP-LIT-09 | Cluster related citations where appropriate (e.g., "Several works address this \cite{a, b, c}") | Should | Not Started |
| FR-PAP-LIT-10 | Every factual claim must be backed by a citation | Must | Not Started |

**Planned Thematic Subsections (adjustable after paper selection):**
1. Background and Foundations
2. Agentic Architectures and Frameworks
3. Knowledge Representation and Reasoning
4. Autonomous Research and Discovery
5. Synthesis and Gap Analysis

**File:** `proposal/sections/03-literature-review.tex`

#### 2.2.4 Research Proposal (FR-PAP-PRO)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-PAP-PRO-01 | Research proposal must be approximately 1 page | Must | Not Started |
| FR-PAP-PRO-02 | Include a clear problem statement grounded in the literature gaps from Section III | Must | Not Started |
| FR-PAP-PRO-03 | Describe the proposed approach and methodology | Must | Not Started |
| FR-PAP-PRO-04 | List expected contributions and their significance | Must | Not Started |
| FR-PAP-PRO-05 | Each contribution must trace back to a specific gap identified in the literature review | Must | Not Started |
| FR-PAP-PRO-06 | Proposal must be concrete and specific (what would you build, study, or prove?) | Must | Not Started |
| FR-PAP-PRO-07 | Proposal must be feasible within a PhD research program | Should | Not Started |
| FR-PAP-PRO-08 | Connect proposed approach to strengths of the surveyed work | Should | Not Started |

**File:** `proposal/sections/04-research-proposal.tex`

#### 2.2.5 Conclusion (FR-PAP-CON)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-PAP-CON-01 | Conclusion must be approximately 0.25 pages | Must | Not Started |
| FR-PAP-CON-02 | Summarize key takeaways from the literature survey | Must | Not Started |
| FR-PAP-CON-03 | Restate the proposed research direction | Must | Not Started |
| FR-PAP-CON-04 | Connect to broader impact and future work | Should | Not Started |

**File:** `proposal/sections/05-conclusion.tex`

#### 2.2.6 References (FR-PAP-REF)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-PAP-REF-01 | Include complete, accurate BibTeX entries for all 6 selected papers | Must | Partial |
| FR-PAP-REF-02 | Include additional supporting references as needed | Should | Not Started |
| FR-PAP-REF-03 | All citations in the text must resolve to entries in `references.bib` | Must | Not Started |
| FR-PAP-REF-04 | Use IEEE citation style (numeric, bracketed) | Must | Configured |
| FR-PAP-REF-05 | No orphan citations (every bib entry must be cited in the text) | Should | Not Started |

**File:** `proposal/references.bib`

### 2.3 Oral Presentation (FR-ORA)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| FR-ORA-01 | Prepare a 15-minute slide-based presentation | Must | Not Started |
| FR-ORA-02 | Prepare for 5 minutes of Q&A from the committee | Must | Not Started |
| FR-ORA-03 | Cover the same content as the paper at a higher level of abstraction | Must | Not Started |
| FR-ORA-04 | Include high-level takeaways from the literature survey | Must | Not Started |
| FR-ORA-05 | Present an overview of the research area and its importance | Must | Not Started |
| FR-ORA-06 | Discuss lessons learned and connections across the surveyed papers | Must | Not Started |
| FR-ORA-07 | Present future research directions (connected to the proposal) | Must | Not Started |
| FR-ORA-08 | Anticipate likely committee questions and prepare responses | Should | Not Started |
| FR-ORA-09 | Include visual aids (diagrams, tables, figures) where they aid understanding | Should | Not Started |
| FR-ORA-10 | Practice delivery to fit within 15-minute time constraint | Must | Not Started |

---

## 3. Non-Functional Requirements

### 3.1 Format and Compliance (NFR-FMT)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| NFR-FMT-01 | Paper must use IEEE conference format (`IEEEtran` document class) | Must | Done |
| NFR-FMT-02 | Paper body must be 5-6 pages (excluding references) | Must | Not Started |
| NFR-FMT-03 | References section does NOT count toward the page limit | Must | Configured |
| NFR-FMT-04 | Paper must compile cleanly with no LaTeX errors or warnings | Must | Not Started |
| NFR-FMT-05 | All citations must resolve (no undefined references) | Must | Not Started |
| NFR-FMT-06 | No orphan or widow lines | Should | Not Started |
| NFR-FMT-07 | Proper use of IEEE section numbering | Must | Configured |
| NFR-FMT-08 | Author block must include name, department, institution, and email | Must | Done |

### 3.2 Quality Standards (NFR-QUA)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| NFR-QUA-01 | Paper must demonstrate SYNTHESIS, not sequential paper summaries | Must | Not Started |
| NFR-QUA-02 | Every factual claim must be supported by a citation | Must | Not Started |
| NFR-QUA-03 | Research proposal must flow logically from the gap analysis | Must | Not Started |
| NFR-QUA-04 | Writing must be clear, concise, and appropriate for an academic audience | Must | Not Started |
| NFR-QUA-05 | Paper must read as a unified argument, not 6 book reports | Must | Not Started |
| NFR-QUA-06 | Non-obvious connections and gaps must be identified (demonstrate insight) | Must | Not Started |
| NFR-QUA-07 | Research proposal must be concrete and feasible | Must | Not Started |
| NFR-QUA-08 | Grammar, spelling, and punctuation must be correct throughout | Must | Not Started |
| NFR-QUA-09 | Consistent terminology and definitions across all sections | Should | Not Started |
| NFR-QUA-10 | Logical flow between sections (introduction sets up literature review; literature review sets up proposal; conclusion ties everything together) | Must | Not Started |

### 3.3 Infrastructure and Delivery (NFR-INF)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| NFR-INF-01 | LaTeX source files maintained in modular structure (`proposal/sections/`) | Must | Done |
| NFR-INF-02 | CI/CD pipeline compiles PDF on push to `main` branch | Must | Done |
| NFR-INF-03 | PDF published to GitHub Pages for easy committee access | Should | Pending (requires manual enable) |
| NFR-INF-04 | Version control with meaningful commit history | Should | Active |
| NFR-INF-05 | Memory-bank documentation maintained for session continuity | Should | Active |

### 3.4 Presentation Standards (NFR-PRE)

| ID | Requirement | Priority | Status |
|----|-------------|----------|--------|
| NFR-PRE-01 | Presentation must fit within 15-minute time limit | Must | Not Started |
| NFR-PRE-02 | Slides must be visually clean and not text-heavy | Should | Not Started |
| NFR-PRE-03 | Presenter must be able to answer questions about all 6 papers in depth | Must | Not Started |
| NFR-PRE-04 | Presentation must demonstrate understanding beyond what is written in the paper | Should | Not Started |

---

## 4. Acceptance Criteria

### 4.1 Deliverable 1: IEEE Conference Paper

The paper is ACCEPTED when ALL of the following are true:

**Content Completeness:**
- [ ] AC-PAP-01: Abstract is 150-200 words and self-contained
- [ ] AC-PAP-02: Introduction motivates the area, defines scope, and previews structure (0.5-0.75 pages)
- [ ] AC-PAP-03: Literature assessment synthesizes all 6 papers by theme (~3 pages)
- [ ] AC-PAP-04: Research proposal includes problem statement, approach, and contributions (~1 page)
- [ ] AC-PAP-05: Conclusion summarizes survey and restates research direction (~0.25 pages)
- [ ] AC-PAP-06: All 6 selected papers are cited and discussed meaningfully

**Quality Gates:**
- [ ] AC-PAP-07: Literature review is organized thematically (NOT paper-by-paper)
- [ ] AC-PAP-08: Every factual claim has a citation
- [ ] AC-PAP-09: Research proposal flows directly from identified gaps in the literature
- [ ] AC-PAP-10: Paper reads as a unified, coherent argument
- [ ] AC-PAP-11: Non-obvious connections and gaps are identified (demonstrates analytical depth)

**Format Compliance:**
- [ ] AC-PAP-12: IEEE conference format (IEEEtran class)
- [ ] AC-PAP-13: Paper body is 5-6 pages (excluding references)
- [ ] AC-PAP-14: LaTeX compiles cleanly with zero errors
- [ ] AC-PAP-15: All citations resolve (no undefined references)
- [ ] AC-PAP-16: No orphan/widow lines

**Paper Selection:**
- [ ] AC-PAP-17: Exactly 6 papers selected
- [ ] AC-PAP-18: At least 3 papers are from the provided reading lists
- [ ] AC-PAP-19: Complete BibTeX entries for all 6 papers

**Delivery:**
- [ ] AC-PAP-20: PDF compiles via GitHub Actions CI/CD
- [ ] AC-PAP-21: PDF accessible via GitHub Pages (once enabled)

### 4.2 Deliverable 2: Oral Presentation

The presentation is ACCEPTED when ALL of the following are true:

- [ ] AC-ORA-01: Slide deck is complete and covers paper content at a high level
- [ ] AC-ORA-02: Presentation fits within 15-minute time limit (verified by practice run)
- [ ] AC-ORA-03: High-level takeaways from the literature are clearly communicated
- [ ] AC-ORA-04: Research overview and area importance are established
- [ ] AC-ORA-05: Lessons learned and cross-paper connections are discussed
- [ ] AC-ORA-06: Future research directions are presented
- [ ] AC-ORA-07: Presenter can answer questions about all 6 papers in depth
- [ ] AC-ORA-08: At least one practice run completed with timing

---

## 5. Dependencies and Constraints

### 5.1 External Dependencies

| Dependency | Description | Status | Impact if Unavailable |
|------------|-------------|--------|----------------------|
| DEP-01: Reading Lists | Provided reading lists from which at least 3 papers must be selected | Needed | Cannot verify FR-SEL-02 compliance |
| DEP-02: Committee Availability | Qualifier committee schedules the oral exam date | Pending | Cannot set final deadline |
| DEP-03: GitHub Pages | Must be manually enabled in repo settings | Pending | PDF not publicly accessible (workaround: share PDF directly) |
| DEP-04: LaTeX Build Environment | `xu-cheng/latex-action@v3` in GitHub Actions | Available | Local build fallback |

### 5.2 Internal Dependencies (Task Ordering)

```
Paper Selection (all 6 papers)
    |
    v
Paper Reading & Annotation (all 6 papers)
    |
    v
Thematic Outline (organize by theme)
    |
    +---> Literature Review (Section III, ~3 pages)
    |         |
    |         v
    |     Gap Analysis (within Section III)
    |         |
    |         v
    +---> Research Proposal (Section IV, ~1 page)
              |
              v
          Introduction (Section II, 0.5-0.75 pages)
              |
              v
          Conclusion (Section V, ~0.25 pages)
              |
              v
          Abstract (Section I, 150-200 words) -- WRITE LAST
              |
              v
          Polish & Format Check (page count, citations, compilation)
              |
              v
          Presentation Preparation (slides, practice)
```

**Key Constraint:** Writing MUST proceed in this order. The literature review informs the proposal, which informs the introduction framing, and the abstract captures everything. Writing out of order produces incoherent papers.

### 5.3 Constraints

| ID | Constraint | Rationale |
|----|-----------|-----------|
| CON-01 | Exactly 6 papers, no more, no fewer | Qualifier requirement |
| CON-02 | At least 3 papers from provided reading lists | Qualifier requirement |
| CON-03 | 5-6 pages body text (IEEE conference format) | Qualifier requirement |
| CON-04 | References do not count toward page limit | Qualifier policy |
| CON-05 | 15-minute presentation + 5-minute Q&A | Qualifier requirement |
| CON-06 | Thematic synthesis, not paper-by-paper summaries | Qualifier expectation (ADR-004) |
| CON-07 | IEEE conference format (`IEEEtran` class) | Qualifier requirement |
| CON-08 | Paper list was due January 20 | Administrative deadline (past) |
| CON-09 | Reading list commitment was due January 30 | Administrative deadline (past) |

---

## 6. Risk Assessment

### 6.1 Risk Register

| ID | Risk | Likelihood | Impact | Mitigation | Status |
|----|------|-----------|--------|------------|--------|
| RSK-01 | Remaining 4 papers do not form coherent themes with the 2 already selected | Medium | High | Select papers strategically to fill thematic gaps; map candidate papers to themes before committing | Open |
| RSK-02 | Page count falls outside 5-6 page range (too short or too long) | Medium | High | Track approximate page counts per section during writing; use LaTeX compilation to check regularly | Open |
| RSK-03 | Literature review reads as paper summaries instead of synthesis | High | High | Use thematic subsections (ADR-004); write comparative statements linking papers; review each paragraph to ensure multiple papers are referenced | Open |
| RSK-04 | Research proposal feels disconnected from the literature review | Medium | High | Write gap analysis subsection explicitly; ensure each proposal contribution references a specific gap; write proposal immediately after literature review | Open |
| RSK-05 | Insufficient depth on individual papers due to 3-page constraint | Medium | Medium | Prioritize key contributions of each paper; use synthesis to discuss papers in context rather than isolation; accept that not every detail can be covered | Open |
| RSK-06 | Committee questions expose shallow understanding of a paper | Medium | High | Read all 6 papers thoroughly (not just abstracts); prepare notes on methodology, limitations, and contributions for each paper; practice Q&A | Open |
| RSK-07 | Presentation exceeds 15-minute time limit | Medium | Medium | Build slides with fewer than 15 slides; practice at least twice with timer; prepare "skip" slides for flexible pacing | Open |
| RSK-08 | Reading list papers are not relevant to Agentic AI theme | Low | High | Review reading lists early; identify papers that overlap with theme before committing; if needed, broaden theme slightly to accommodate | Open |
| RSK-09 | LaTeX compilation failures block progress | Low | Medium | CI/CD pipeline catches errors early; test compile locally if needed; modular sections isolate compilation issues | Mitigated |
| RSK-10 | Incomplete BibTeX entries cause missing citations | Low | Medium | Complete all BibTeX entries during paper selection phase; verify with test compilation | Open |
| RSK-11 | GitHub Pages not enabled, blocking committee access to PDF | Low | Low | Manual step required in repo settings; can share PDF directly as fallback | Open |
| RSK-12 | Time pressure causes skipping the reading/annotation phase | Medium | High | Resist the urge to write before reading; annotations directly feed the thematic outline; poor reading leads to poor synthesis | Open |

### 6.2 Risk Priorities

**Critical (address immediately):**
- RSK-01: Paper selection coherence -- must be resolved before any writing begins
- RSK-03: Synthesis vs. summary -- the single most important quality factor

**High (address during writing):**
- RSK-02: Page count management
- RSK-04: Proposal-literature connection
- RSK-06: Committee Q&A preparation
- RSK-12: Adequate reading time

**Medium (monitor):**
- RSK-05: Depth vs. breadth tradeoff
- RSK-07: Presentation timing

**Low (mitigated or low impact):**
- RSK-08, RSK-09, RSK-10, RSK-11

---

## 7. Verification Plan

### 7.1 Paper Verification Checkpoints

| Checkpoint | When | What to Verify |
|------------|------|----------------|
| CP-01: Paper Selection | After selecting all 6 papers | All 6 selected; at least 3 from reading lists; papers span themes; BibTeX entries complete |
| CP-02: Reading Complete | After annotating all papers | Key themes extracted per paper; connections between papers noted; gaps identified |
| CP-03: Outline Review | After thematic outline | Themes cover all papers; logical flow from themes to gaps; proposal direction evident |
| CP-04: Literature Draft | After writing Section III | ~3 pages; thematic organization; all 6 papers cited; synthesis not summary; gap analysis present |
| CP-05: Proposal Draft | After writing Section IV | ~1 page; grounded in gaps; concrete approach; clear contributions |
| CP-06: Full Draft | After all sections written | 5-6 pages; all sections present; coherent flow; all citations resolve |
| CP-07: Final Review | Before submission | Clean compilation; format compliance; page count; grammar and spelling; no TODOs remaining |

### 7.2 Presentation Verification

| Checkpoint | When | What to Verify |
|------------|------|----------------|
| CP-08: Slides Draft | After slide creation | Covers all paper sections; not text-heavy; visual aids included |
| CP-09: Practice Run | Before exam | Fits in 15 minutes; smooth transitions; Q&A preparation reviewed |

---

## 8. Traceability Matrix

This matrix maps requirements to the project phases where they are fulfilled.

| Requirement Group | Phase 1: Selection | Phase 2: Lit Review | Phase 3: Proposal | Phase 4: Completion | Phase 5: Presentation |
|-------------------|:-:|:-:|:-:|:-:|:-:|
| FR-SEL (Paper Selection) | X | | | | |
| FR-PAP-ABS (Abstract) | | | | X | |
| FR-PAP-INT (Introduction) | | | | X | |
| FR-PAP-LIT (Literature) | | X | | | |
| FR-PAP-PRO (Proposal) | | | X | | |
| FR-PAP-CON (Conclusion) | | | | X | |
| FR-PAP-REF (References) | X | X | X | X | |
| FR-ORA (Oral) | | | | | X |
| NFR-FMT (Format) | | X | X | X | |
| NFR-QUA (Quality) | | X | X | X | |
| NFR-INF (Infrastructure) | X | | | X | |
| NFR-PRE (Presentation) | | | | | X |

---

## 9. Current State Summary

**Overall Progress: Phase 1 (Paper Selection) -- In Progress**

| Category | Complete | Total | Percentage |
|----------|----------|-------|-----------|
| Papers Selected | 2 | 6 | 33% |
| BibTeX Entries Complete | 0 | 6 | 0% |
| Sections Written | 0 | 5 | 0% |
| Acceptance Criteria Met | 3 | 29 | 10% |
| Infrastructure Items | 4 | 5 | 80% |

**What is done:**
- Repository and documentation system (ADR-001)
- IEEE LaTeX template with modular sections (ADR-002)
- CI/CD pipeline for PDF build and deploy (ADR-003)
- Thematic organization decision (ADR-004)
- 2 of 6 papers selected and uploaded

**What is needed next:**
1. Select remaining 4 papers (at least 1 more from reading lists)
2. Complete BibTeX entries for all 6 papers
3. Read and annotate all 6 papers
4. Create thematic outline
5. Begin writing (literature review first)

---

## 10. Document References

| Document | Location | Purpose |
|----------|----------|---------|
| Project Brief | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/projectbrief.md` | Core objectives |
| Active Context | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/activeContext.md` | Current work state |
| Progress Tracking | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/progress.md` | Task completion |
| Phase Lifecycle | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/phases.md` | Phase coordination |
| System Patterns | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/systemPatterns.md` | Paper structure |
| Product Context | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/productContext.md` | Research area context |
| Technical Context | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/techContext.md` | LaTeX and CI/CD setup |
| Architectural Decisions | `/Users/djjay0131/code/vt-phd-qualifier/memory-bank/architecturalDecisions.md` | ADR-001 through ADR-004 |
| Qualifier Requirements | https://chbrown13.github.io/qualifier.html | Official requirements |

---

**Revision History:**
- 2026-02-20: Initial requirements document created. Comprehensive coverage of both deliverables, acceptance criteria, dependencies, risks, and verification plan.
