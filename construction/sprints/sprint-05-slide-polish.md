# Sprint 05: Slide Polish

**Sprint Goal:** Bring slides 2-20 to presentation-ready state by inserting speaker notes from `files/slides.md`, tightening body text, and adding or improving a TikZ diagram or image-based visual on every slide.
**Start Date:** 2026-03-05
**Status:** In Progress (S12 next)

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

---

### Task S12: Slide 12 - Positioning My Work

**Section:** Synthesis

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 12 speaker notes (intersection of agents + KGs, span-level traceability, stronger evaluation, SE focus, longitudinal)
- [ ] Polish: the "Intersection" block text is already good; ensure the three refinement bullets are parallel in grammatical form
- [ ] Add a TikZ puzzle-piece diagram: a jigsaw piece labeled "Agentic KGs" slotting into a notch in a larger rectangle; the notch is labeled "The Gap"; use myOrange fill for the piece

**Acceptance Criteria:**
- Note block present and introduces span-level traceability as the key positioning claim
- Puzzle-piece TikZ is present and uses theme colors
- The three refinement bullets are grammatically parallel

---

### Task S13: Slide 13 - Proposed Architecture

**Section:** Proposal

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 13 speaker notes (persistent research state loop, shared KG as source of truth, human oversees)
- [ ] Polish: in the block below the diagram, verify "Source of Truth" is bolded; remove any redundant label duplicating the diagram arrows
- [ ] Verify existing Human-Agent-KG TikZ loop diagram: confirm the "oversee" dashed arrow from human to KG is present and labeled; if the diagram clips or overlaps the block below, reduce node spacing

**Acceptance Criteria:**
- Note block present and articulates the loop concept (human queries, agent writes, KG stores, agent reads back)
- TikZ loop compiles without overfull hbox warnings
- "Source of Truth" is bolded in the block

---

### Task S14: Slide 14 - Core Innovation

**Section:** Proposal

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 14 speaker notes (span-level vs. chunk-level RAG, canonicalization agent, de-duplication, full audit trail)
- [ ] Polish: reorder the three enumerated items so Span-level alignment is first, Canonicalization Agent second, Versioned provenance third (matches speaker notes order)
- [ ] Improve existing Document-to-Graph TikZ: add a provenance chain annotation - a dashed line from the highlighted span back to the graph node labeled "provenance"; add a small second graph node connected to the first, labeled "Canonicalized"

**Acceptance Criteria:**
- Note block present and explains the span-level distinction from standard RAG
- Provenance chain dashed line is visible in the diagram
- Enumerated items are in the order: alignment, canonicalization, provenance

---

### Task S15: Slide 15 - Evaluation Framework

**Section:** Evaluation

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 15 speaker notes (four metrics: alignment P/R/F1, canonicalization kappa, traceability audit, persistence retention over 4 weeks)
- [ ] Polish: add a column header row to the table using `\rowcolor` or `\textbf` to visually differentiate the header; keep the exampleblock question
- [ ] Add a small TikZ icon bar alongside or above the table: four small icons representing each claim (magnifier for alignment, merge symbol for canonicalization, chain link for traceability, clock for persistence), each labeled with the claim name

**Acceptance Criteria:**
- Note block present and walks through all four metrics in the table's order
- Table header row is visually distinct
- Icon bar or equivalent visual is present (TikZ acceptable)

---

### Task S16: Slide 16 - Experimental Design Overview

**Section:** Evaluation

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 16 speaker notes (4-week longitudinal study, annotated SE papers, synthetic duplicate injection, human audit)
- [ ] Polish: add a one-line activity descriptor next to each week marker in the text column (e.g., "Week 1: Dataset construction", "Week 2: Injection + baseline", etc.)
- [ ] Improve existing vertical timeline TikZ: add activity labels to the right of each week dot (e.g., "Baseline + Dataset", "Injection Study", "Canonicalization Audit", "Retention Test"); add a horizontal bracket spanning all four weeks labeled "Longitudinal Window"

**Acceptance Criteria:**
- Note block present and covers all four experimental components
- Timeline TikZ has labeled activity annotations per week
- "Longitudinal Window" bracket or equivalent is present

---

### Task S17: Slide 17 - Contributions

**Section:** Contributions

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 17 speaker notes (three contributions: formal definition, curation protocol, reference infrastructure)
- [ ] Polish: add a short phrase after each contribution bullet clarifying the target audience or artifact type (e.g., "Formal definition - foundational vocabulary for the field")
- [ ] Add a TikZ three-icon row below the enumerated list: three spaced symbols - a scroll/document (formal definition), a gear (protocol), a server/cylinder (infrastructure) - each labeled with the contribution name using the myOrange accent color

**Acceptance Criteria:**
- Note block present and maps each contribution to its type (definition, protocol, infrastructure)
- Three-icon TikZ row is present and uses consistent sizing
- Icons are recognizable without detailed rendering (simple geometric shapes are fine)

---

### Task S18: Slide 18 - Near-Term Work

**Section:** Contributions

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 18 speaker notes (evaluation studies, artifact release, SE-domain deployment)
- [ ] Polish: add a time horizon label to each bullet (e.g., "Months 1-6", "Month 6", "Year 1") to show sequencing
- [ ] Add a TikZ roadmap graphic: a horizontal path with two labeled nodes - "Now" (current position marker, myRed filled circle) and "Next" (open circle, myOrange border) - connected by a thick arrow; annotate each node with the near-term work items

**Acceptance Criteria:**
- Note block present and covers evaluation, artifact release, and SE deployment
- Roadmap TikZ has "Now" and "Next" markers with annotations
- Time horizon labels appear on the bullet list

---

### Task S19: Slide 19 - Long-Term Vision

**Section:** Contributions

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 19 speaker notes (beyond SE, cross-domain, persistent AI research infrastructure, structured memory for scientific discovery)
- [ ] Polish: add "e.g., Biology, Physics, Climate Science" as a parenthetical to the Cross-domain bullet, replacing the existing `\ldots` ellipsis
- [ ] Add a TikZ horizon diagram: a horizontal line representing the horizon, with three domain icons above it (rectangles labeled "Biology", "Physics", "CS"), arranged at increasing distances to suggest expansion; a sun or glow effect behind the horizon using a filled arc

**Acceptance Criteria:**
- Note block present and uses the "foundation for persistent AI-assisted research" framing
- Horizon TikZ with domain icons is present
- Cross-domain bullet is more specific than the current form

---

### Task S20: Slide 20 - Conclusion

**Section:** Conclusion

- [ ] Insert `\note{...}` block sourced from `files/slides.md` Slide 20 speaker notes (from fragmented chat to persistent traceable state, infrastructure is the missing link, thank you)
- [ ] Polish: the three bullets below the diagram are good; add a final emphasized line "Infrastructure is the missing link to AI-assisted discovery." as a standalone `\emph{}` or inside a block
- [ ] Improve existing Chat-to-Persistent-State TikZ: add a subtitle label below the arrow ("via Agentic Knowledge Graphs"); ensure "Fragmented Chat" and "Persistent State" box sizes are equal and visually balanced on a 16:9 frame

**Acceptance Criteria:**
- Note block present and ends with a natural "thank you / questions" transition
- "Infrastructure is the missing link" statement is visually prominent
- TikZ arrow diagram is horizontally centered and balanced

---

### Task S21: Final Compile and Notes Verification

- [ ] Compile `presentation/main.tex` with `latexmk -pdf` and confirm zero errors
- [ ] Temporarily enable `\setbeameroption{show notes}` and recompile; open PDF and verify:
  - [ ] Each slide 2-20 shows a notes page
  - [ ] No notes page is blank
- [ ] Disable notes option and do a final clean compile
- [ ] Update this sprint's task checkboxes to reflect completion
- [ ] Update `memory-bank/phases.md` sprint reference if applicable

**Acceptance Criteria:**
- Zero LaTeX errors in final compile
- Notes pages verified for all 19 slides (2-20)
- Final PDF exported without notes option active

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
