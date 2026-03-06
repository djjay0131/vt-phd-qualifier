# Sprint 05: Slide Polish

**Sprint Goal:** Bring slides 2-20 to presentation-ready state by inserting speaker notes from `files/slides.md`, tightening body text, and adding or improving a TikZ diagram or image-based visual on every slide.
**Start Date:** 2026-03-05
**Status:** COMPLETE — All slides S02-S20 polished, image replacements done, VT logo added, 33 pages clean

**Prerequisites:**
- `presentation/main.tex` exists with all 20 slides scaffolded
- `files/slides.md` contains canonical speaker notes for all slides
- Slide 1 already has `\note{...}` block and image (treat as done)
- LaTeX compiles cleanly before this sprint begins

**Design Reference:** [construction/design/slide-polish-design.md](../design/slide-polish-design.md)

---

## Quality Gate

| Criterion | Check |
|-----------|-------|
| Every slide 2-20 has a `\note{...}` block | [ ] |
| Note text faithfully follows `files/slides.md` | [ ] |
| Every slide 2-20 has at least one non-textual visual | [ ] |
| No bullet text simply repeats the note verbatim | [ ] |
| `latexmk -pdf main.tex` compiles with zero errors | [ ] |
| PDF shows correct slide count and section navigation | [ ] |

---

## Tasks

### Task S02: Slide 2 - The Structural Gaps ✅

**Section:** Motivation

- [x] Notes written and approved
- [x] Bullets polished (Persistence, Traceability, Evaluability)
- [x] TikZ diagram retained; infrastructure framing added

---

### Task S03: Slide 3 - Guiding Question ✅

**Section:** Motivation

- [x] Notes written and approved
- [x] Research question block visually prominent

---

### Task S04: Slide 4 - Landscape Overview ✅

**Section:** Literature Survey

- [x] Notes written and approved
- [x] Bullets removed; full-width image layout (landscape_overview.png)
- [x] Image sized with height=0.72\textheight keepaspectratio

---

### Task S05: Slide 5 - Mechanistic Interpretability ✅

**Section:** Literature Survey

- [x] Notes written and approved
- [x] Two-column layout: bullets + alertblock left, image right
- [x] Sharkey citation bolded; alertblock recolored orange globally
- [x] Image: mechanistic_interpretability.png (960px, ICC stripped)

---

### Task S06: Slide 6 - Concept-Based Interpretability ✅

**Section:** Literature Survey

- [x] Notes written and approved (Option A landing)
- [x] Bullets removed; image left (0.65\textwidth), alertblock right (0.32\textwidth)
- [x] Image: concept_interpretability.png (960px, ICC stripped)

---

### Task S07: Slide 7 - RAG and Vector Memory Systems ✅

**Section:** Literature Survey

- [x] Notes written and approved (Suryawanshi, canonical-memory and provenance gaps)
- [x] Limitations block reordered (no canonical memory before no provenance chain)
- [x] Image-based visual: rag_vs_kg.jpg (960px, JPEG, two-column layout with alertblock)

---

### Task S08: Slide 8 - Knowledge Graph Research ✅

**Section:** Literature Survey

- [x] Notes written and approved (automation gap, KGs+LLMs integration)
- [x] Italicized conclusion line added below columns
- [x] TikZ KG diagram: 4 nodes (Paper, Problem, Evidence, Method) with labeled edges, myOrange palette
- [x] TikZ replaced with kg_research.jpg (overlapping edge labels fixed via image)

---

### Task S09: Slide 9 - Agentic Systems ✅

**Section:** Literature Survey

- [x] Notes written and approved (amnesia framing, Denario, Trinkenreich)
- [x] Both footcites present; bullet text polished
- [x] Image-based visual: agentic_amnesia.jpg (960px, JPEG, two-column layout with alertblock)

---

### Task S10: Slide 10 - Empirical Evaluation Standards ✅

**Section:** Literature Survey

- [x] Notes written and approved (Ralph, Baltes, single-pass gap, longitudinal need)
- [x] Observation block sharpened to reference single-pass/qualitative evaluations
- [x] TikZ clipboard/checklist diagram: checked and unchecked rows, myOrange palette

---

### Task S11: Slide 11 - Cross-Cutting Gaps in the Literature ✅

**Section:** Synthesis

- [x] Notes written and approved (four-adjective fragmentation framing, expanded 4 paragraphs)
- [x] Four-word adjective labels: unstructured, static, amnesic, short-term (shifted to avoid circles)
- [x] TikZ Venn: VT colors (myRed/myOrange), GAP node centered with myRed border, labels at y=±2.0/±0.8
- [x] TikZ Venn replaced with cross_cutting_gaps.jpg + two-column bullet layout (Retrieval/Graphs/Agents/Evaluation)

---

### Task S12: Slide 12 - Positioning My Work ✅

**Section:** Synthesis

- [x] Notes written and approved (intersection of agents + KGs, span-level traceability, stronger evaluation, SE focus, longitudinal)
- [x] Two-column layout: bullets left, positioning_my_work.jpg right
- [x] Three refinement bullets grammatically parallel

---

### Task S13: Slide 13 - Proposed Architecture ✅

**Section:** Proposal

- [x] Notes written and approved (persistent research state loop, shared KG as source of truth, human oversees)
- [x] Two-column: TikZ loop left, block right (fixed cut-off bullet issue)
- [x] "Source of Truth" bolded in block

---

### Task S13b: Slide 13b - Problem Extraction & Ranking ✅ (NEW)

**Section:** Proposal (inserted between S13 and S14)

- [x] New slide added to cover problem extraction/ranking step
- [x] Two-column: bullets left, TikZ paper→ranked problem nodes right
- [x] TikZ replaced with problem_extraction.jpg
- [x] Kept brief (low time allocation in 15-min talk)

---

### Task S14: Slide 14 - Core Innovation ✅

**Section:** Proposal

- [x] Notes written and approved (span-level vs. chunk-level RAG, canonicalization agent)
- [x] Provenance chain dashed line added to TikZ
- [x] Canonicalized node added to diagram
- [x] TikZ replaced with core_innovation.jpg

---

### Task S15: Slide 15 - Evaluation Framework ✅

**Section:** Evaluation

- [x] Notes written and approved (four metrics: alignment P/R/F1, kappa, traceability audit, persistence)
- [x] Icon bar above table (magnifier, merge, chain, clock)
- [x] "Key Question" block uses block (not exampleblock green)

---

### Task S16: Slide 16 - Experimental Design Overview ✅

**Section:** Evaluation

- [x] Notes written and approved (4-week longitudinal, annotated SE papers, synthetic duplicates, human audit)
- [x] experimental_design.jpg in right column
- [x] Bullets shortened to 2-3 words each
- [x] 4-week justification and post-build timing explained in notes

---

### Task S17: Slide 17 - Contributions ✅

**Section:** Contributions

- [x] Notes written and approved
- [x] "Formal definition" reframed as "Span-level traceability specification" (more defensible)
- [x] Three-icon TikZ (scroll, gear, server) with myOrange labels

---

### Task S18: Slide 18 - Near-Term Work ✅

**Section:** Contributions

- [x] Notes written and approved (evaluation, artifact release, SE deployment)
- [x] Time horizon labels added (Months 1-6, 6-7, 7-8, Year 1)
- [x] TikZ roadmap: filled myRed "Now" → thick arrow → open myOrange "Next"

---

### Task S19: Slide 19 - Long-Term Vision ✅

**Section:** Contributions

- [x] Notes written and approved (beyond SE, cross-domain synthesis framing)
- [x] long_term_vision.jpg in right column
- [x] Cross-domain bullet with (Biology, Physics, Climate Science)

---

### Task S20: Slide 20 - Conclusion ✅

**Section:** Conclusion

- [x] Notes written and approved (infrastructure is the missing link, thank you / questions)
- [x] "Infrastructure is the missing link" as `\emph{}` prominent centered line
- [x] TikZ improved: equal box sizes, subtitle "via Agentic Knowledge Graphs" under arrow

---

### Task S21: Final Compile and Notes Verification ✅

- [x] main.pdf compiled cleanly (33 pages, zero errors, zero overfull warnings)
- [x] main-notes.pdf compiled cleanly (33 pages, zero errors)
- [x] Both PDFs reside in presentation/
- [x] VT horizontal logo added to frametitle top-right on every slide (vt_logo_horiz.jpg)
- [x] agentic_amnesia.jpg replaced with updated version
- [x] Q&A Page 1 split from 5-item overflow frame into two frames (1a: S2/S7/S8, 1b: S9/S12)
- [x] Print-ready PDFs generated via Ghostscript (main_print.pdf, main-notes_print.pdf)

---

## Architecture Decisions

- ADR-002: IEEE LaTeX with Modular Sections (Beamer shares compilation pipeline)
- ADR-004: Thematic Literature Organization (section structure preserved unchanged)

---

## Dependencies

- `presentation/main.tex` with all 20 slides scaffolded (exists)
- `files/slides.md` with canonical speaker notes (exists)
- `presentation/images/` directory (exists)
- TikZ libraries already in preamble (shapes.geometric, arrows.meta, positioning, calc, decorations.pathmorphing)

---

## Risks

| Risk | Mitigation | Status |
|------|------------|--------|
| TikZ diagrams overflow slide frame | Test compile after each task; use `scale` parameter to resize | Open |
| Note text diverges from slides.md | Cross-check each note block against slides.md before marking task done | Open |
| Additional TikZ libraries needed | Add to preamble before using; keep list documented | Open |
| Over-engineering visuals slows progress | Limit each diagram to 6-8 TikZ elements; use simple shapes | Open |
