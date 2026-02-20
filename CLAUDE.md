# VT PhD Qualifier - Session Info

## Project Overview

Writing a 5-6 page IEEE conference paper for the Virginia Tech PhD qualifying exam. The paper is a literature survey of 6 selected papers on **Agentic AI for Autonomous Research**, with a research proposal extending the surveyed work.

## Documentation System

**IMPORTANT:** This project uses a Memory Bank documentation system. On context reset, read ALL files in `memory-bank/` to restore full project context.

### Quick Start

1. Read `memory-bank/activeContext.md` for current state
2. Read `memory-bank/progress.md` for task status
3. Read `memory-bank/projectbrief.md` for qualifier requirements

### Memory Bank Files

| File | Purpose |
|------|---------|
| `projectbrief.md` | Qualifier requirements and deliverables |
| `productContext.md` | Research area context and writing approach |
| `techContext.md` | LaTeX setup, CI/CD, repo structure |
| `systemPatterns.md` | Paper structure and writing patterns |
| `activeContext.md` | Current focus and next steps |
| `progress.md` | Task completion tracking |
| `phases.md` | Phase coordination |
| `architecturalDecisions.md` | Key decisions (ADR format) |

## Session Notes

- Started: 2026-02-20
- Status: Paper Setup Complete, Writing Phase Next
- Last Updated: 2026-02-20

## Current Phase

**Phase 1: Paper Selection** - Select remaining 4 papers, read and annotate all 6

## Completed Work

- [x] Phase 0: Project Setup (2026-02-20)
  - Repository, memory-bank, agents, LaTeX template, CI/CD

## Current Deliverables

- `proposal/main.tex` - IEEE conference paper (TODO placeholders)
- `proposal/sections/` - 5 modular section files
- `proposal/references.bib` - Bibliography (2/6 papers entered)
- `.github/workflows/build-and-publish-pdf.yml` - CI/CD pipeline

## Qualifier Requirements

- **Format:** IEEE conference paper, 5-6 pages (refs excluded)
- **Sections:** Abstract+Intro (~1p), Literature (~3p), Proposal (~1p), Conclusion
- **Papers:** 6 total, 3+ from reading lists
- **Oral:** 15-min presentation + 5-min Q&A

## Papers Selected (2/6)

1. Agentic Knowledge Graphs for Research Progression
2. Research4Agents
3. TBD
4. TBD
5. TBD
6. TBD

## CI/CD

- GitHub Actions: Automated PDF compilation on push to main
- GitHub Pages: (enable in repo settings: Settings > Pages > Source: GitHub Actions)

## Context

This file provides quick session tracking. For comprehensive project context, refer to the `memory-bank/` folder.
