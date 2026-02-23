# Design Document: VT PhD Qualifier

**Status:** Complete
**Created:** 2026-02-20
**Author:** DJ Turner
**References:** ADR-001, ADR-002, ADR-003, ADR-004

---

## 1. Problem Statement

Produce two deliverables for the Virginia Tech PhD qualifying examination:

1. A 5-6 page IEEE conference paper surveying 6 papers on Agentic AI for Autonomous Research, synthesized by theme with a research proposal extending the surveyed work.
2. A 15-minute oral presentation with 5 minutes of Q&A covering high-level takeaways, research overview, and future directions.

The paper must demonstrate synthesis (not summary), surface gaps and tensions across the literature, and ground a concrete research proposal in those gaps. At least 3 of the 6 papers must come from the provided reading lists.

---

## 2. Paper Architecture

### 2.1 Page Budget

| Section | File | Target Length | Page Budget |
|---------|------|---------------|-------------|
| Abstract | `01-abstract.tex` | 150-200 words | ~0.25 pages |
| Introduction | `02-introduction.tex` | 3-4 paragraphs | 0.5-0.75 pages |
| Literature Assessment | `03-literature-review.tex` | 5 subsections | ~3.0 pages |
| Research Proposal | `04-research-proposal.tex` | 3 subsections | ~1.0 page |
| Conclusion | `05-conclusion.tex` | 2-3 paragraphs | ~0.25 pages |
| **Total** | | | **5.0-5.25 pages** |
| References | `references.bib` | Unlimited | Not counted |

The target of 5.0-5.25 pages of content leaves 0.75-1.0 pages of margin before hitting the 6-page maximum. This buffer accounts for figures, tables, or formatting expansion.

### 2.2 Argument Flow

The paper follows a single coherent argument arc:

```
Agentic AI is transforming research (Introduction)
    |
    v
Here is what the field has built so far (Lit Review: Background, Architectures, Knowledge)
    |
    v
Here is what autonomous research looks like today (Lit Review: Autonomous Research)
    |
    v
Here is what is missing (Lit Review: Synthesis & Gap Analysis)
    |
    v
Here is how to fill those gaps (Research Proposal)
    |
    v
This matters because... (Conclusion)
```

Every section must advance this arc. No section stands alone.

---

## 3. Section-by-Section Content Plan

### 3.1 Abstract (01-abstract.tex)

**Goal:** Provide a self-contained summary that a reader can use to decide whether to read the paper.

**Must accomplish:**
- State the research area (agentic AI for autonomous research)
- Describe the scope of the survey (6 papers, what themes they cover)
- Summarize the key finding from the synthesis (the primary gap or tension)
- State the proposed research direction in one sentence
- Close with the significance of the proposal

**Constraints:**
- 150-200 words exactly
- No citations in the abstract
- Write LAST, after all other sections are complete

**Dependencies:** All other sections must be final before writing the abstract.

### 3.2 Introduction (02-introduction.tex)

**Goal:** Motivate the reader to care about agentic AI for research, define the scope of the survey, and preview the paper structure.

**Must accomplish:**
- Paragraph 1: Open with the broader context -- LLMs are enabling a new class of autonomous agents that can conduct research tasks. Establish why this matters.
- Paragraph 2: Narrow the scope -- this survey focuses on how agentic systems combine knowledge representation, multi-agent coordination, and autonomous reasoning for research progression. Define key terms.
- Paragraph 3: State the contribution -- this paper surveys 6 papers organized by theme, identifies gaps in the current landscape, and proposes research to address those gaps.
- Paragraph 4: Preview the structure -- brief roadmap of sections.

**Constraints:**
- 0.5-0.75 pages (do not exceed)
- Every claim needs a citation or is common knowledge
- Do not begin with "In recent years..." or similar cliches
- Must reference the 5 thematic subsections of the literature review by name

**Dependencies:** Thematic structure of literature review must be finalized first.

### 3.3 Literature Assessment (03-literature-review.tex)

**Goal:** Demonstrate mastery through thematic synthesis that surfaces connections, tensions, and gaps across all 6 papers.

This is the core of the paper. It must NOT read as 6 individual summaries. Every subsection weaves multiple papers together.

#### 3.3.1 Background and Foundations (~0.5 pages)

**Goal:** Establish the shared conceptual ground that all 6 papers build upon.

**Must accomplish:**
- Define foundational concepts: LLM-based agents, tool use, knowledge graphs, retrieval-augmented generation
- Explain why these building blocks matter for research automation
- Cite papers that depend on these foundations (all 6 papers should appear here at least once)
- Set up the vocabulary used throughout the rest of the review

**Key question this subsection answers:** "What does the reader need to know before understanding the surveyed work?"

#### 3.3.2 Agentic Architectures and Frameworks (~0.75 pages)

**Goal:** Compare and contrast how the surveyed papers design agents and multi-agent systems.

**Must accomplish:**
- Compare architectural patterns across papers (single-agent vs. multi-agent, role specialization, coordination mechanisms)
- Identify which papers propose frameworks vs. which use existing ones
- Highlight design trade-offs (autonomy vs. control, specialization vs. generality)
- Note what evaluation criteria papers use for their architectures

**Key question this subsection answers:** "How do researchers structure agentic systems for research tasks, and what trade-offs do they make?"

#### 3.3.3 Knowledge Representation and Reasoning (~0.75 pages)

**Goal:** Examine how agents acquire, store, and reason over structured knowledge.

**Must accomplish:**
- Compare knowledge representation approaches (knowledge graphs, vector stores, hybrid)
- Analyze how papers integrate retrieval with reasoning (RAG patterns, graph traversal, etc.)
- Identify the role of structured vs. unstructured knowledge
- Highlight how knowledge representation enables or limits agent capabilities

**Key question this subsection answers:** "How do agents manage the knowledge they need for research, and what are the limitations?"

#### 3.3.4 Autonomous Research and Discovery (~0.5 pages)

**Goal:** Examine the end-to-end research workflows that agents perform.

**Must accomplish:**
- Describe the research tasks that agents automate (literature review, hypothesis generation, experiment design, knowledge synthesis)
- Compare the scope of autonomy across papers (fully autonomous vs. human-in-the-loop)
- Assess how papers evaluate research quality and output
- Note what research domains are covered vs. missing

**Key question this subsection answers:** "What can research agents actually do today, and how well do they do it?"

#### 3.3.5 Synthesis and Gap Analysis (~0.5 pages)

**Goal:** Tie all themes together, surface cross-cutting patterns, and identify the gaps that motivate the research proposal.

**Must accomplish:**
- Identify 2-3 cross-cutting themes that span multiple subsections
- Surface tensions or contradictions between papers (e.g., different claims about agent autonomy, conflicting evaluation approaches)
- Identify 2-3 concrete gaps that no paper addresses adequately
- Rank gaps by significance and tractability
- The primary gap must directly motivate the research proposal

**Key question this subsection answers:** "What is missing from the current landscape, and what should be built next?"

**Dependencies:** This subsection must be written AFTER subsections 3.3.1-3.3.4. It is the bridge to the research proposal.

### 3.4 Research Proposal (04-research-proposal.tex)

**Goal:** Propose concrete research that extends the surveyed work, grounded in the gaps identified in Section 3.3.5.

#### 3.4.1 Problem Statement

**Must accomplish:**
- Reference the specific gap(s) from Section 3.3.5 by section label
- State the problem in 2-3 sentences
- Explain why existing approaches are insufficient (citing specific papers)
- Define the scope of the proposed research

#### 3.4.2 Proposed Approach

**Must accomplish:**
- Describe the high-level methodology (what you would build, study, or prove)
- Connect the approach to strengths from the surveyed papers (building on what works)
- Identify the key technical challenges
- Explain what makes this approach feasible

#### 3.4.3 Expected Contributions

**Must accomplish:**
- List 2-3 specific contributions
- Each contribution traces back to a gap from Section 3.3.5
- State how each contribution advances the state of the art
- Briefly note how contributions could be evaluated

**Constraints:**
- ~1 page total for the entire proposal section
- Must be concrete and specific (not "we will explore...")
- Must feel like a natural consequence of the literature review, not a separate idea

**Dependencies:** Synthesis and Gap Analysis (3.3.5) must be written first.

### 3.5 Conclusion (05-conclusion.tex)

**Goal:** Leave the reader with a clear understanding of what was learned and where the field is going.

**Must accomplish:**
- Summarize the key insight from the thematic synthesis (1-2 sentences)
- Restate the proposed research direction and why it matters
- Connect to the broader trajectory of agentic AI research
- Do NOT introduce new information

**Constraints:**
- ~0.25 pages (2-3 short paragraphs)
- No new citations
- Should echo the introduction's framing, creating a sense of closure

**Dependencies:** All other sections must be complete.

---

## 4. Paper Selection Strategy

### 4.1 Current State

| Slot | Paper | Source | Status |
|------|-------|--------|--------|
| 1 | Agentic Knowledge Graphs for Research Progression | Student-selected | Uploaded |
| 2 | Research4Agents | Student-selected | Uploaded |
| 3 | From Papers to Progress: Rethinking Knowledge Accumulation in SE | Student-selected | Uploaded |
| 4 | TBD | Must be from reading list | Candidate pool available |
| 5 | TBD | Must be from reading list | Candidate pool available |
| 6 | TBD | Flexible | Candidate pool available |

### 4.2 Selection Criteria

Each paper must satisfy at least one of:
- Contributes to agentic architectures and frameworks (Theme 2)
- Contributes to knowledge representation and reasoning (Theme 3)
- Contributes to autonomous research and discovery (Theme 4)
- Provides methodological or empirical foundations (Theme 1)

Additionally, the full set of 6 papers must:
- Cover at least 3 of the 4 content themes (Sections 3.3.1-3.3.4)
- Include at least 3 papers from the provided reading lists
- Contain at least 1 paper that challenges or contrasts with the others (to enable tension analysis)
- Be recent enough to reflect the current state of the art

### 4.3 Candidate Assessment

Papers available in `files/paperstoreview/`:

| Paper | Themes Covered | Reading List? | Fit Assessment |
|-------|---------------|---------------|----------------|
| Empirical Standards for SE Research | Foundations, methodology | Yes | Provides evaluation framework for assessing other papers |
| Open Problems in Mechanistic Interpretability | Foundations (tangential) | Yes | Low fit -- different research area |
| Get on the Train: Using LLMs for SE Research | Autonomous research, methodology | Yes | Strong fit -- LLMs in research context |
| Guidelines for Empirical Studies with LLMs | Foundations, methodology | Yes | Moderate fit -- methodological lens |
| The Denario Project | Architectures, knowledge, discovery | Yes | Strong fit -- end-to-end research agent |
| KG-based RAG for Cross-Document IE | Knowledge representation | Unknown | Strong fit -- KG + RAG integration |

### 4.4 Selection Decision Process

Selection happens in Sprint 1. The decision should maximize:
1. **Theme coverage** -- every theme has at least 2 papers contributing
2. **Reading list compliance** -- at least 3 from reading lists
3. **Tension potential** -- at least one paper that takes a different approach
4. **Narrative coherence** -- papers should tell a story together

---

## 5. Thematic Mapping Strategy

### 5.1 Mapping Process

After all 6 papers are selected and read, create a paper-to-theme matrix:

```
                     | Background | Architectures | Knowledge | Research | Gaps
---------------------|------------|---------------|-----------|----------|------
Paper 1 (Agentic KG) |     X      |       X       |     X     |    X     |
Paper 2 (R4Agents)   |     X      |       X       |           |    X     |
Paper 3 (Papers2Prog)|     X      |               |           |    X     |
Paper 4 (TBD)        |            |               |           |          |
Paper 5 (TBD)        |            |               |           |          |
Paper 6 (TBD)        |            |               |           |          |
```

**Rules:**
- Every paper must appear in at least 2 themes
- Every theme must have at least 2 papers
- If a theme has only 1 paper, either select a different paper or merge the theme

### 5.2 Annotation Template

For each paper, capture during reading:

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

### 5.3 Synthesis Moves

When writing each theme subsection, use these synthesis patterns:

| Pattern | Template | When to Use |
|---------|----------|-------------|
| Agreement | "Both [A] and [B] demonstrate that..." | Papers converge on a finding |
| Contrast | "While [A] employs X, [B] takes a different approach with Y..." | Papers diverge on method |
| Extension | "[B] extends the work of [A] by adding..." | One paper builds on another |
| Tension | "[A] claims X, yet [B]'s findings suggest..." | Papers disagree |
| Gap | "Neither [A] nor [B] addresses..." | Identifying what is missing |
| Cluster | "Several approaches [A, B, C] share the pattern of..." | Multiple papers align |

---

## 6. Research Proposal Design

### 6.1 Gap-to-Proposal Pipeline

```
Literature Review Subsections 3.3.1-3.3.4
    |
    v  (each subsection identifies local limitations)
    |
Synthesis & Gap Analysis (3.3.5)
    |
    v  (aggregates into 2-3 major gaps, ranks by significance)
    |
Primary Gap Selection
    |
    v  (most significant + tractable gap becomes the focus)
    |
Problem Statement (4.1)
    |
    v  (grounded in specific citations and gaps)
    |
Proposed Approach (4.2)
    |
    v  (builds on strengths from surveyed work)
    |
Expected Contributions (4.3)
    |
    v  (each maps back to a gap)
```

### 6.2 Proposal Quality Criteria

The research proposal must satisfy:

- [ ] Problem statement references specific gaps by section label
- [ ] Problem is not already solved by any of the 6 papers
- [ ] Approach builds on strengths identified in the survey
- [ ] Approach is concrete enough to be actionable (not "explore" or "investigate")
- [ ] Each contribution maps to a specific gap
- [ ] Contributions are evaluable (how would you know if they succeeded?)
- [ ] Proposal fits in ~1 page

---

## 7. Presentation Design

### 7.1 Slide Structure and Timing

Total time: 15 minutes presentation + 5 minutes Q&A

| Slide(s) | Content | Time | Notes |
|-----------|---------|------|-------|
| 1 | Title slide | 0:15 | Name, title, advisor, date |
| 2 | Motivation and context | 1:30 | Why agentic AI for research matters -- hook the audience |
| 3 | Scope and paper selection | 1:00 | The 6 papers, why these, what they cover |
| 4 | Background concepts | 1:30 | Key terms: agents, KGs, RAG -- visual diagram |
| 5-6 | Agentic architectures | 2:00 | Architecture comparison diagram, trade-offs |
| 7-8 | Knowledge representation | 2:00 | How agents manage knowledge, approaches compared |
| 9 | Autonomous research capabilities | 1:30 | What agents can do today, scope of autonomy |
| 10 | Synthesis and gaps | 2:00 | Cross-cutting findings, key tensions, primary gaps -- this is the pivot |
| 11-12 | Research proposal | 2:00 | Problem, approach, expected contributions |
| 13 | Conclusion and future directions | 1:00 | Key takeaway, broader significance |
| 14 | Questions | 0:15 | Transition to Q&A |
| | **Total** | **15:00** | |

### 7.2 Presentation Principles

- **High-level, not exhaustive:** The presentation distills the paper, it does not reproduce it. Focus on insights, not mechanics.
- **Visual over textual:** Use diagrams for architecture comparisons, tables for paper-to-theme mappings, and minimal bullet points.
- **Narrative arc:** The presentation follows the same argument flow as the paper (motivation -> survey -> gaps -> proposal -> significance).
- **Anticipate questions:** Prepare backup slides for common Q&A topics:
  - Why these 6 papers?
  - How does your proposal differ from [specific paper]?
  - What are the limitations of your proposed approach?
  - How would you evaluate the proposal?

### 7.3 Content Mapping from Paper to Presentation

| Paper Section | Presentation Coverage | Adaptation |
|---------------|----------------------|------------|
| Abstract | Not presented separately | Woven into motivation |
| Introduction | Slides 2-3 | Condense to hook + scope |
| Background & Foundations | Slide 4 | One visual diagram |
| Agentic Architectures | Slides 5-6 | Comparison diagram |
| Knowledge Representation | Slides 7-8 | Approach comparison |
| Autonomous Research | Slide 9 | Capability overview |
| Synthesis & Gaps | Slide 10 | Key findings + gaps |
| Research Proposal | Slides 11-12 | Problem + approach |
| Conclusion | Slide 13 | One takeaway message |

---

## 8. Writing Workflow and Dependencies

### 8.1 Dependency Graph

```
Paper Selection & Reading (Sprint 1)
    |
    +---> Paper Annotations (per-paper notes using template from 5.2)
    |
    +---> Paper-to-Theme Matrix (Section 5.1)
    |
    v
Literature Review Writing (Sprint 2)
    |
    +---> 3.3.1 Background & Foundations
    |         |
    +---> 3.3.2 Agentic Architectures     (can parallel with 3.3.3)
    |         |
    +---> 3.3.3 Knowledge Representation   (can parallel with 3.3.2)
    |         |
    +---> 3.3.4 Autonomous Research        (depends on 3.3.2, 3.3.3)
    |         |
    +---> 3.3.5 Synthesis & Gap Analysis   (depends on 3.3.1-3.3.4)
    |
    v
Research Proposal (Sprint 3)
    |
    +---> 3.4.1 Problem Statement          (depends on 3.3.5)
    |         |
    +---> 3.4.2 Proposed Approach          (depends on 3.4.1)
    |         |
    +---> 3.4.3 Expected Contributions     (depends on 3.4.2)
    |
    v
Paper Completion (Sprint 3, continued)
    |
    +---> Introduction                     (depends on lit review structure)
    |
    +---> Conclusion                       (depends on proposal)
    |
    +---> Abstract                         (depends on ALL other sections)
    |
    +---> Final polish and page check
    |
    v
Presentation (Sprint 4)
    |
    +---> Slide content                    (depends on final paper)
    |
    +---> Rehearsal and timing
    |
    +---> Backup slides for Q&A
```

### 8.2 Critical Path

The critical path through the project is:

```
Paper Selection -> Paper Reading -> Lit Review (3.3.1-3.3.5) -> Proposal -> Abstract -> Polish
```

The longest sequential chain is the literature review, which requires all 5 subsections written in partial sequence. Subsections 3.3.2 and 3.3.3 can be written in parallel, but 3.3.4 and 3.3.5 are strictly sequential.

### 8.3 Parallelizable Work

| Task A | Task B | Can Parallel? |
|--------|--------|---------------|
| Reading Paper 1 | Reading Paper 2 | Yes |
| Lit Review 3.3.2 | Lit Review 3.3.3 | Yes |
| Introduction | Conclusion | No (conclusion depends on proposal) |
| Paper polish | Presentation slides | No (slides depend on final paper) |
| BibTeX entries | Paper annotations | Yes |

---

## 9. Quality Gates

### 9.1 Gate 1: Paper Selection Complete

**Checkpoint:** Before any writing begins.

| Criterion | Check |
|-----------|-------|
| 6 papers selected | Count = 6 |
| 3+ from reading lists | Count reading-list papers >= 3 |
| All papers uploaded to `files/` | All PDFs present |
| All BibTeX entries complete | No TODO in `references.bib` |
| Paper-to-theme matrix populated | Every paper in 2+ themes, every theme has 2+ papers |
| Per-paper annotations complete | All 6 annotation templates filled |

### 9.2 Gate 2: Literature Review Draft

**Checkpoint:** Before writing the research proposal.

| Criterion | Check |
|-----------|-------|
| All 5 subsections drafted | No TODO placeholders remain |
| All 6 papers cited | Each paper appears in `\cite{}` at least twice |
| Synthesis patterns used | At least 3 different synthesis moves from Section 5.3 |
| Gap analysis identifies 2-3 gaps | Gaps are concrete and specific |
| Page count | ~3 pages (2.75-3.25 acceptable) |
| LaTeX compiles cleanly | No errors or warnings |

### 9.3 Gate 3: Research Proposal Draft

**Checkpoint:** Before writing introduction, conclusion, and abstract.

| Criterion | Check |
|-----------|-------|
| Problem statement references gaps | Explicit `\ref{sec:lit-synthesis}` |
| Approach is concrete | Describes what to build/study/prove |
| Contributions map to gaps | Each contribution traces to a specific gap |
| Page count | ~1 page (0.75-1.25 acceptable) |

### 9.4 Gate 4: Complete Paper

**Checkpoint:** Before starting presentation preparation.

| Criterion | Check |
|-----------|-------|
| All sections complete | No TODO placeholders anywhere |
| Abstract 150-200 words | Word count verified |
| Total page count 5-6 pages | Excluding references |
| All citations resolve | No `[?]` in compiled PDF |
| No orphan/widow lines | Visual inspection of PDF |
| Paper compiles cleanly | `latexmk` succeeds with no errors |
| Argument arc is coherent | Read-through from intro to conclusion flows |
| Published to GitHub Pages | CI/CD pipeline succeeds |

### 9.5 Gate 5: Presentation Ready

**Checkpoint:** Before the oral examination.

| Criterion | Check |
|-----------|-------|
| All slides complete | 13-14 slides as planned |
| Timing verified | Rehearsal fits in 15 minutes |
| Backup slides prepared | At least 3 anticipatory Q&A slides |
| Narrative arc matches paper | Same argument flow |
| Visuals are clear | Diagrams readable, minimal text per slide |

---

## 10. Sprint Mapping

This design maps to 4 sprints:

| Sprint | Phase | Goal | Inputs | Outputs |
|--------|-------|------|--------|---------|
| Sprint 1 | Phase 1 | Paper selection and reading | Candidate papers, reading lists | 6 selected papers, annotations, theme matrix, complete BibTeX |
| Sprint 2 | Phase 2 | Literature review | Annotations, theme matrix | 3-page literature assessment (all 5 subsections) |
| Sprint 3 | Phases 3-4 | Research proposal and paper completion | Lit review (esp. gap analysis) | Proposal, introduction, conclusion, abstract, polished paper |
| Sprint 4 | Phase 5 | Presentation | Final paper | Slide deck, rehearsal, backup slides |

Each sprint should be created using `create-sprint` when the preceding quality gate is passed.

---

## 11. Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Papers do not cluster into themes cleanly | Medium | High | Adjust thematic subsections after reading; themes are flexible per ADR-004 |
| Page budget exceeded | Medium | Medium | Track page count per subsection during writing; trim Background first |
| Page budget underutilized | Low | Medium | Expand Synthesis & Gap Analysis or add a comparison table |
| Research proposal feels disconnected | Medium | High | Write gap analysis before proposal; ensure explicit section references |
| Candidate papers from reading list are low relevance | Low | Medium | 6 candidates available; only need 1-2 more from list |
| Presentation runs over 15 minutes | Medium | Medium | Rehearse with timer; cut slide content rather than rushing |
| LaTeX compilation issues | Low | Low | CI/CD catches errors early; test locally before push |

---

## 12. Verification Plan

### How We Know the Paper Succeeds

1. **Synthesis test:** A reader of only the literature review should understand the landscape without reading any of the 6 papers individually.
2. **Gap test:** The gaps identified in Section 3.3.5 should feel inevitable after reading Sections 3.3.1-3.3.4.
3. **Proposal test:** The research proposal should feel like the obvious next step after reading the gap analysis.
4. **Coherence test:** Reading the introduction and then skipping to the conclusion should still make sense as a narrative arc.
5. **Independence test:** No subsection of the literature review should be readable as a standalone paper summary. Every subsection must weave multiple papers.

### How We Know the Presentation Succeeds

1. **Timing test:** Full rehearsal completes in 14-15 minutes.
2. **Clarity test:** Someone unfamiliar with the papers should follow the argument from slides alone.
3. **Q&A readiness:** Can answer "why these papers?" and "how does your proposal differ from X?" without hesitation.

---

## Appendix A: File Manifest

| File | Purpose | Modified By |
|------|---------|-------------|
| `proposal/main.tex` | Main document, includes all sections | Sprint 3 (polish) |
| `proposal/sections/01-abstract.tex` | Abstract | Sprint 3 |
| `proposal/sections/02-introduction.tex` | Introduction | Sprint 3 |
| `proposal/sections/03-literature-review.tex` | Literature assessment | Sprint 2 |
| `proposal/sections/04-research-proposal.tex` | Research proposal | Sprint 3 |
| `proposal/sections/05-conclusion.tex` | Conclusion | Sprint 3 |
| `proposal/references.bib` | Bibliography | Sprint 1 |
| `files/sources.md` | Paper source tracking | Sprint 1 |
| `memory-bank/phases.md` | Phase status tracking | Every sprint |
| `memory-bank/activeContext.md` | Current work state | Every sprint |
| `memory-bank/progress.md` | Task completion | Every sprint |

## Appendix B: References

- ADR-001: Memory Bank Documentation Structure
- ADR-002: IEEE LaTeX with Modular Sections
- ADR-003: GitHub Actions CI/CD Pipeline
- ADR-004: Thematic Literature Organization
- Qualifier Requirements: https://chbrown13.github.io/qualifier.html
