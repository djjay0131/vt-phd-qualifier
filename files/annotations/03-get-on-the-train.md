## Paper: Get on the Train or be Left on the Station: Using LLMs for Software Engineering Research

**Authors:** Bianca Trinkenreich, Fabio Calefato, Geir Hanssen, Kelly Blincoe, Marcos Kalinowski, Mauro Pezze, Paolo Tell, Margaret-Anne Storey
**Year:** 2025
**Venue:** arXiv:2506.12691
**BibTeX Key:** trinkenreich2025train

### Summary (2-3 sentences)
This position paper applies McLuhan's Tetrad of Media Laws to systematically analyze how Large Language Models (LLMs) are transforming software engineering (SE) research across every stage of the research pipeline -- from research question formulation through writing and dissemination. Emerging from discussions at the 2nd Copenhagen Symposium on Human-Centered AI in SE, the authors examine what LLMs enhance, make obsolete, retrieve, and risk reversing in SE research practice. The paper concludes with a four-part call to action: (1) experimentation with LLMs in SE research, (2) transparent reporting guidelines, (3) benchmarks for LLM-generated research artifacts, and (4) educational resources for responsible LLM usage.

### Key Contributions
- Application of McLuhan's Tetrad of Media Laws as an analytical framework for understanding LLM impact on the full SE research pipeline (Table 1 mapping all six pipeline stages)
- Detailed analysis of two critical pipeline stages -- Research Goals & Questions Formulation and Analysis & Interpretation -- through the four Tetrad lenses (enhance, obsolesce, retrieve, reverse)
- Identification of "creativity echo chambers" as a key reversal risk: LLMs may homogenize research questions by reinforcing established knowledge patterns rather than enabling genuinely novel inquiry
- A concrete four-part call to action for the SE research community: experimentation, reporting guidelines, evaluation benchmarks, and educational resources
- Articulation of the concept that LLMs can retrieve "coffee house research" -- informal, collaborative ideation culture that has diminished in modern academia

### Architecture/Method
The paper is structured around McLuhan's Tetrad of Media Effects (1977), a media theory framework that asks four questions about any new technology:
1. **Enhance** -- What does the technology amplify or intensify?
2. **Obsolesce** -- What does the technology push aside or make redundant?
3. **Retrieve** -- What previously obsolesced practice does the technology bring back?
4. **Reverse** -- What does the technology flip into when pushed to extremes?

The authors apply this framework across a six-stage research pipeline: (1) Research Goals & Questions Formulation, (2) Experimental Design & Methodology, (3) Data Collection, (4) Data Processing, (5) Analysis & Interpretation, and (6) Writing & Dissemination, plus cross-cutting impacts. The framework was collaboratively developed by 10 researchers during a symposium, with the pipeline structure itself initially generated using a GPT tool (the Disruptive Playbook) and then refined by the authors. The paper provides detailed discussion of two stages and summarizes all six in Table 1.

### Knowledge Representation Approach
This paper does not propose a formal knowledge representation system but provides a structured conceptual framework for understanding how LLMs interact with research knowledge:
- **Literature synthesis as knowledge retrieval**: LLMs can automate systematic literature review tasks including search string formulation, study selection, data extraction, and synthesis (Obsolesce dimension)
- **Cross-domain knowledge linking**: LLMs can retrieve theories from other domains (cognitive psychology, organizational science) to interpret SE findings, acting as interdisciplinary knowledge bridges (Retrieve dimension)
- **Pattern extraction from scientific text**: References Tshitoyan et al. (2019), showing AI can extract hidden patterns from scientific publications that predict future discoveries -- a form of latent knowledge representation in literature
- **Knowledge homogenization risk**: LLMs may converge on "safe" and predictable topics because they generate content based on existing knowledge patterns, potentially narrowing the knowledge space rather than expanding it

### Research Tasks Addressed
- **Research ideation and hypothesis generation**: LLMs as brainstorming partners for research question formulation, including multi-agent systems for iteratively refining hypotheses (AI Co-Scientist)
- **Systematic literature review automation**: Search string formulation, study selection, data extraction, and synthesis
- **Qualitative data analysis**: Coding of interview transcripts, surveys, issue-tracker comments, and software reviews
- **Quantitative data analysis**: Statistical technique selection, assumption checking, result interpretation
- **Mixed-methods integration**: Bridging qualitative and quantitative findings through visualization and joint analysis
- **Interdisciplinary theory retrieval**: Finding related theoretical frameworks across domains
- **Research writing and dissemination**: Automated drafting, summarization, and multilingual dissemination

### Evaluation Method
This is a position paper and does not include empirical evaluation. The analytical framework (McLuhan's Tetrad) was applied collaboratively by a team of 10 researchers at the 2nd Copenhagen Symposium on Human-Centered AI in SE (November 2024), funded by the Alfred P. Sloan Foundation and the Carlsberg Foundation. The authors explicitly acknowledge that "other researchers may have different ideas about the effects LLMs will have on SE research and that our speculation would also change as LLMs evolve." The paper draws on existing empirical work (28 references) to support its claims at each Tetrad dimension.

### Strengths
- **Systematic analytical framework**: The McLuhan Tetrad provides a balanced, four-dimensional view that avoids pure techno-optimism or pessimism, forcing consideration of both benefits and risks
- **Comprehensive pipeline coverage**: Table 1 covers all six stages of the research pipeline, providing a complete map of LLM impact on research practice
- **Nuanced treatment of reversal risks**: The "creativity echo chamber" concept and the warning about researcher deskilling are particularly insightful and well-articulated
- **Practical call to action**: The four concrete recommendations (experimentation, reporting guidelines, benchmarks, education) are actionable for the community
- **Historical perspective**: The "coffee house research" retrieval concept adds depth, connecting modern LLM-augmented research to historical intellectual traditions
- **Collaborative authorship**: The framework was developed by a diverse team of 10 researchers from multiple institutions and countries, lending breadth to the analysis

### Weaknesses/Limitations
- **No empirical validation**: As a position paper, none of the claims are empirically tested; the entire analysis is speculative (the authors acknowledge this)
- **SE-specific scope may limit generalizability**: While the research pipeline is generic, the detailed analysis focuses on SE-specific concerns (GitHub mining, code change classification, etc.)
- **Incomplete pipeline discussion**: Only two of six pipeline stages are discussed in depth; the remaining four are only covered in Table 1 with brief phrases
- **Limited engagement with agent architectures**: While mentioning the AI Co-Scientist multi-agent system, the paper does not deeply engage with agentic AI frameworks where LLMs autonomously execute multi-step research workflows
- **No concrete examples of failure**: The reversal risks (hallucinations, bias amplification, deskilling) are discussed abstractly without concrete case studies or empirical evidence of these failures occurring in SE research
- **McLuhan framework limitations**: The Tetrad is a speculative framework by design and may oversimplify the complex, non-linear ways LLMs interact with research practice

### Connections to Other Papers
**Other papers in the set:**
- **Empirical Standards for SE Research (Ralph et al., 2021)**: Directly referenced (ref [17]) as the basis for transparent reporting guidelines. The authors advocate for extending empirical standards to cover LLM usage in SE research. This paper's call for "clear review guidelines about the use of LLMs in SE research" is essentially a proposal to update the empirical standards framework.
- **Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025)**: Also directly referenced (ref [25], Wagner et al. 2025, which includes Baltes). The paper's second call to action -- transparent reporting on LLM usage -- aligns closely with and builds upon this guidelines paper.
- **Open Problems in Mechanistic Interpretability (Sharkey et al., 2025)**: The reversal risks identified (hallucinations, bias amplification, false reliability) connect to interpretability challenges. Understanding why LLMs produce specific outputs (mechanistic interpretability) could help mitigate the "misleading interpretations" and "AI hallucinations" the authors warn about.
- **The Denario Project (Villaescusa-Navarro et al., 2025)**: Denario represents a concrete instance of using AI for scientific research in astrophysics -- an example of the kind of LLM-augmented research pipeline this paper theorizes about. The Denario project's multi-agent approach to scientific discovery embodies the "enhance" dimension of the Tetrad.
- **KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025)**: The Retrieve dimension's emphasis on interdisciplinary knowledge linking and cross-domain theory finding connects directly to knowledge graph approaches for structuring and retrieving research knowledge. KG-based RAG could address some of the hallucination risks identified in the Reverse dimension by grounding LLM outputs in structured knowledge.

### Useful Quotes (with page numbers)

1. **Page 1 (Abstract):** "We argue that the SE research community must proactively engage with and shape the integration of LLMs into research practices, emphasizing human agency in this transformation."

2. **Page 2 (Research Goals - Reverse):** "Since LLMs today tend to generate content based on existing knowledge, relying too heavily on them for research ideation risks creating a creativity echo chamber, where generated questions and study designs reflect common patterns rather than genuinely novel insights."

3. **Page 2 (Research Goals - Reverse):** "If LLMs reinforce established knowledge structures, researchers may unknowingly converge on 'safe' and predictable topics, leading to a homogenization of research rather than groundbreaking discoveries."

4. **Page 3 (Analysis - Retrieve):** "LLMs can revive interest in finding related theories in other domains to interpret SE findings (something we have not been doing enough of in recent years)."

5. **Page 3 (Analysis - Reverse):** "While the model-to-model agreement can predict when LLMs could safely replace human annotators, it also highlights the potential for systemic bias where LLMs reinforce each other's errors, creating a false perception of reliability."

6. **Page 4 (Call to Action):** "Although LLMs can be used to accelerate paper production, their true transformative potential lies in enabling researchers to redirect their time toward deeper intellectual engagement and focus on doing impactful research."

7. **Page 4 (Call to Action):** "We urge our fellow members of the software engineering research community to use any time saved by LLMs to invest in thoughtful dialogue with colleagues, stakeholders, and potential beneficiaries of their work."

8. **Page 4 (Call to Action):** "Using LLMs for SE research presents a significant opportunity to speed up discovery and unlock new avenues for impactful research... overreliance on LLMs can result in lower skills of researchers."
