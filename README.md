# VT PhD Qualifier

Literature survey and research proposal for the Virginia Tech PhD Qualifying Examination.

**Topic:** Agentic AI for Autonomous Research

## Deliverables

- **IEEE Conference Paper** (5-6 pages) -- literature survey of 6 papers + research proposal
- **Oral Presentation** (15 min + 5 min Q&A)
- **Published PDF** via GitHub Pages

## Project Structure

```text
vt-phd-qualifier/
├── README.md                  # This file
├── CLAUDE.md                  # Session tracking
├── .github/workflows/         # CI/CD pipeline
├── .claude/agents/            # Specialized agents
├── memory-bank/               # Documentation system
├── construction/              # Project management
├── files/                     # Reference papers (PDFs)
└── proposal/                  # LaTeX source files
    ├── main.tex               # Main document (IEEE format)
    ├── references.bib         # Bibliography
    └── sections/              # Modular sections
        ├── 01-abstract.tex
        ├── 02-introduction.tex
        ├── 03-literature-review.tex
        ├── 04-research-proposal.tex
        └── 05-conclusion.tex
```

## Quick Start

1. Read `CLAUDE.md` for session context
2. Read `memory-bank/activeContext.md` for current state
3. Edit sections in `proposal/sections/`
4. Push to `main` to trigger PDF build and deploy

## Qualifier Requirements

Source: <https://chbrown13.github.io/qualifier.html>

- **6 papers** (3+ from provided reading lists)
- **5-6 pages** IEEE conference format (references excluded)
- Abstract + Introduction (~1 page)
- Literature Assessment (~3 pages)
- Research Proposal (~1 page)
- Conclusion

## Status

**Current Phase:** Paper Selection (Phase 1)

**Papers Selected:** 2/6

**Next Steps:** Select remaining papers, read and annotate, begin writing
