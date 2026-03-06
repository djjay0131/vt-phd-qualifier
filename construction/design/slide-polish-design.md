# Slide Polish Design: Beamer Presentation Notes, Text, and Visuals

**Status:** Complete
**Created:** 2026-03-05
**Author:** Construction Coordinator

---

## Problem Statement

The Beamer presentation at `presentation/main.tex` has 20 content slides but slides 2-20 are missing `\note{...}` blocks. Several slides also have thin body text and placeholder or absent visual elements. The goal is to ensure every slide (2-20) has proper speaker notes sourced from `files/slides.md`, tightened body text, and a clear TikZ diagram or image-based visual. Slide 1 is already complete.

---

## Solution Approach

Work through slides 2-20 one at a time, applying three actions per slide in a single editing pass:

1. **Speaker notes** - Insert `\note{...}` blocks whose text follows `files/slides.md` closely. Prose is lightly adapted for in-slide placement but the meaning and sequence of the canonical notes must not change.
2. **Text polish** - Tighten bullet text and block labels so they reinforce, not repeat, the spoken words. Changes are minimal: remove redundancy, sharpen phrasing.
3. **Visual element** - Either improve an existing TikZ diagram or add a new one. When a standalone image is more appropriate, a PNG or SVG is placed in `presentation/images/` and referenced with `\includegraphics`. Every slide should have at least one non-textual element.

The canonical source of truth for speaker notes is `files/slides.md`. Any editing of note prose must preserve the intent and specific claims in that file.

---

## Constraints

- Do NOT change theme colors (myRed, myOrange), section structure, or slide order.
- Do NOT alter the title slide, outline slide, Questions slide, or References slide.
- Slide 1 is already complete (image + notes) - skip it.
- Images go in `presentation/images/` and are loaded via `\graphicspath{{images/}}`.
- TikZ libraries already loaded: `shapes.geometric`, `shapes.misc`, `shapes.symbols`, `arrows.meta`, `positioning`, `calc`, `decorations.pathmorphing`.
- Additional TikZ libraries may be added to the preamble if required.
- Keep each slide's LaTeX concise; avoid over-engineering diagrams that distract from spoken content.
- Do NOT use external images unless they are created as part of this work (no internet downloads).

---

## Repository Context

| Path | Purpose |
|------|---------|
| `presentation/main.tex` | Single-file Beamer source, all 20 slides |
| `files/slides.md` | Canonical speaker notes + visual concepts per slide |
| `presentation/images/` | Image assets; currently contains `ai_research_state_problem.png` |
| `presentation/references.bib` | BibTeX; not modified in this sprint |

Key preamble facts already in `main.tex`:
- `\usepackage{tikz}` with libraries listed above
- `\usepackage{graphicx}` with `\graphicspath{{images/}}`
- `\usepackage{booktabs}` (tables available)
- Speaker notes are activated by uncommenting `%\setbeameroption{show notes}` in the preamble

---

## Visual Strategy Per Section

### Section 1: Motivation (Slides 2-3)
- **Slide 2 (Structural Gaps):** Three cracked pillars TikZ already exists. Improve label clarity and crack styling.
- **Slide 3 (Guiding Question):** Bridge diagram TikZ already exists. Refine node proportions and label placement.

### Section 2: Literature Survey (Slides 4-10)
- **Slide 4 (Landscape Overview):** Add a TikZ landscape map showing 5 territories (hexagons or regions).
- **Slide 5 (Mechanistic Interpretability):** Add a TikZ neural-network / magnifying-glass motif: a simple layer of nodes with a magnifier overlay.
- **Slide 6 (Concept-Based Interpretability):** Add a TikZ latent-space vector scatter with directional arrows labeled as concepts.
- **Slide 7 (RAG & Vector Memory):** Improve existing columns layout; add a TikZ "pile of documents" vs. structured shelf contrast.
- **Slide 8 (Knowledge Graph Research):** Add a small TikZ graph (nodes + labeled edges) in the right column.
- **Slide 9 (Agentic Systems):** Add a TikZ agent desk that gets erased (strikethrough lines on memory area).
- **Slide 10 (Empirical Evaluation Standards):** Add a TikZ checklist / clipboard motif.

### Section 3: Synthesis (Slides 11-12)
- **Slide 11 (Cross-Cutting Gaps):** Venn diagram TikZ already exists. Ensure labels and the GAP node are prominent.
- **Slide 12 (Positioning My Work):** Add a TikZ puzzle-piece fitting into the gap.

### Section 4: Proposal (Slides 13-14)
- **Slide 13 (Proposed Architecture):** Loop diagram TikZ already exists. Verify it is clear and well-labeled.
- **Slide 14 (Core Innovation):** Document-to-graph TikZ already exists. Add span highlight and provenance chain annotation.

### Section 5: Evaluation (Slides 15-16)
- **Slide 15 (Evaluation Framework):** Table already present. Add column color headers or a small TikZ measurement icon alongside.
- **Slide 16 (Experimental Design):** Timeline TikZ already exists. Add activity labels to each week marker.

### Section 6: Contributions (Slides 17-19)
- **Slide 17 (Contributions):** Add a TikZ three-icon row: scroll, gear, server.
- **Slide 18 (Near-Term Work):** Add a TikZ roadmap with "Now" and "Next" markers.
- **Slide 19 (Long-Term Vision):** Add a TikZ horizon line with domain icons.

### Section 7: Conclusion (Slide 20)
- **Slide 20 (Conclusion):** Chat-to-infrastructure arrow TikZ already exists. Confirm it is clean and well-proportioned.

---

## How to Verify It Works

1. Run `latexmk -pdf main.tex` from `presentation/` with no errors or unresolved references.
2. Enable `\setbeameroption{show notes}` and verify every slide 2-20 shows a notes page.
3. Open the compiled PDF and visually confirm:
   - Every slide has at least one non-textual visual element.
   - No slide has bullet text that simply duplicates the notes verbatim.
   - Speaker notes match the intent of `files/slides.md` for each slide.
4. Disable notes option before final export.

---

## Implementation Phases

| Phase | Slides | Focus |
|-------|--------|-------|
| A | 2-3 | Motivation - notes + refine existing TikZ |
| B | 4-7 | Literature Survey (interpretability + RAG) - notes + new visuals |
| C | 8-11 | Literature Survey (KG, agents, eval) + Synthesis - notes + new visuals |
| D | 12-16 | Synthesis positioning + Proposal + Evaluation - notes + refine/extend TikZ |
| E | 17-20 | Contributions + Conclusion - notes + new visuals |

Each phase edits `presentation/main.tex` directly. After all phases, a single compilation pass confirms the full deck compiles cleanly.

---

## ADR References

- ADR-002: IEEE LaTeX with Modular Sections (presentation uses Beamer, same compilation pipeline)
- ADR-004: Thematic Literature Organization (section structure must be preserved)

---

**Revision:** 2026-03-05 - Initial specification
