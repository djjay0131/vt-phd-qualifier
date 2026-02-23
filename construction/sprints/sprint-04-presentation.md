# Sprint 4: Presentation Preparation

**Sprint Goal:** Create slide deck for 15-minute oral presentation + 5 minutes Q&A, rehearse, and prepare for committee questions.
**Phase:** Phase 5 - Presentation
**Start Date:** TBD (after Sprint 3 complete)
**Status:** Not Started

**Prerequisites:**
- Sprint 3 complete (Quality Gate 4 passed -- paper is final)
- Final IEEE conference paper (5-6 pages) compiled and published
- All 6 paper annotations available
- Paper-to-theme matrix finalized

**Design Reference:** [construction/design/qualifier-design.md](../design/qualifier-design.md) -- Sections 7, 9.5, 12

---

## Quality Gate 5: Presentation Ready

| Criterion | Check | Status |
|-----------|-------|--------|
| All slides complete | 13-14 slides as planned | [ ] |
| Timing verified | Rehearsal fits in 15 minutes | [ ] |
| Backup slides prepared | At least 3 anticipatory Q&A slides | [ ] |
| Narrative arc matches paper | Same argument flow | [ ] |
| Visuals are clear | Diagrams readable, minimal text per slide | [ ] |

---

## Tasks

### Task 1: Slide Deck Setup

Create the presentation scaffold and title slide.

- [ ] Choose presentation tool (Keynote, Google Slides, Beamer, or PowerPoint)
- [ ] Set up slide template with consistent styling (fonts, colors, layout)
- [ ] Create Slide 1: Title slide (name, paper title, advisor, date, Virginia Tech branding)
- [ ] Establish visual style guide for the deck (accent colors, diagram palette, font sizes)

**Acceptance Criteria:**
- Template is set up with consistent styling across all slide layouts
- Title slide contains all required information (name, title, advisor, date)
- Slide dimensions and font sizes are appropriate for projection

---

### Task 2: Opening Slides -- Motivation and Scope (Slides 2-3)

Condense the introduction into a compelling hook and clear scope statement.

- [ ] Create Slide 2: Motivation and context (1:30 allocation)
  - [ ] Craft 1-2 sentence hook explaining why agentic AI for research matters
  - [ ] Include a compelling visual or statistic that grounds the motivation
  - [ ] Keep text minimal -- audience should listen, not read
- [ ] Create Slide 3: Scope and paper selection (1:00 allocation)
  - [ ] List all 6 papers (abbreviated titles)
  - [ ] Show what themes they cover (visual mapping or compact table)
  - [ ] Explain selection rationale in speaker notes

**Content Source:** Paper Introduction (Section 2) condensed to hook + scope

**Acceptance Criteria:**
- Slide 2 motivates the audience within 90 seconds without technical jargon
- Slide 3 makes the 6-paper scope and thematic coverage immediately clear
- Speaker notes capture the full talking points for both slides

---

### Task 3: Background Slide (Slide 4)

Establish shared vocabulary with one visual diagram.

- [ ] Create Slide 4: Background concepts (1:30 allocation)
  - [ ] Design a single visual diagram showing relationships between key concepts (LLM-based agents, tool use, knowledge graphs, RAG)
  - [ ] Define 3-4 key terms visually rather than as bullet points
  - [ ] Ensure diagram is readable from the back of the room
- [ ] Write speaker notes with definitions and transitions

**Content Source:** Paper Section 3.3.1 (Background and Foundations) distilled to one diagram

**Acceptance Criteria:**
- One clear diagram captures all foundational concepts
- No more than 4-5 key terms introduced
- Diagram is self-explanatory with minimal labels

---

### Task 4: Agentic Architectures Slides (Slides 5-6)

Present architecture comparison as a visual comparison, not a paper-by-paper walkthrough.

- [ ] Create Slide 5: Architecture patterns overview (first half of 2:00 allocation)
  - [ ] Design architecture comparison diagram showing patterns across papers (single-agent vs. multi-agent, role specialization, coordination mechanisms)
  - [ ] Highlight 2-3 key architectural decisions that differentiate approaches
- [ ] Create Slide 6: Architecture trade-offs (second half of 2:00 allocation)
  - [ ] Create a trade-off visual (table or 2x2 matrix) for autonomy vs. control, specialization vs. generality
  - [ ] Surface key insight: what the architectural choices reveal about the field
- [ ] Write speaker notes linking specific papers to each architectural pattern

**Content Source:** Paper Section 3.3.2 (Agentic Architectures and Frameworks)

**Acceptance Criteria:**
- Architecture comparison is visual, not textual
- Trade-offs are clearly communicated (not just listed)
- Individual papers are referenced but content is synthesized, not summarized per-paper

---

### Task 5: Knowledge Representation Slides (Slides 7-8)

Compare how agents manage knowledge across the surveyed papers.

- [ ] Create Slide 7: Knowledge representation approaches (first half of 2:00 allocation)
  - [ ] Design comparison visual showing different approaches (knowledge graphs, vector stores, hybrid)
  - [ ] Show how papers cluster by approach
- [ ] Create Slide 8: Integration with reasoning (second half of 2:00 allocation)
  - [ ] Illustrate how retrieval connects to reasoning (RAG patterns, graph traversal)
  - [ ] Highlight limitations and open challenges in knowledge management
- [ ] Write speaker notes connecting each approach to specific papers and their results

**Content Source:** Paper Section 3.3.3 (Knowledge Representation and Reasoning)

**Acceptance Criteria:**
- Approach comparison is visual (diagram or structured table, not bullet list)
- Clear connection drawn between knowledge representation choices and agent capabilities
- At least 3 papers referenced across these two slides

---

### Task 6: Autonomous Research Slide (Slide 9)

Show what agents can actually do today.

- [ ] Create Slide 9: Autonomous research capabilities (1:30 allocation)
  - [ ] Create a capability overview (e.g., table or visual spectrum) of research tasks agents automate
  - [ ] Show the scope of autonomy: fully autonomous vs. human-in-the-loop
  - [ ] Note which research domains are covered vs. missing
- [ ] Write speaker notes with specific examples from the papers

**Content Source:** Paper Section 3.3.4 (Autonomous Research and Discovery)

**Acceptance Criteria:**
- Audience can quickly see what agents do today and where boundaries are
- Scope of autonomy is visually represented, not just described
- Slide does not exceed ~5 visual elements (avoid clutter)

---

### Task 7: Synthesis and Gaps Slide (Slide 10)

This is the pivot slide -- the most important single slide in the deck.

- [ ] Create Slide 10: Synthesis and gaps (2:00 allocation)
  - [ ] Present 2-3 cross-cutting findings that span multiple literature themes
  - [ ] Surface the key tensions or contradictions between papers
  - [ ] Clearly state 2-3 gaps, with the primary gap visually highlighted
  - [ ] Design the slide to serve as a bridge: "here is what is missing, and here is what we should build"
- [ ] Write detailed speaker notes covering the full argument for each gap
- [ ] Ensure the primary gap on this slide leads directly to Slide 11

**Content Source:** Paper Section 3.3.5 (Synthesis and Gap Analysis)

**Acceptance Criteria:**
- Gaps are concrete and specific (not vague observations)
- The primary gap that motivates the proposal is visually prominent
- The slide creates a natural transition from "what exists" to "what is needed"
- This slide can stand alone as a summary of the entire literature review

---

### Task 8: Research Proposal Slides (Slides 11-12)

Present the proposed research as a direct response to the gaps.

- [ ] Create Slide 11: Problem statement and approach (first half of 2:00 allocation)
  - [ ] State the problem in 1-2 sentences (traced back to Slide 10 gaps)
  - [ ] Describe the proposed approach at a high level with a visual or diagram
  - [ ] Show how the approach builds on strengths from the surveyed papers
- [ ] Create Slide 12: Expected contributions (second half of 2:00 allocation)
  - [ ] List 2-3 specific contributions
  - [ ] Visually map each contribution back to a gap from Slide 10
  - [ ] Include brief note on evaluation strategy
- [ ] Write speaker notes explaining feasibility and technical challenges

**Content Source:** Paper Section 4 (Research Proposal -- all 3 subsections)

**Acceptance Criteria:**
- Problem statement explicitly connects to gaps from Slide 10
- Approach is concrete ("build X that does Y") not vague ("explore the space of...")
- Contributions are traceable back to specific gaps
- A committee member can see the logical chain: gap -> problem -> approach -> contribution

---

### Task 9: Closing Slides (Slides 13-14)

Close with one takeaway and transition to Q&A.

- [ ] Create Slide 13: Conclusion and future directions (1:00 allocation)
  - [ ] State the single key takeaway from the entire presentation
  - [ ] Connect to the broader trajectory of agentic AI research
  - [ ] Keep to 3-4 lines maximum
- [ ] Create Slide 14: Questions slide (0:15 allocation)
  - [ ] Clean transition slide with "Questions?" and contact information
  - [ ] Optionally include 2-3 seed questions to prompt discussion
- [ ] Write speaker notes for concluding remarks and transition phrasing

**Content Source:** Paper Section 5 (Conclusion) distilled to one message

**Acceptance Criteria:**
- Conclusion echoes the motivation from Slide 2 (creates narrative closure)
- No new information introduced on Slide 13
- Questions slide is clean and professional

---

### Task 10: Diagram and Visual Creation

Create all diagrams and visuals referenced in slides.

- [ ] Background concepts diagram (Slide 4): relationships between agents, KGs, RAG, tool use
- [ ] Architecture comparison diagram (Slide 5): patterns across papers
- [ ] Trade-off matrix or visual (Slide 6): autonomy vs. control, specialization vs. generality
- [ ] Knowledge representation comparison visual (Slide 7): approaches across papers
- [ ] Retrieval-reasoning integration diagram (Slide 8): how retrieval feeds reasoning
- [ ] Capability overview visual (Slide 9): what agents do, autonomy spectrum
- [ ] Gap visualization (Slide 10): cross-cutting gaps with primary gap highlighted
- [ ] Proposal approach diagram (Slide 11): high-level architecture or methodology visual
- [ ] Contribution-to-gap mapping visual (Slide 12): traceability diagram

**Acceptance Criteria:**
- All diagrams use consistent visual style (colors, fonts, line weights)
- Every diagram is readable at projection size (test at reduced scale)
- Diagrams are original (not screenshots from papers) but can reference paper figures conceptually
- No diagram contains more than 7-8 visual elements (Miller's law)

---

### Task 11: Backup Slides for Q&A Preparation

Prepare anticipatory slides for likely committee questions.

- [ ] Backup Slide A: "Why these 6 papers?"
  - [ ] Show selection criteria and how papers satisfy them
  - [ ] Acknowledge what was excluded and why
- [ ] Backup Slide B: "How does your proposal differ from [specific paper]?"
  - [ ] Create comparison table: proposal vs. closest existing work
  - [ ] Highlight what is novel in the proposal
- [ ] Backup Slide C: "What are the limitations of your proposed approach?"
  - [ ] List 2-3 honest limitations
  - [ ] For each, note how it could be mitigated or is acceptable
- [ ] Backup Slide D: "How would you evaluate the proposal?"
  - [ ] Describe evaluation methodology and metrics
  - [ ] Note what success looks like concretely
- [ ] Prepare written responses (not slides) for additional likely questions:
  - [ ] "What would you do differently if you started the survey over?"
  - [ ] "How does this relate to your broader PhD research?"
  - [ ] "What is the timeline for the proposed research?"
  - [ ] "What related work did you consider but not include?"

**Acceptance Criteria:**
- At least 4 backup slides prepared (A through D)
- Each backup slide can be presented in under 60 seconds
- Written responses exist for at least 4 additional anticipated questions
- Answers are honest about limitations (committee members detect evasion)

---

### Task 12: Speaker Notes and Narrative Script

Write the full narrative connecting all slides.

- [ ] Write speaker notes for every slide (Slides 1-14)
- [ ] Ensure narrative follows the same argument arc as the paper:
  - Motivation -> Survey -> Gaps -> Proposal -> Significance
- [ ] Mark transitions between major sections with explicit transition phrases
- [ ] Verify that the narrative is self-contained (someone hearing only the narration should follow the argument)
- [ ] Time each slide's speaker notes against its allocation:

| Slide(s) | Allocated Time | Notes Word Target (~130 wpm) |
|-----------|---------------|-------------------------------|
| 1 | 0:15 | ~30 words |
| 2 | 1:30 | ~195 words |
| 3 | 1:00 | ~130 words |
| 4 | 1:30 | ~195 words |
| 5-6 | 2:00 | ~260 words total |
| 7-8 | 2:00 | ~260 words total |
| 9 | 1:30 | ~195 words |
| 10 | 2:00 | ~260 words |
| 11-12 | 2:00 | ~260 words total |
| 13 | 1:00 | ~130 words |
| 14 | 0:15 | ~30 words |

**Acceptance Criteria:**
- Speaker notes exist for all 14 slides
- Total word count of notes is approximately 1,900-2,000 words (15 min at ~130 wpm)
- Transition phrases are explicitly marked
- Notes are written in natural speaking language (not academic prose)

---

### Task 13: Rehearsal and Timing

Rehearse the presentation and verify timing.

- [ ] Rehearsal 1: Solo run-through with timer
  - [ ] Record total time
  - [ ] Note slides that run over or under allocation
  - [ ] Identify pacing issues or unclear transitions
- [ ] Adjust slide content and speaker notes based on Rehearsal 1
- [ ] Rehearsal 2: Run-through with revised content
  - [ ] Verify total time is 14-15 minutes
  - [ ] Check that no individual slide exceeds its allocation by more than 15 seconds
- [ ] Rehearsal 3 (optional but recommended): Present to a peer or advisor
  - [ ] Collect feedback on clarity, pacing, and argument flow
  - [ ] Note any questions asked (add to Q&A preparation)
- [ ] Final adjustments based on all rehearsals

**Acceptance Criteria:**
- At least 2 full rehearsals completed with timing recorded
- Final rehearsal time is between 14:00 and 15:00
- No single slide exceeds its allocation by more than 15 seconds
- All pacing issues identified in Rehearsal 1 are resolved by Rehearsal 2

---

### Task 14: Quality Gate 5 Validation

Verify all presentation-ready criteria are met.

- [ ] All slides complete (13-14 content slides)
- [ ] Timing verified (rehearsal fits in 15 minutes)
- [ ] Backup slides prepared (at least 3 anticipatory Q&A slides)
- [ ] Narrative arc matches paper argument flow
- [ ] Visuals are clear (diagrams readable, minimal text per slide)
- [ ] Presentation success tests pass:
  - [ ] Full rehearsal completes in 14-15 minutes
  - [ ] Someone unfamiliar can follow argument from slides alone
  - [ ] Can answer "why these papers?" and "how does your proposal differ?" without hesitation
- [ ] Update `memory-bank/phases.md`: Phase 5 status to "Complete"
- [ ] Update `memory-bank/progress.md` with sprint completion

**Acceptance Criteria:**
- All Quality Gate 5 criteria checked and passing
- Memory bank updated to reflect Phase 5 completion
- Presentation is ready for the oral examination

---

## Content Mapping Reference

How the final paper maps to presentation slides:

| Paper Section | Slides | Adaptation |
|---------------|--------|------------|
| Abstract | (none -- woven into motivation) | Not presented separately |
| Introduction | 2-3 | Condense to hook + scope |
| Background and Foundations | 4 | One visual diagram |
| Agentic Architectures | 5-6 | Comparison diagram |
| Knowledge Representation | 7-8 | Approach comparison |
| Autonomous Research | 9 | Capability overview |
| Synthesis and Gaps | 10 | Key findings + gaps (pivot slide) |
| Research Proposal | 11-12 | Problem + approach + contributions |
| Conclusion | 13 | One takeaway message |

---

## Presentation Principles (from Design Doc Section 7.2)

1. **High-level, not exhaustive** -- distill the paper, do not reproduce it
2. **Visual over textual** -- diagrams, tables, minimal bullets
3. **Same narrative arc** -- motivation -> survey -> gaps -> proposal -> significance
4. **Anticipate questions** -- backup slides for predictable Q&A topics

---

## Architecture Decisions

- ADR-001: Memory Bank Documentation Structure
- ADR-002: IEEE LaTeX with Modular Sections
- ADR-004: Thematic Literature Organization

---

## Dependencies

- Final IEEE conference paper (Quality Gate 4 passed)
- All 6 paper annotations (from Sprint 1)
- Paper-to-theme matrix (from Sprint 1)
- Compiled PDF published to GitHub Pages (from Sprint 3)

---

## Risks

| Risk | Likelihood | Impact | Mitigation | Status |
|------|-----------|--------|------------|--------|
| Presentation runs over 15 minutes | Medium | Medium | Rehearse with timer; cut slide content rather than rushing | Open |
| Diagrams are too complex for projection | Medium | Medium | Test all visuals at reduced scale; apply 7-element maximum | Open |
| Committee asks unanticipated question | Medium | Low | Broad preparation with written responses; honesty about limitations | Open |
| Narrative arc diverges from paper | Low | High | Use content mapping table as checklist; review paper before each rehearsal | Open |
| Technical issues during presentation | Low | Medium | Have PDF backup of slides; arrive early to test equipment | Open |
| Speaker notes feel scripted | Medium | Low | Write in natural language; rehearse enough to internalize, not memorize | Open |
