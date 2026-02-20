# System Patterns: VT PhD Qualifier Paper

## Paper Architecture

### Document Structure (IEEE Conference Format, 5-6 pages)

```text
┌─────────────────────────────────────────────────────────┐
│  ABSTRACT + INTRODUCTION (~1 page)                      │
│  - Motivate agentic AI research area                    │
│  - Define scope and key terms                           │
│  - Preview paper structure                              │
├─────────────────────────────────────────────────────────┤
│  LITERATURE ASSESSMENT (~3 pages)                       │
│  ┌───────────────────────────────────────────────────┐  │
│  │ Background & Foundations                          │  │
│  │ - Core concepts underlying the surveyed papers    │  │
│  ├───────────────────────────────────────────────────┤  │
│  │ Agentic Architectures & Frameworks                │  │
│  │ - Agent design, multi-agent systems, coordination │  │
│  ├───────────────────────────────────────────────────┤  │
│  │ Knowledge Representation & Reasoning              │  │
│  │ - KGs, RAG, structured knowledge for agents       │  │
│  ├───────────────────────────────────────────────────┤  │
│  │ Autonomous Research & Discovery                   │  │
│  │ - AI-driven research, scientific automation       │  │
│  ├───────────────────────────────────────────────────┤  │
│  │ Synthesis & Gap Analysis                          │  │
│  │ - Cross-cutting themes, contradictions, gaps      │  │
│  └───────────────────────────────────────────────────┘  │
├─────────────────────────────────────────────────────────┤
│  RESEARCH PROPOSAL (~1 page)                            │
│  - Problem statement grounded in gaps                   │
│  - Proposed approach and methodology                    │
│  - Expected contributions                               │
├─────────────────────────────────────────────────────────┤
│  CONCLUSION (~0.25 pages)                               │
│  - Key takeaways from survey                            │
│  - Restate research direction                           │
├─────────────────────────────────────────────────────────┤
│  REFERENCES (unlimited, does not count toward pages)    │
└─────────────────────────────────────────────────────────┘
```

## Writing Patterns

### Literature Synthesis (NOT Summary)
- Group papers by **theme**, not one-by-one
- Find **connections** between papers (shared methods, complementary ideas)
- Identify **tensions** (conflicting claims, different approaches to same problem)
- Surface **gaps** (what no paper addresses, what's left unsolved)
- Build toward the research proposal

### Citation Integration
- Every claim backed by citation
- Use comparative language: "While [X] proposes..., [Y] takes a different approach..."
- Cluster related citations: "Several works address this challenge \cite{a, b, c}"
- Highlight where papers agree and disagree

### Research Proposal Flow
- Gap Analysis -> Problem Statement -> Approach -> Contributions
- Each contribution should trace back to a specific gap
- Be concrete: what would you build/study/prove?

## Development Workflow

### Writing Process
1. Read and annotate all 6 papers
2. Identify themes and create outline
3. Write literature review section by section
4. Write research proposal based on gaps
5. Write introduction and conclusion
6. Write abstract last
7. Polish and verify page count

### Quality Checks
- IEEE format compliance
- Page count: 5-6 pages (excluding references)
- All 6 papers cited and discussed meaningfully
- No orphan/widow lines
- Clean LaTeX compilation
- All citations resolve
