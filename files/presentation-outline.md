# PhD Oral Presentation  
## Agentic Knowledge Graphs for Research Progression

**Total Time:** 15 minutes  
**Structure:** Literature-Centered Survey → Synthesis → Proposal Direction  

---

# SECTION 1 — Motivation (3 Slides)

## Slide 1 — Research State Is Ephemeral
- Research reasoning is fragmented and transient
- LLM-assisted workflows amplify volatility
- Structural memory is missing

## Slide 2 — The Structural Gaps
- Persistence
- Traceability
- Evaluability
- These are infrastructure problems, not model-quality problems

## Slide 3 — Guiding Question
How can research state be made persistent, traceable, and empirically evaluable in AI-assisted workflows?

---

# SECTION 2 — Literature Survey (8–9 Slides)

## Slide 4 — Landscape Overview
Domains surveyed:
- Mechanistic Interpretability
- Retrieval-Augmented Generation (RAG)
- Knowledge Graph Systems
- Agentic Systems
- Empirical Evaluation Standards

---

## Slide 5 — Mechanistic Interpretability
Key ideas:
- Reverse engineering internal representations
- Sparse dictionary learning
- Structural decomposition

Limitations:
- Focused on model internals
- No persistent research-state modeling

---

## Slide 6 — Concept-Based Interpretability
- Probes and representation alignment
- Correlation vs causation concerns
- Limited persistence mechanisms

---

## Slide 7 — RAG & Vector Memory Systems
Strengths:
- Scalable retrieval
- Semantic similarity

Limitations:
- No structured reasoning
- No canonical memory
- No provenance chain
- No longitudinal state

---

## Slide 8 — Knowledge Graph Research
Strengths:
- Ontology-based structure
- Provenance modeling
- Logical relationships

Limitations:
- Manual curation
- Static graphs
- No automated maintenance

---

## Slide 9 — Agentic Systems
- Autonomous task execution
- Tool orchestration

Limitations:
- Ephemeral memory
- No structural persistence
- Weak auditability

---

## Slide 10 — Empirical Evaluation Standards
- Need for explicit baselines
- Human validation
- Reproducibility artifacts
- Longitudinal evaluation

Observation:
Many systems lack structured validation frameworks.

---

## Slide 11 — Cross-Cutting Gaps in the Literature
Across domains:

- Retrieval lacks structure
- Graphs lack automation
- Agents lack persistent memory rigor
- Evaluation lacks longitudinal validation

This fragmentation motivates new infrastructure.

---

# SECTION 3 — Relation to My Work (2 Slides)

## Slide 12 — Positioning My Work
Intersection:
- Agentic systems
- Knowledge graph persistence
- Span-level traceability

Literature refined:
- Need for stronger evaluation
- Clearer scope (SE focus)
- Explicit longitudinal testing

---

# SECTION 4 — Proposed Research Direction (4 Slides)

## Slide 13 — Proposed Architecture
Human → Agent → Knowledge Graph → Agent → Human

Persistent research state loop.

---

## Slide 14 — Core Innovation
- Span-level evidence alignment
- Canonicalization agent
- Versioned provenance chains

---

## Slide 15 — Evaluation Framework
Validation Matrix:

| Claim | Metric | Baseline |
|-------|--------|----------|
| Span-level alignment | Precision/Recall/F1 | RAG |
| Canonicalization | Cohen’s κ | Embedding clustering |
| Traceability | Audit completeness % | RAG |
| Persistence | Retention accuracy | Chat-only LLM |

---

## Slide 16 — Experimental Design Overview
- Annotated span dataset
- Synthetic duplicate injection
- Human traceability audit
- 4-week longitudinal retention task
- Statistical comparison vs baseline

---

# SECTION 5 — Contributions & Future Directions (3 Slides)

## Slide 17 — Contributions
- Formal definition of Research State
- Agentic Curation Protocol
- Reference infrastructure implementation

---

## Slide 18 — Near-Term Work
- Controlled evaluation studies
- Artifact release
- SE-focused deployment

---

## Slide 19 — Long-Term Vision
- Cross-domain expansion
- Persistent AI-assisted research infrastructure
- Structured memory for scientific discovery

---

# Slide 20 — Conclusion
From fragmented chat interaction  
to persistent, traceable research state infrastructure.