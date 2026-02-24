# Architectural Decisions

This file tracks significant decisions made throughout the project lifecycle.

## Decision Format

Each decision should include:
- **Date:** When the decision was made
- **Status:** Proposed | Accepted | Deprecated | Superseded
- **Context:** What prompted this decision
- **Decision:** What was decided
- **Consequences:** Impact and trade-offs
- **Alternatives Considered:** Other options evaluated

---

## ADR-001: Memory Bank Documentation Structure

**Date:** 2026-02-20
**Status:** Accepted

**Context:**
Need a systematic documentation approach that maintains context across sessions for writing the qualifier paper.

**Decision:**
Adopt the memory-bank documentation structure from the construction-ai-proposal project.

**Consequences:**
- Pros: Proven structure, comprehensive coverage, easy context recovery
- Cons: Requires discipline to maintain
- Impact: Better organization across writing sessions

---

## ADR-002: IEEE LaTeX with Modular Sections

**Date:** 2026-02-20
**Status:** Accepted

**Context:**
Qualifier requires IEEE conference format. Need a maintainable LaTeX setup for iterative writing.

**Decision:**
Use `IEEEtran` document class with modular section files in `proposal/sections/`, matching the pattern from construction-ai-proposal:
- `01-abstract.tex` through `05-conclusion.tex`
- Separate `references.bib` for bibliography
- Main document (`main.tex`) uses `\input{}` for each section

**Consequences:**
- Pros: Easy to edit individual sections, clean git diffs, proven workflow
- Cons: Slightly more files to manage than single-file approach
- Impact: Efficient collaborative/iterative writing process

---

## ADR-003: GitHub Actions CI/CD Pipeline

**Date:** 2026-02-20
**Status:** Accepted

**Context:**
Need automated PDF compilation and easy sharing with committee. Construction-ai-proposal had a working pipeline.

**Decision:**
Implement GitHub Actions workflow with:
- Automated LaTeX compilation on push to `main`
- GitHub Pages deployment for public PDF access
- GitHub Releases with versioned PDFs

**Consequences:**
- Pros: No local LaTeX required, easy sharing via URL, build verification
- Cons: Requires GitHub Pages enabled in repo settings
- Impact: Professional delivery, automated quality gate

---

## ADR-004: Thematic Literature Organization

**Date:** 2026-02-20
**Status:** Accepted

**Context:**
Qualifier requires "insightful literature survey" that synthesizes papers into a "coherent framework." Need to avoid the trap of paper-by-paper summaries.

**Decision:**
Organize literature review by theme rather than by paper:
- Background & Foundations
- Agentic Architectures & Frameworks
- Knowledge Representation & Reasoning
- Autonomous Research & Discovery
- Synthesis & Gap Analysis

Subsections may be adjusted once all 6 papers are selected and read.

**Consequences:**
- Pros: Demonstrates synthesis, surfaces connections and gaps naturally
- Cons: Harder to write than sequential summaries
- Impact: Stronger qualifier paper that shows analytical ability

**Alternatives Considered:**
- Paper-by-paper summaries: Rejected, doesn't meet "insightful synthesis" requirement
- Chronological organization: Rejected, less useful for identifying themes and gaps

---

## Template for Future Decisions

```markdown
## ADR-XXX: [Decision Title]

**Date:** YYYY-MM-DD
**Status:** Proposed | Accepted | Deprecated | Superseded

**Context:**
[What is the issue that we're seeing that is motivating this decision or change?]

**Decision:**
[What is the change that we're actually proposing or doing?]

**Consequences:**
- Pros: [Positive outcomes]
- Cons: [Negative outcomes or trade-offs]
- Impact: [Overall impact on the project]

**Alternatives Considered:**
- [Alternative 1]: [Why rejected]
- [Alternative 2]: [Why rejected]
```

---

## Notes

- Update this file when making significant decisions
- Reference ADR numbers when discussing decisions elsewhere
