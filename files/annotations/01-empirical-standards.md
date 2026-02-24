## Paper: Empirical Standards for Software Engineering Research

**Authors:** Paul Ralph et al. (40+ contributors from ACM SIGSOFT Paper and Peer Review Quality Initiative)
**Year:** 2021
**Venue:** arXiv:2010.03525 (ACM SIGSOFT Empirical Standards Initiative, Version 0.2.0)
**BibTeX Key:** ralph2021empirical

### Summary (2-3 sentences)

This paper presents a community-driven framework of empirical standards -- brief, public, methodology-specific checklists -- designed to replace the ad hoc, opaque evaluation criteria currently used in software engineering peer review. Developed by over 40 subject-matter experts under ACM SIGSOFT, the standards cover methodologies ranging from controlled experiments to case studies to systematic reviews, each organized into essential, desirable, and extraordinary attributes. The paper argues that structured, standards-based review can simultaneously increase review quality, paper quality, and acceptance rates by aligning author and reviewer expectations around transparent, community-endorsed criteria.

### Key Contributions

- **Empirical Standards Framework:** A modular set of methodology-specific checklists (General Standard + method-specific standards + cross-cutting supplements) that codify community expectations for how SE research should be conducted and reported.
- **Three-Tier Attribute Taxonomy:** Each standard classifies attributes as essential (necessary for publication), desirable (recommended but not always required), and extraordinary (award-quality), providing graduated quality expectations.
- **Structured Review Process:** A proposal to replace free-form essay-style peer review with dynamic, checklist-based review forms featuring decision trees that balance structure with flexibility through follow-up questions about justified deviations.
- **Adoption Models:** Three concrete adoption pathways (accidental, partial, full) for venues to progressively integrate the standards into their review processes.
- **Governance Model:** An open, GitHub-based governance structure for evolving the standards through community input, with defined roles for maintainers and a steering committee.
- **Scientific Justification:** A rigorous argument rooted in inter-rater reliability research that the unreliability of peer review stems from lack of structure, not reviewer incompetence, and that structured checklists improve consistency (as demonstrated in healthcare and research reporting).

### Architecture/Method

The framework uses a **modular, layered architecture**:

1. **General Standard** -- applies to all empirical research; reduces duplication across method-specific standards.
2. **Methodology-Specific Standards** -- individual standards for experiments (with human participants), questionnaire surveys, case studies, systematic reviews, grounded theory, action research, optimization studies, quantitative simulations, exploratory data science, engineering research, longitudinal studies, case surveys, and multi-methodology studies.
3. **Cross-Cutting Supplements** -- address recurring concerns such as information visualization, sampling, inter-rater reliability/agreement, ethics, open science, and pre-registration.

Each standard includes: definition, application scope, essential/desirable/extraordinary attributes, quality criteria, acceptable deviations, antipatterns, invalid criticisms, suggested readings, exemplars, and notes.

For full adoption, the paper proposes a **dynamic review form system** where:
- Authors select their methodology at submission time.
- The system generates a pre-submission checklist and a reviewer form from the relevant standards.
- Reviewers answer predominantly yes/no questions; decision trees with follow-up questions activate only when essential attributes are marked missing.
- The system (not reviewers) compiles answers and produces accept/revise/reject recommendations based on venue-configured decision rules.

The design process itself was a large-scale community effort: ACM SIGSOFT solicited volunteers in 2018, teams of subject-matter experts drafted each standard based on existing published methodological guidance, drafts were circulated for feedback, and the standards were hosted on GitHub for transparent version control and community contributions.

### Knowledge Representation Approach

The paper represents methodological knowledge as **structured, modular checklists** hosted on GitHub. This is essentially a **rule-based knowledge representation** where:

- Each methodology is a distinct knowledge module with defined attributes.
- Attributes are classified into a three-tier hierarchy (essential / desirable / extraordinary).
- Decision trees encode conditional logic for evaluating compliance (e.g., "Is random assignment used?" -> if no -> "Is the deviation justified?" -> if yes -> accept).
- Cross-cutting supplements serve as shared knowledge components referenced by multiple standards.
- The GitHub-based governance model treats the standards as living documents -- versioned, issue-tracked, and evolved through community pull requests.

This approach is notable for representing **implicit community knowledge** (what constitutes good research practice) as **explicit, structured, machine-processable criteria**, bridging the gap between tacit methodological expertise and transparent evaluation rubrics.

### Research Tasks Addressed

- **Peer Review Quality:** Improving the reliability, fairness, and transparency of scholarly peer review in software engineering.
- **Research Design Guidance:** Providing researchers with methodology-specific checklists to design better studies and write better manuscripts.
- **Reviewer Calibration:** Reducing inter-reviewer disagreement by providing shared, community-endorsed evaluation criteria.
- **Review Process Automation:** Enabling (partial) automation of the review workflow through structured forms and decision-tree logic.
- **Quality Assessment in Secondary Studies:** Enabling systematic literature reviewers to assess primary study quality using standardized criteria.
- **Graduate Education:** Providing a compact, authoritative resource for teaching research methods.

### Evaluation Method

The paper does **not** present a traditional empirical evaluation (no user study, no controlled experiment measuring the standards' impact). Instead, it relies on:

- **Argument from inter-rater reliability research:** Citations to established findings that peer review exhibits low inter-rater agreement and that structured checklists improve consistency (citing NIPS experiment by Price 2014, Bullock & Tubbs 1987, Plint et al. 2006, Treadwell et al. 2014).
- **Design science approach:** The standards themselves are the artifact; the paper describes their design rationale, design process, and governance.
- **Community validation:** Over 40 subject-matter experts from international institutions contributed to drafting and reviewing the standards.
- **Prototype system:** A structured-review prototype is mentioned as under development (https://web.cs.dal.ca/SIGSOFT-Empirical-Standards/).
- **Adoption evidence:** The paper notes that accidental adoption is already occurring, with reviewers spontaneously using the standards.

### Strengths

- **Massive community effort:** Over 40 domain experts contributed, lending the standards significant authority and breadth of perspective.
- **Practical and actionable:** The standards are immediately usable by authors (pre-submission checklists), reviewers (structured evaluation), venues (adoption models), and educators (teaching resource).
- **Modular and extensible:** The layered architecture (general + method-specific + supplements) allows the framework to grow organically as new methodologies emerge.
- **Balances structure with flexibility:** The decision-tree approach with follow-up questions about justified deviations prevents rigid, box-ticking rejection of innovative research.
- **Addresses root cause:** Grounded in the insight that peer review unreliability stems from lack of structure rather than reviewer incompetence -- a well-supported claim from inter-rater reliability research.
- **Open governance:** GitHub-based evolution model enables transparent, community-driven maintenance and improvement.
- **Addresses diversity and inclusion:** Explicitly considers bias mitigation in both the development process and the standards themselves (e.g., preventing cross-paradigmatic criticism like demanding quantitative metrics in qualitative studies).

### Weaknesses/Limitations

- **No empirical evaluation of the standards' impact:** The paper does not report any controlled study or even pilot data measuring whether the standards actually improve review quality, acceptance rates, or inter-rater agreement.
- **Potential for rigidity despite safeguards:** While decision trees include flexibility mechanisms, there is an acknowledged risk that reviewers may adopt a superficial "box-ticking" approach, especially under time pressure.
- **Depends on venue adoption:** The standards' effectiveness is contingent on broad adoption by conferences and journals; without institutional buy-in, the impact remains limited to voluntary, ad hoc use.
- **Coverage gaps:** At version 0.2.0, not all SE methodologies have dedicated standards; novel or hybrid methods may be inadequately covered.
- **Does not address LLM-era research:** Published in 2021, the standards predate the explosion of LLM-based SE research and do not include standards for evaluating studies involving large language models, AI agents, or AI-assisted research workflows.
- **Scalability of governance:** As adoption grows, maintaining quality and consistency across a growing set of standards with evolving maintainers could become challenging.
- **Western/academic bias:** Despite diversity efforts, the contributor list skews toward European and North American institutions, which may limit the standards' applicability in other research cultures.

### Connections to Other Papers

This paper serves as the **methodological quality foundation** for the literature survey, providing the framework against which all other papers in the set can be evaluated for research rigor.

**Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025):** The empirical standards provide the evaluation criteria that Trinkenreich et al.'s work on LLMs in SE research should be measured against. As LLMs become tools for conducting SE research, the standards need to evolve to address AI-assisted study design and execution -- a gap this paper acknowledges implicitly through its "living document" governance model.

**Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025):** Baltes et al.'s guidelines can be seen as a direct extension of the empirical standards framework to the LLM era. Where Ralph et al. provide methodology-specific standards for traditional SE research methods, Baltes et al. address the new methodological challenges that arise when LLMs are the subject or tool of empirical studies. Together, these two papers form a comprehensive quality framework spanning pre-LLM and LLM-era SE research.

**Open Problems in Mechanistic Interpretability (Sharkey et al., 2025):** The empirical standards' emphasis on transparent, reproducible evaluation criteria connects to interpretability research, which seeks to make AI decision-making transparent. Both papers advocate for moving from opaque processes (peer review / neural network inference) to structured, interpretable ones.

**The Denario Project (Villaescusa-Navarro et al., 2025):** As a large-scale scientific simulation project, Denario would fall under the empirical standards' Quantitative Simulations Standard. The standards provide criteria for evaluating the rigor of computational science research, including simulation validation and reproducibility.

**KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025):** The standards' structured, modular knowledge representation (checklists organized by methodology) is conceptually analogous to the knowledge graph approach in Suryawanshi et al., where structured representations enable systematic information extraction. Both papers address the challenge of organizing domain knowledge into actionable, machine-processable formats.

### Useful Quotes (with page numbers)

1. **On the root cause of peer review failure (p. 3):**
   > "This disconnect between authors' and reviewers' expectations is why peer review is so unpredictable and frustrating. Meanwhile, the common disconnect between reviewer expectations, community norms and published methodological guidance makes peer review fundamentally unscientific."

2. **On the nature of empirical standards (p. 4):**
   > "An empirical standard is essentially a one-page checklist of specific criteria that can be used by authors to conduct and report research, and by reviewers to evaluate manuscripts."

3. **On the scientific basis for structured review (p. 15):**
   > "Peer review isn't unreliable because reviewers are ignorant or lazy or pedantic or whatever we yell at our screens when we don't like a review. Peer review is unreliable because it lacks structure."

4. **On fairness and transparency (p. 3-4):**
   > "Adopting empirical standards makes peer review fair and transparent in two ways. First, the standards allow the authors and the reviewers to work from the same rubric, so there are no secrets and fewer surprises. Second, the standards allow crucial decisions about what is and is not acceptable scientific practice to be made by our scientific community collectively, instead of by reviewers, individually."

5. **On the vision for structured review (p. 10):**
   > "We envision a structured review process where reviewers evaluate a manuscript against a standard by answering predominately yes-or-no questions. A manuscript's accept-reject decision is a consequence of the decision rules devised by the venue."

6. **On the myth of necessary rejection (p. 3):**
   > "The truth is that constant rejection is neither intrinsic to science nor necessary for quality control. Rather, constant rejection is rooted in dissensus within scientific communities regarding how research should be conducted, and the accidental obfuscation of review criteria."
