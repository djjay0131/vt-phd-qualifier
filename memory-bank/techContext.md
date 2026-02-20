# Technical Context: VT PhD Qualifier

## Document Infrastructure

### LaTeX Setup
- **Format**: IEEE conference paper (`\documentclass[conference]{IEEEtran}`)
- **Bibliography**: BibTeX with `IEEEtran.bst`
- **Modular sections**: Each section in `proposal/sections/`
- **Build**: `latexmk` via GitHub Actions

### Repository Structure

```text
vt-phd-qualifier/
├── README.md                  # Project overview
├── CLAUDE.md                  # Session tracking
├── .github/
│   └── workflows/
│       └── build-and-publish-pdf.yml  # CI/CD pipeline
├── .claude/
│   └── agents/                # Specialized agents (13 total)
├── memory-bank/               # Documentation system
├── construction/              # Project management
├── files/                     # Uploaded reference papers
│   ├── Agentic_Knowledge_Graphs_for_Research_Progression.pdf
│   └── Research4Agents (4).pdf
└── proposal/                  # LaTeX source files
    ├── main.tex               # Main document
    ├── references.bib         # Bibliography
    └── sections/              # Modular sections
        ├── 01-abstract.tex
        ├── 02-introduction.tex
        ├── 03-literature-review.tex
        ├── 04-research-proposal.tex
        └── 05-conclusion.tex
```

### CI/CD Pipeline

- **GitHub Actions**: Automated LaTeX compilation on push to `main`
- **GitHub Pages**: PDF published at `djjay0131.github.io/vt-phd-qualifier/`
- **Releases**: Versioned PDFs attached to GitHub releases

### Tools

| Tool | Purpose | Status |
|------|---------|--------|
| LaTeX (IEEEtran) | Paper formatting | Active |
| BibTeX | Bibliography management | Active |
| Git | Version control | Active |
| GitHub Actions | CI/CD pipeline | Active |
| GitHub Pages | PDF publishing | Active |
| Claude Code | AI-assisted writing | Active |

## LaTeX Section Files

| File | Section | Target Length |
|------|---------|--------------|
| `01-abstract.tex` | Abstract | ~150-200 words |
| `02-introduction.tex` | Introduction | ~0.5-0.75 pages |
| `03-literature-review.tex` | Literature Assessment | ~3 pages |
| `04-research-proposal.tex` | Research Proposal | ~1 page |
| `05-conclusion.tex` | Conclusion | ~0.25 pages |

## Dependencies

### LaTeX Packages
- `IEEEtran` class
- `cite`, `amsmath`, `amssymb`, `graphicx`
- `hyperref`, `booktabs`, `balance`

### External Resources
- Qualifier requirements: https://chbrown13.github.io/qualifier.html
- IEEE LaTeX template
- 6 selected research papers (2 uploaded, 4 TBD)

## Notes

- GitHub Pages deployment requires enabling Pages in repo settings (Settings > Pages > Source: GitHub Actions)
- The `xu-cheng/latex-action@v3` handles LaTeX compilation in CI
- References do NOT count toward the 5-6 page limit
