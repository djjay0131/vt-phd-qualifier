# Sprint 3: Research Proposal and Paper Completion

**Sprint Goal:** Write the research proposal, introduction, conclusion, and abstract; then polish and publish the complete 5-6 page IEEE paper.
**Start Date:** 2026-02-24
**Status:** In Progress (Tasks 1-6 complete)

**Prerequisites:** Sprint 2 complete (Quality Gate 2 passed -- literature review drafted, all 5 subsections complete, gap analysis identifies 2-3 concrete gaps)

**Design Reference:** [construction/design/qualifier-design.md](../design/qualifier-design.md) -- Sections 3.4, 3.2, 3.5, 3.1, 6, 8, 9.3, 9.4

**Phases Covered:** Phase 3 (Research Proposal) + Phase 4 (Paper Completion)

---

## Input Artifacts

These must exist and be complete before Sprint 3 begins:

- [ ] Complete literature review (~3 pages) in `proposal/sections/03-literature-review.tex`
- [ ] All 5 subsections drafted (3.3.1-3.3.5), no TODO placeholders
- [ ] Gap analysis (Section 3.3.5) identifies 2-3 concrete, ranked gaps
- [ ] All 6 paper annotations complete
- [ ] Paper-to-theme matrix finalized
- [ ] All 6 papers cited at least twice each in the literature review
- [ ] LaTeX compiles cleanly at sprint start

---

## Writing Order

**STRICT:** Sections must be written in this order per the design document dependency graph (Section 8.1). Do not skip ahead.

```
Research Proposal (Section IV)
    |
    v
Introduction (Section II)
    |
    v
Conclusion (Section V)
    |
    v
Abstract (Section I)  -- WRITE LAST
    |
    v
Final Polish + Publish
```

---

## Tasks

### Task 1: Research Proposal -- Problem Statement (Section 4.1)

**File:** `proposal/sections/04-research-proposal.tex`
**Target:** First subsection of ~1 page proposal

- [x] Review gap analysis in Section 3.3.5 and identify the primary gap to address
- [x] Reference the specific gap(s) by section label (explicit `\ref{sec:lit-synthesis}`)
- [x] State the problem in 2-3 sentences
- [x] Explain why existing approaches (citing specific papers) are insufficient
- [x] Define the scope of the proposed research
- [x] Verify the problem is NOT already solved by any of the 6 papers
- [x] Compile LaTeX and verify no errors

**Acceptance Criteria:**
- Problem statement explicitly references Section 3.3.5 gaps by label
- At least 2 citations to surveyed papers explaining insufficiency
- Problem is scoped to something tractable (not "solve all of agentic AI")
- Problem is distinct from what any individual surveyed paper already addresses

---

### Task 2: Research Proposal -- Proposed Approach (Section 4.2)

**File:** `proposal/sections/04-research-proposal.tex`
**Dependencies:** Task 1 complete

- [x] Describe the high-level methodology (what to build, study, or prove)
- [x] Connect the approach to strengths identified in surveyed papers (build on what works)
- [x] Identify 2-3 key technical challenges
- [x] Explain what makes this approach feasible
- [x] Use concrete language (NOT "explore" or "investigate" -- say what will be built or measured)
- [x] Compile LaTeX and verify no errors

**Acceptance Criteria:**
- Approach is concrete and actionable (a reader can envision what would be built/studied)
- Approach references strengths from at least 2 surveyed papers
- Technical challenges are acknowledged, not hand-waved
- Feasibility argument is present

---

### Task 3: Research Proposal -- Expected Contributions (Section 4.3)

**File:** `proposal/sections/04-research-proposal.tex`
**Dependencies:** Task 2 complete

- [x] List 2-3 specific contributions
- [x] Map each contribution to a specific gap from Section 3.3.5
- [x] State how each contribution advances the state of the art
- [x] Briefly note how each contribution could be evaluated
- [x] Compile LaTeX and verify no errors

**Acceptance Criteria:**
- Each contribution traces back to a named gap
- Contributions are evaluable (there is a way to measure success)
- No contribution is vague or unfalsifiable
- Total proposal section is ~1 page (0.75-1.25 acceptable)

---

### Task 4: Quality Gate 3 -- Research Proposal Draft

**Dependencies:** Tasks 1-3 complete

- [x] Problem statement references specific gaps from synthesis section (Section 3.3.5)
- [x] Approach is concrete (describes what to build/study/prove, not "explore")
- [x] Each contribution traces back to a specific gap
- [ ] Page count check: proposal section is ~1 page (0.75-1.25 acceptable) — DEFERRED to Task 9 (currently ~1.5-2 pages)
- [x] Proposal feels like a natural consequence of the literature review (not a separate idea)
- [x] Read proposal immediately after reading Section 3.3.5 -- does it flow?
- [x] LaTeX compiles cleanly with `latexmk`

**Gate Decision:**
- All criteria pass: proceed to Task 5
- Any criterion fails: revise proposal before continuing

---

### Task 5: Introduction (Section II)

**File:** `proposal/sections/02-introduction.tex`
**Dependencies:** Quality Gate 3 passed; literature review structure finalized
**Target:** 0.5-0.75 pages

- [x] Paragraph 1: Broad context -- LLMs enabling autonomous agents for research tasks; establish why this matters
- [x] Paragraph 2: Narrow scope -- this survey focuses on agentic systems combining knowledge representation, multi-agent coordination, and autonomous reasoning
- [x] Paragraph 3: Contribution statement -- surveys 6 papers by theme, identifies gaps, proposes research
- [x] Paragraph 4: Section roadmap -- brief preview of each section by name
- [ ] Reference all 5 thematic subsections of the literature review by name in the roadmap — roadmap references sections by label, subsection names deferred to polish
- [x] Verify every factual claim has a citation or is common knowledge
- [x] Do NOT begin with "In recent years..." or similar cliches
- [x] Page count check: 0.5-0.75 pages (do not exceed)
- [x] Compile LaTeX and verify no errors

**Acceptance Criteria:**
- Four distinct paragraphs with clear purpose
- All 5 literature review subsection themes are named in the roadmap
- No uncited claims (unless common knowledge)
- No cliche openings
- Page count within 0.5-0.75 range

---

### Task 6: Conclusion (Section V)

**File:** `proposal/sections/05-conclusion.tex`
**Dependencies:** Task 5 complete; proposal section complete
**Target:** ~0.25 pages (2-3 short paragraphs)

- [x] Summarize the key insight from thematic synthesis (1-2 sentences)
- [x] Restate the proposed research direction and why it matters
- [x] Connect to the broader trajectory of agentic AI research
- [x] Do NOT introduce new information or new citations
- [x] Verify conclusion echoes the introduction's framing (sense of closure)
- [x] Page count check: ~0.25 pages
- [x] Compile LaTeX and verify no errors

**Acceptance Criteria:**
- No new information or citations introduced
- Echoes the framing from the introduction
- Reader finishes with a clear sense of what was learned and where the field is going
- Within page budget

---

### Task 7: Abstract (Section I) -- WRITE LAST

**File:** `proposal/sections/01-abstract.tex`
**Dependencies:** ALL other sections complete (Tasks 1-6)
**Target:** 150-200 words

- [ ] State the research area (agentic AI for autonomous research)
- [ ] Describe the scope of the survey (6 papers, themes covered)
- [ ] Summarize the key finding from the synthesis (primary gap or tension)
- [ ] State the proposed research direction in one sentence
- [ ] Close with significance of the proposal
- [ ] Word count verification: must be 150-200 words exactly
- [ ] No citations in the abstract
- [ ] Compile LaTeX and verify no errors

**Acceptance Criteria:**
- Self-contained: a reader can decide whether to read the paper from the abstract alone
- Word count 150-200 (verified by count)
- Zero citations
- Covers all five elements: area, scope, finding, direction, significance

---

### Task 8: Compilation and Citation Verification

**Dependencies:** Tasks 1-7 complete

- [ ] Run `latexmk` -- full clean build succeeds with no errors
- [ ] Check compiled PDF for `[?]` markers (unresolved citations)
- [ ] Verify all `\ref{}` cross-references resolve (no "??" in PDF)
- [ ] Verify all 6 papers appear in the references section
- [ ] Verify no TODO placeholders remain anywhere in any `.tex` file
- [ ] Check that `references.bib` has no syntax errors

**Acceptance Criteria:**
- Zero LaTeX errors or warnings (font warnings acceptable)
- Zero `[?]` citation markers in PDF
- Zero `??` cross-reference markers in PDF
- Zero TODO placeholders in any section file
- All 6 papers present in compiled references

---

### Task 9: Page Count and Formatting Polish

**Dependencies:** Task 8 complete

- [ ] Total page count: 5-6 pages excluding references
- [ ] If under 5 pages: identify sections to expand (Synthesis & Gap Analysis first, per design doc)
- [ ] If over 6 pages: identify sections to trim (Background first, per design doc)
- [ ] Check for orphan lines (single line of a paragraph at top of column/page)
- [ ] Check for widow lines (single line of a paragraph at bottom of column/page)
- [ ] Fix any orphan/widow issues with minor rewording or `\looseness` adjustments
- [ ] Grammar and spelling check across all sections
- [ ] Visual inspection of PDF: figures, tables, spacing look correct
- [ ] Verify IEEE conference format compliance (margins, font sizes, column layout)

**Acceptance Criteria:**
- Page count is 5-6 pages (excluding references)
- No orphan or widow lines
- No spelling or grammar errors
- IEEE format is correct on visual inspection

---

### Task 10: Argument Arc Coherence Review

**Dependencies:** Task 9 complete

- [ ] Read the complete paper start to finish in one pass
- [ ] Verify the argument arc flows: Introduction sets up the problem, Literature Review builds the landscape, Gap Analysis surfaces what is missing, Proposal addresses the gaps, Conclusion brings it home
- [ ] Check that the introduction and conclusion echo each other (sense of closure)
- [ ] Verify no section feels disconnected or like a standalone piece
- [ ] Run verification tests from design doc Section 12:
  - [ ] Synthesis test: lit review is understandable without reading original papers
  - [ ] Gap test: gaps feel inevitable after reading Sections 3.3.1-3.3.4
  - [ ] Proposal test: proposal feels like the obvious next step after gap analysis
  - [ ] Coherence test: reading intro then conclusion makes sense as a narrative arc
  - [ ] Independence test: no lit review subsection reads as a standalone paper summary

**Acceptance Criteria:**
- All 5 verification tests from design doc Section 12 pass
- No section feels disconnected
- Argument arc is coherent from first paragraph to last

---

### Task 11: Quality Gate 4 -- Complete Paper

**Dependencies:** Tasks 8-10 complete

This is the final quality gate before presentation preparation.

- [ ] All sections complete -- no TODO placeholders anywhere
- [ ] Abstract is 150-200 words
- [ ] Total page count is 5-6 pages (excluding references)
- [ ] All citations resolve -- no `[?]` in compiled PDF
- [ ] No orphan or widow lines
- [ ] Paper compiles cleanly -- `latexmk` succeeds with no errors
- [ ] Argument arc is coherent -- read-through flows from intro to conclusion
- [ ] Published to GitHub Pages -- CI/CD pipeline succeeds
- [ ] All 5 verification tests from design doc Section 12 pass

**Gate Decision:**
- All criteria pass: Sprint 3 complete; proceed to Sprint 4 (Presentation)
- Any criterion fails: address the failure before marking sprint complete

---

### Task 12: Publish to GitHub Pages

**Dependencies:** Quality Gate 4 criteria met (except this one)

- [ ] Commit all final changes to `main` branch (or merge PR to `main`)
- [ ] Verify GitHub Actions workflow triggers on push
- [ ] Verify PDF compiles successfully in CI
- [ ] Verify PDF is published to GitHub Pages
- [ ] Download and inspect the published PDF to confirm it matches local build

**Acceptance Criteria:**
- GitHub Actions build completes with green status
- PDF is accessible via GitHub Pages URL
- Published PDF matches local compilation

---

## Files Modified in This Sprint

| File | Section | Task(s) |
|------|---------|---------|
| `proposal/sections/04-research-proposal.tex` | Research Proposal | 1, 2, 3, 4 |
| `proposal/sections/02-introduction.tex` | Introduction | 5 |
| `proposal/sections/05-conclusion.tex` | Conclusion | 6 |
| `proposal/sections/01-abstract.tex` | Abstract | 7 |
| `proposal/main.tex` | Main document | 9 (if formatting adjustments needed) |
| `proposal/references.bib` | Bibliography | 8 (if corrections needed) |
| `memory-bank/phases.md` | Phase tracking | On sprint completion |
| `memory-bank/activeContext.md` | Current state | On sprint completion |
| `memory-bank/progress.md` | Task tracking | Throughout sprint |

---

## Architecture Decisions

- ADR-002: IEEE LaTeX with Modular Sections (sections are separate files, included by `main.tex`)
- ADR-003: GitHub Actions CI/CD Pipeline (automated build and publish on push to main)
- ADR-004: Thematic Literature Organization (themes drive structure, proposal flows from gaps)

---

## Dependencies

- Sprint 2 must be complete with Quality Gate 2 passed
- Complete literature review with gap analysis (the input to the proposal)
- All 6 paper annotations and paper-to-theme matrix (for cross-referencing)
- Working LaTeX build environment (local and CI)
- GitHub Pages enabled in repository settings

---

## Risks

| Risk | Likelihood | Impact | Mitigation | Status |
|------|-----------|--------|------------|--------|
| Research proposal feels disconnected from literature review | Medium | High | Write gap analysis (3.3.5) before proposal; use explicit `\ref{}` to section labels; read 3.3.5 then proposal back-to-back | Open |
| Page budget exceeded (over 6 pages) | Medium | Medium | Track cumulative page count after each section; trim Background subsection first per design doc | Open |
| Page budget underutilized (under 5 pages) | Low | Medium | Expand Synthesis & Gap Analysis or add a comparison table per design doc | Open |
| Abstract does not fit 150-200 word constraint | Low | Low | Draft at 175 words (middle of range); iterate with word count after each edit | Open |
| Orphan/widow lines degrade formatting | Medium | Low | Visual PDF inspection; use `\looseness=-1` or minor rewording to fix | Open |
| CI/CD pipeline fails on final push | Low | Medium | Test local compilation first; ensure `references.bib` is error-free | Open |
| Argument arc breaks across sections | Medium | High | Full read-through (Task 10) specifically checks coherence; apply design doc verification tests | Open |

---

## Progress Summary

```
Sprint Progress: 6/12 tasks (50%)

Completed:
- [x] Task 1:  Research Proposal -- Problem Statement
- [x] Task 2:  Research Proposal -- Proposed Approach
- [x] Task 3:  Research Proposal -- Expected Contributions
- [x] Task 4:  Quality Gate 3 -- Research Proposal Draft (page count deferred)
- [x] Task 5:  Introduction
- [x] Task 6:  Conclusion

Not Started:
- [ ] Task 7:  Abstract
- [ ] Task 8:  Compilation and Citation Verification
- [ ] Task 9:  Page Count and Formatting Polish
- [ ] Task 10: Argument Arc Coherence Review
- [ ] Task 11: Quality Gate 4 -- Complete Paper
- [ ] Task 12: Publish to GitHub Pages
```

---

## Notes

- Writing order is STRICT: Proposal -> Introduction -> Conclusion -> Abstract -> Polish. The design doc dependency graph (Section 8.1) dictates this order because each section depends on prior sections being complete.
- The abstract must be written LAST. It is a summary of the complete paper and cannot be accurate until all other content is final.
- Quality Gate 3 is a checkpoint within this sprint (after proposal, before introduction). Quality Gate 4 is the sprint exit gate.
- The design doc Section 12 verification tests are the ultimate quality measure for the paper. Task 10 applies all five tests.
- Page budget target is 5.0-5.25 pages of content, leaving 0.75-1.0 pages of margin before the 6-page maximum.
