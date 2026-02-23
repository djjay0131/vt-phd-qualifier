## Paper: Guidelines for Empirical Studies in Software Engineering involving Large Language Models

**Authors:** Sebastian Baltes, Florian Angermeir, Chetan Arora, Lukas Bohme, Fabio Calefato, Marvin Munoz Baron, Chunyang Chen, Neil Ernst, Davide Falessi, Brian Fitzgerald, Davide Fucci, Marcos Kalinowski, Stefano Lambiase, Daniel Russo, Mircea Lungu, Lutz Prechelt, Paul Ralph, Rijnard van Tonder, Christoph Treude, Stefan Wagner
**Year:** 2025
**Venue:** arXiv:2508.15503
**BibTeX Key:** baltes2025guidelines

### Summary (2-3 sentences)

This paper presents a community-driven effort to establish guidelines for designing and reporting empirical studies involving LLMs in software engineering research. It introduces a taxonomy of seven LLM-based study types (LLMs as Annotators, Judges, Synthesis tools, Subjects, and three categories of LLMs as tools for software engineers) and distills eight guidelines covering transparency, reproducibility, and validity. The guidelines use RFC 2119 must/should/may language and are maintained as a living resource at llm-guidelines.org, developed through an extensive coordination process involving 20 empirical SE experts.

### Key Contributions

- **Taxonomy of LLM study types:** A seven-category taxonomy organized into two groups: (1) LLMs as tools for SE researchers (Annotators, Judges, Synthesis, Subjects) and (2) LLMs as tools for software engineers (Studying LLM Usage, New SE Tools, Benchmarking LLMs for SE Tasks).
- **Eight actionable guidelines** with must/should/may criteria, each contextualized by study type:
  1. Declare LLM usage and role
  2. Report model version, configuration, and customizations
  3. Report tool architecture beyond models
  4. Report prompts, their development, and interaction logs
  5. Use human validation for LLM outputs
  6. Use an open LLM as a baseline
  7. Use suitable baselines, benchmarks, and metrics
  8. Report limitations and mitigations
- **Living resource model:** Guidelines are maintained online (llm-guidelines.org) with a public GitHub repository for community contributions.
- **Comprehensive exemplars:** Each study type and guideline includes published examples from SE and adjacent fields, plus discussion of advantages and challenges.

### Architecture/Method

The paper follows a structured community methodology:

1. **Origin:** Discussion sessions at the 2024 International Software Engineering Research Network (ISERN) meeting in Barcelona, followed by a position paper at WSESE 2025.
2. **Development process:** Bi-weekly meetings among 20 co-authors to refine the taxonomy and guidelines. At least two co-authors assigned to each study type and guideline, followed by internal peer review and external expert review.
3. **Taxonomy structure:** The seven study types are organized hierarchically:
   - **LLMs as Tools for SE Researchers:** Annotators (labeling artifacts), Judges (evaluating properties), Synthesis (integrating/distilling information), Subjects (simulating human behavior)
   - **LLMs as Tools for Software Engineers:** Studying LLM Usage, LLMs for New SE Tools, Benchmarking LLMs for SE Tasks
4. **Guideline structure:** Each guideline contains: tl;dr summary, detailed recommendations with must/should/may criteria, published examples, advantages, challenges, and mapping to relevant study types.
5. **RFC 2119 formalism:** The guidelines adopt the Internet Engineering Task Force's requirement level keywords (must, should, may) from RFC 2119 and RFC 8174 to clearly distinguish essential from desired criteria.

### Knowledge Representation Approach

This paper structures knowledge about LLM-based empirical research through a multi-layered organizational framework:

- **Taxonomy as knowledge schema:** The seven study types serve as a classification system that maps the space of how LLMs are used in SE research. Each study type has a well-defined description, examples, advantages, and challenges, creating a structured ontology of LLM research practices.
- **Guidelines as codified best practices:** The eight guidelines encode expert consensus as formalized rules with explicit requirement levels (must/should/may), transforming tacit community knowledge into explicit, actionable standards.
- **Cross-referencing between study types and guidelines:** Each guideline section ends with a "Study Types" subsection that contextualizes the guideline for each study type, creating a matrix-like knowledge structure.
- **Living document approach:** By maintaining guidelines as a versioned online resource with community input via GitHub, the paper represents knowledge as an evolving, collaboratively maintained artifact rather than a static publication.
- **Exemplar-based knowledge transfer:** Each section includes concrete published examples from SE and other fields, grounding abstract guidelines in real research practice.

### Research Tasks Addressed

- **Reproducibility crisis in LLM-based research:** Addresses the fundamental challenge that LLM non-determinism, opaque training data, and evolving model architectures make reproduction and replication of empirical studies extremely difficult.
- **Lack of standardized reporting:** Fills the gap of no existing holistic guidelines for conducting and reporting SE studies involving LLMs.
- **Validity threats:** Tackles threats to internal, external, and construct validity that are specific to LLM-based studies, including data leakage, benchmark contamination, model drift over time, and biases.
- **Open science for LLM research:** Provides a framework for transparency despite the inherently closed nature of many commercial LLMs, recommending open baselines, replication packages, and full interaction log disclosure.
- **Evaluation standardization:** Addresses the need for suitable benchmarks, metrics, and baselines for assessing LLM performance on SE tasks, including discussion of metrics like BLEU, pass@k, and inter-rater agreement measures.
- **Agentic tool evaluation:** Explicitly addresses challenges in studying agentic software development tools (e.g., Claude Code), including agent behavior traceability, tool-calling documentation, and human-in-the-loop validation.

### Evaluation Method

This paper is itself a set of guidelines rather than an empirical study, so it does not have a traditional evaluation. However, its validation approach includes:

- **Community expert development:** The guidelines were co-developed by 20 empirical SE researchers from institutions across 12 countries, ensuring broad expert consensus.
- **Iterative refinement:** Bi-weekly meetings with structured topic assignments, internal peer review, and external expert review.
- **Grounding in existing literature:** Each study type and guideline is supported by published research exemplars from SE and adjacent fields (145 references total).
- **Alignment with established frameworks:** The paper contextualizes itself relative to existing guidelines (e.g., TRIPOD-LLM for healthcare, ACM SIGSOFT Open Science Policies, Sallou et al.'s vision paper on validity threats in LLM-based SE research).
- **Living resource model:** Ongoing community validation through the public GitHub repository and llm-guidelines.org website.

### Strengths

- **Comprehensive coverage:** The taxonomy and guidelines cover the full spectrum of LLM use in SE research, from simple annotation tasks to complex agentic tool evaluation.
- **Practical and actionable:** The RFC 2119 must/should/may formalism makes it clear which criteria are essential vs. desired, making the guidelines directly usable by researchers and reviewers.
- **Well-structured cross-referencing:** The systematic mapping of guidelines to study types creates a useful matrix that helps researchers identify which guidelines apply to their specific study.
- **Forward-looking:** The paper explicitly addresses emerging challenges like agentic systems (Claude Code, GitHub Copilot), multi-agent architectures, and the Model Context Protocol, demonstrating awareness of the rapidly evolving LLM landscape.
- **Living resource:** The commitment to maintaining guidelines as a versioned, community-editable resource acknowledges that static guidelines would quickly become outdated given the pace of LLM development.
- **Strong author team:** 20 co-authors from major empirical SE research groups worldwide lends significant authority and represents genuine community consensus.
- **Explicit scope boundaries:** The paper is careful to define what is in scope (SE research, natural language LLMs, direct research/tool support) and out of scope (multimodal models, writing support, proofreading), avoiding overreach.

### Weaknesses/Limitations

- **No empirical validation of guideline adoption:** The paper does not measure whether following these guidelines actually improves reproducibility or study quality. There is no controlled experiment comparing studies that follow vs. do not follow the guidelines.
- **Potential for rapid obsolescence:** Despite the living resource model, the guidelines are anchored to the current LLM landscape (GPT-4, Llama, etc.). Fundamental architectural shifts (e.g., multimodal-first models, which are explicitly excluded) could limit applicability.
- **Compliance burden:** The comprehensive set of must/should/may criteria may be burdensome for researchers, especially those with limited resources, potentially discouraging adoption or leading to superficial compliance.
- **Limited scope to SE:** While the SE focus is intentional, the guidelines would benefit from broader interdisciplinary input, as many challenges (non-determinism, data leakage, benchmark contamination) are universal across disciplines using LLMs.
- **Excludes multimodal models:** The explicit exclusion of multimodal foundational models is a significant limitation given that modern LLMs increasingly handle images, audio, and video alongside text.
- **No enforcement mechanism:** Unlike the ACM Empirical Standards (Ralph et al., 2021), these guidelines do not have a formal role in the peer review process, making adoption voluntary.
- **Tension between openness and commercial reality:** The guideline to use open LLMs as baselines, while laudable for reproducibility, acknowledges that open models often lag behind commercial ones, potentially limiting the practical relevance of baseline comparisons.

### Connections to Other Papers

**Empirical Standards for SE Research (Ralph et al., 2021):**
This is the most direct connection. Ralph et al. established general empirical standards for SE research across multiple study types. Baltes et al. explicitly complement this work by addressing LLM-specific challenges that the original empirical standards did not anticipate. Paul Ralph is a co-author on both papers, ensuring continuity. Where Ralph et al. provide general methodology standards, Baltes et al. add an LLM-specific layer addressing non-determinism, model versioning, prompt reporting, and benchmark contamination. The two papers together form a layered framework: general empirical SE standards (Ralph et al.) plus LLM-specific addenda (Baltes et al.).

**Open Problems in Mechanistic Interpretability (Sharkey et al., 2025):**
Baltes et al.'s guidelines on reporting model versions, configurations, and limitations directly relate to the interpretability challenges Sharkey et al. identify. The "opaque training data" and "evolving architectures" that Baltes et al. flag as reproducibility barriers are precisely the issues that mechanistic interpretability seeks to address at a more fundamental level. Baltes et al. offer practical workarounds (open baselines, detailed reporting) for the transparency gaps that mechanistic interpretability aims to solve theoretically.

**Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025):**
This is a highly complementary paper. While Trinkenreich et al. advocate for and explore the use of LLMs in SE research activities, Baltes et al. provide the methodological guardrails for doing so rigorously. Trinkenreich et al.'s use cases (e.g., LLMs for coding, data analysis, literature review) map directly onto Baltes et al.'s study types (Annotators, Judges, Synthesis). Together, the two papers form a "how to use" / "how to do it properly" pair.

**The Denario Project (Villaescusa-Navarro et al., 2025):**
The Denario Project represents a large-scale scientific simulation and data infrastructure effort in astrophysics. While not directly about LLMs, Baltes et al.'s emphasis on reproducibility, detailed reporting of computational configurations, and open science practices parallels Denario's commitment to making simulation data and methods transparent and reusable. Baltes et al.'s guideline on reporting tool architectures and hosting environments is analogous to Denario's detailed documentation of simulation parameters. Both papers share a core concern with enabling others to reproduce and build upon computational research.

**KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025):**
Suryawanshi et al.'s knowledge graph-based RAG system is a concrete example of the kind of LLM-based tool architecture that Baltes et al.'s Guideline 3 (Report Tool Architecture Beyond Models) requires documenting. The RAG system's integration of knowledge graphs, retrieval mechanisms, and LLM inference exemplifies the multi-component architectures that Baltes et al. argue must be transparently reported. Additionally, Baltes et al.'s guidelines on reporting prompts, interaction logs, and evaluation metrics would directly apply to evaluating KG-based RAG systems.

### Useful Quotes (with page numbers)

1. **On the core problem (p. 1, Abstract):**
   > "Large language models (LLMs) are increasingly being integrated into software engineering (SE) research and practice, yet their non-determinism, opaque training data, and evolving architectures complicate the reproduction and replication of empirical studies."

2. **On the scope and goal of the guidelines (p. 1, Introduction):**
   > "So far, there are no holistic guidelines for conducting and reporting studies involving LLMs in SE research. With this community effort, we try to fill this gap."

3. **On the challenge of commercial model evolution (p. 1, Introduction):**
   > "Even if we knew the specific version of a commercial LLM used for an empirical study, the reported task performance could still change over time, since commercial models are known to evolve beyond version identifiers."

4. **On LLM non-determinism and reproducibility (p. 5, Guideline 2):**
   > "LLMs are inherently non-deterministic. However, this cannot be an excuse to dismiss the verifiability and reproducibility of empirical studies involving LLMs. Although exact reproducibility is hard to achieve, researchers can do their best to come as close as possible to that gold standard."

5. **On agentic tool traceability (p. 6, Guideline 3):**
   > "For agent-based systems that use external tools (e.g., Claude Code and its subagents), researchers must discuss agent behavior traceability by clearly delineating three distinct components: (1) LLM Input/Output: Internal deliberation, planning, and interpretation performed by the model. (2) External tool calls: Specific invocations of APIs, databases, file systems, or other external services that the agent explicitly triggers. (3) User or system interactions: Human-in-the-loop feedback, environment responses, or multi-agent communication."

6. **On generalizability across LLMs and time (p. 10, Guideline 8):**
   > "In LLM-based studies, generalizability boils down to two main concerns: (1) First, are the results specific to an LLM, or can they be achieved with other LLMs as well? (2) Second, will these results still be valid in the future?"

7. **On benchmarks not capturing real-world complexity (p. 9, Guideline 7):**
   > "Benchmarks usually do not capture the full complexity and diversity of software engineering work."

8. **On the conclusion and overall contribution (p. 10, Conclusion):**
   > "Adopting these practices will not eliminate LLM non-determinism, but it will make claims auditable, and results easier to replicate and compare across studies."
