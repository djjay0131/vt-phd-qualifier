# Paper-to-Theme Matrix

**Survey Theme:** Agentic AI for Autonomous Research

**Coverage rules:** Every paper in ≥2 themes; every theme has ≥2 papers.

---

## Themes

| ID | Theme | Design Doc Section |
|----|-------|-------------------|
| T1 | Background and Foundations | §3.3.1 |
| T2 | Agentic Architectures and Frameworks | §3.3.2 |
| T3 | Knowledge Representation and Reasoning | §3.3.3 |
| T4 | Autonomous Research and Discovery | §3.3.4 |

---

## Matrix

**Legend:** `P` = Primary theme (main contribution), `S` = Secondary theme (significant contribution), `-` = Not applicable

| Paper | BibTeX Key | T1: Foundations | T2: Agentic Arch | T3: Knowledge Rep | T4: Autonomous Research |
|-------|------------|:--------------:|:----------------:|:-----------------:|:-----------------------:|
| Empirical Standards for SE Research (Ralph et al., 2021) | `ralph2021empirical` | **P** | - | S | - |
| Open Problems in Mechanistic Interpretability (Sharkey et al., 2025) | `sharkey2025mechanistic` | **P** | S | **P** | - |
| Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025) | `trinkenreich2025train` | S | **P** | - | **P** |
| Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025) | `baltes2025guidelines` | **P** | - | - | S |
| The Denario Project (Villaescusa-Navarro et al., 2025) | `villaescusa2025denario` | - | **P** | S | **P** |
| KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025) | `suryawanshi2025kgrag` | - | S | **P** | S |

### Theme Coverage Counts

| Theme | Primary Papers | Secondary Papers | Total |
|-------|---------------|-----------------|-------|
| T1: Foundations | Ralph, Sharkey, Baltes (3) | Trinkenreich (1) | 4 |
| T2: Agentic Architectures | Trinkenreich, Denario (2) | Sharkey, KG-RAG (2) | 4 |
| T3: Knowledge Representation | Sharkey, KG-RAG (2) | Ralph, Denario (2) | 4 |
| T4: Autonomous Research | Trinkenreich, Denario (2) | Baltes, KG-RAG (2) | 4 |

**Coverage check:** All rules satisfied ✓

---

## Paper Theme Justifications

### T1: Background and Foundations

**Primary:**
- **Ralph et al.**: Provides the methodological quality framework for empirical SE research — the pre-LLM baseline against which all AI-assisted research must be evaluated. Essential for contextualizing why rigorous standards matter for agentic research systems.
- **Sharkey et al.**: Provides foundational understanding of LLM capabilities and limitations (superposition, feature circuits, emergent behaviors) that underpins all agentic AI systems. Understanding what LLMs can and cannot represent is foundational for building reliable research agents.
- **Baltes et al.**: Directly extends and updates the foundational SE research standards (Ralph et al.) to the LLM era. Bridges the pre-LLM and LLM-era research standards landscape.

**Secondary:**
- **Trinkenreich et al.**: Provides context for how AI/LLMs are transforming SE research practices — the "why now" background for the survey's central argument.

### T2: Agentic Architectures and Frameworks

**Primary:**
- **Trinkenreich et al.**: Surveys and advocates for using LLM-based frameworks (agents, chains, tools) to automate SE research tasks. Identifies specific tools and use cases.
- **Denario et al.**: The central case study of a multi-agent research system. Planning & Control orchestration, modular pipeline (Idea → Literature → Methods → Analysis → Paper → Review), AG2/LangGraph frameworks.

**Secondary:**
- **Sharkey et al.**: Understanding LLM internal representations (features, circuits) is directly relevant to designing robust agent systems — interpretability enables better architecture decisions.
- **Suryawanshi et al.**: A 5-stage pipeline architecture (chunking → KG construction → community detection → summarization → retrieval) represents a simpler, non-agentic but structured framework for research knowledge retrieval.

### T3: Knowledge Representation and Reasoning

**Primary:**
- **Sharkey et al.**: Studies how LLMs internally represent knowledge — linear representation hypothesis, superposition, feature circuits, world models. These sub-symbolic, distributed representations are a foundational question for knowledge-based AI.
- **Suryawanshi et al.**: Proposes explicit, symbolic knowledge graph construction from research papers. 2,601 entities, 3,052 relations, community detection. Represents the external/explicit pole of the knowledge representation spectrum.

**Secondary:**
- **Ralph et al.**: The empirical standards framework is itself a structured knowledge representation — methodology-specific checklists encode implicit community knowledge as explicit, modular, machine-processable criteria. Analogous conceptually to KG construction.
- **Denario et al.**: Represents knowledge implicitly through LLM weights and session context (no persistent KG). Contrasts with Suryawanshi et al.'s explicit approach — key tension point for synthesis.

### T4: Autonomous Research and Discovery

**Primary:**
- **Trinkenreich et al.**: Directly argues that SE researchers should adopt LLM tools to automate research sub-tasks (literature reviews, data analysis, paper writing). Positions LLMs as research *tools* for human-directed research.
- **Denario et al.**: Goes further — positions LLMs as research *agents* capable of end-to-end autonomous paper generation. Tests this across 13 disciplines with expert evaluation.

**Secondary:**
- **Baltes et al.**: Addresses the empirical study of LLMs *as research subjects* — directly relevant to how autonomous research systems should be evaluated, what protocols to follow, and what validity threats to guard against.
- **Suryawanshi et al.**: Demonstrates automated cross-document information extraction from research papers — a component capability toward autonomous literature synthesis and research knowledge building.

---

## Tension and Contrast Points

### Productive Tensions for Literature Synthesis

| Tension | Papers Involved | Theme |
|---------|----------------|-------|
| **Pre-LLM standards vs. LLM-era needs**: Ralph's framework (2021) does not address LLM studies; Baltes fills this gap — but the tension reveals how fast the field moves. | Ralph ↔ Baltes | T1 |
| **Explicit vs. implicit knowledge**: KG-RAG builds structured, queryable knowledge graphs; Denario stores knowledge ephemerally in LLM context — fundamentally different epistemics. | KG-RAG ↔ Denario | T3 |
| **LLMs as tools vs. LLMs as agents**: Trinkenreich advocates human-directed LLM tool use; Denario attempts full autonomy — with honest admission of current limitations. | Trinkenreich ↔ Denario | T4 |
| **Transparency vs. capability**: Sharkey argues for mechanistic understanding of LLMs; Denario and large agentic systems operate as black boxes — the interpretability gap is a reliability threat. | Sharkey ↔ Denario | T2, T3 |
| **Empirical rigor vs. rapid demonstration**: Denario's evaluation (single-expert scores, no baselines, no IRR) fails the standards Ralph and Baltes prescribe — the system for automating research doesn't meet research standards. | Ralph/Baltes ↔ Denario | T1, T4 |

---

## Cross-Cutting Patterns for Synthesis

### Pattern 1: The Autonomy Spectrum
Papers span a clear spectrum of automation in research:
- **Fully human, standard-guided**: Ralph et al. (human researchers using structured checklists)
- **LLM-assisted, human-directed**: Trinkenreich et al. (humans using LLMs as tools)
- **LLM-constrained methodology**: Baltes et al. (structured protocols for LLM-involving studies)
- **Structured knowledge retrieval**: KG-RAG (automated IE but no autonomous research action)
- **Autonomous multi-agent research**: Denario (end-to-end without human-in-the-loop)
- **Foundational capability understanding**: Sharkey et al. (what's possible and what's not in current LLMs)

### Pattern 2: The Transparency-Capability Tradeoff
Every paper touches on a tension between transparency/interpretability and raw capability:
- KG-RAG: highly transparent (explicit graph), lower capability (no autonomy)
- Denario: high capability (autonomous research), opaque (black-box LLM reasoning)
- Sharkey: proposes research program to close this gap (interpretability tools for LLMs)
- Ralph/Baltes: transparency through structured methodology standards

### Pattern 3: Standards Lag Innovation
A recurring theme is that formal standards (Ralph's SE empirical standards, Baltes's LLM guidelines) consistently trail the capabilities being studied:
- Ralph's 2021 standards lack LLM methodology → Baltes addresses in 2025
- Baltes's 2025 guidelines don't yet cover agentic research systems like Denario
- Denario's evaluation fails to meet either standard → the autonomy frontier outpaces quality frameworks

### Pattern 4: Knowledge Externalization
All papers grapple with whether scientific knowledge should be:
- **Implicit** (in LLM weights, distributed, not directly inspectable) — Denario, Sharkey (problem)
- **Explicit** (in structured external stores, queryable, auditable) — KG-RAG, Ralph's checklists
This is a fundamental architectural and epistemological choice with implications for reproducibility, interpretability, and cumulative scientific progress.

---

## Proposed Literature Review Section Outline

Based on this matrix, the literature review section (Section 3) should be organized as:

| Subsection | Theme | Primary Papers | Key Tension |
|------------|-------|----------------|-------------|
| §3.1 Foundations for Rigorous AI Research | T1 | Ralph, Baltes | Standards lag innovation |
| §3.2 Agentic Architectures for Research Tasks | T2 | Trinkenreich, Denario | Tools vs. agents |
| §3.3 Knowledge Representation Strategies | T3 | Sharkey, KG-RAG | Explicit vs. implicit |
| §3.4 Toward Autonomous Research Systems | T4 | Denario, Trinkenreich | Depth vs. breadth |

*Note: This outline is preliminary and subject to refinement during Sprint 2 writing. See design document Section 3.3 for detailed subsection content plans.*
