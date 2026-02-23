## Paper: Open Problems in Mechanistic Interpretability

**Authors:** Lee Sharkey, Bilal Chughtai, Joshua Batson, Jack Lindsey, Jeff Wu, et al. (30 authors from Apollo Research, Anthropic, Google DeepMind, Eleuther AI, FAR AI, MIT, Harvard, and others)
**Year:** 2025
**Venue:** arXiv:2501.16496
**BibTeX Key:** sharkey2025mechanistic

### Summary (2-3 sentences)

This paper is a comprehensive forward-looking review that identifies and taxonomizes open problems in mechanistic interpretability -- the field that aims to understand the computational mechanisms underlying neural networks' capabilities. It organizes challenges into three categories: (1) foundational methods for reverse engineering and decomposing neural networks, (2) applications such as monitoring for unsafe AI cognition, controlling model behavior, predicting capabilities, and extracting scientific knowledge ("microscope AI"), and (3) socio-technical challenges including translating technical progress into AI governance levers. The review synthesizes perspectives from 30 researchers across leading AI safety and research organizations, providing both a snapshot of the current frontier and a roadmap for future priorities.

### Key Contributions

- Provides a structured taxonomy of open problems in mechanistic interpretability organized along three axes: methods/foundations, applications, and socio-technical challenges
- Critically evaluates sparse dictionary learning (SDL) / sparse autoencoders (SAEs) as the dominant decomposition method, cataloging 9 distinct practical and conceptual limitations (reconstruction errors, expense, linear representation assumption, sparsity as imperfect proxy for interpretability, unexplained feature geometry, architectural limitations, activation-only focus, and missing concepts)
- Formalizes the three-step reverse engineering pipeline for neural networks: decomposition, description of functional roles, and validation of descriptions
- Identifies "microscope AI" as a key application -- using interpretability to extract novel scientific knowledge from trained models, with examples from chess, medicine, and psychology
- Articulates the concept of "enumerative safety" -- the possibility that decomposing all network components could let us verify that no mechanisms exist for specific dangerous capabilities
- Discusses how mechanistic interpretability could provide concrete levers for AI governance, including compliance with the EU AI Act and GDPR
- Highlights the need for "model organisms" (standardized benchmark networks) analogous to model organisms in biology
- Frames the automation of interpretability research as both a necessary scalability measure and a current limitation

### Architecture/Method

The paper does not propose a single new method but rather surveys and critically evaluates the methodological landscape:

**Two Methodological Approaches:**
1. **Reverse Engineering** (bottom-up): Decompose network into components, then identify their functional roles
   - Step 1: Decomposition -- breaking networks into interpretable units (neurons, attention heads, or learned directions via SDL)
   - Step 2: Description -- hypothesizing functional roles via highly activating examples, attribution methods, feature synthesis, logit lens, causal interventions, or activation steering
   - Step 3: Validation -- testing hypotheses through prediction, adversarial examples, handcrafted replacements, ground truth testing, or downstream engineering goals

2. **Concept-based Interpretability** (top-down): Propose human concepts, then search for network components that correspond to them
   - Uses concept-based probes (linear classifiers trained to predict concepts from hidden representations)
   - Concept activation vectors, information-theoretic probing, structural probing
   - Concept bottleneck models for intrinsic interpretability

**Sparse Dictionary Learning (SDL)** is the dominant current paradigm, including:
- Sparse Autoencoders (SAEs): encode hidden activations into a wide, sparse hidden space to identify "latent" directions corresponding to features
- Transcoders: reconstruct next-layer activations instead of same-layer
- Crosscoders: reconstruct activations across multiple layers simultaneously
- Underpinned by the Linear Representation Hypothesis (concepts are linearly represented as directions in embedding space) and the Superposition Hypothesis (networks represent more features than dimensions via sparse encoding)

**Circuit Discovery Pipeline:**
1. Task definition
2. Decomposition into a directed acyclic graph (DAG)
3. Identification of task-relevant subgraphs via causal interventions
4. Iterative description-validation loop
5. Final validation for faithfulness, minimality, and completeness

### Knowledge Representation Approach

This paper directly addresses how neural networks internally represent knowledge:

- **Linear Representation Hypothesis (LRH):** High-level concepts are linearly represented as directions (vectors) in neural network embeddings. Two core claims: (i) multiple concepts compose via vector addition, and (ii) concept intensity is represented by vector magnitude. The strong version (all concepts are linear) is demonstrably false, but a weaker version is well-supported.

- **Superposition Hypothesis:** Networks represent more features than they have dimensions by encoding them sparsely and linearly in activation spaces. This explains polysemanticity (individual neurons responding to multiple unrelated concepts).

- **Feature Geometry:** The geometric arrangement of features relative to each other reflects semantic and functional structure. SDL decomposes networks into individual directions but leaves these geometric relationships unexplained.

- **Distributed Representations:** Knowledge may span multiple layers, individual neurons are polysemantic, and attention heads also exhibit polysemanticity. This means no single architectural unit (neuron, head, layer) provides a natural decomposition.

- **Mechanisms vs. Activations:** A critical distinction is drawn between representations (activations that carry information) and mechanisms (the parameters, nonlinearities, and architectural components that compute on those representations). Current methods primarily study activations, with much less attention to how structure in activations is computed via weights.

### Research Tasks Addressed

1. **Neural network decomposition:** How to "carve networks at their joints" into interpretable components
2. **Feature identification and description:** Automatically labeling what network components do
3. **Validation of interpretability claims:** Preventing "interpretability illusions" and ensuring causal (not merely correlational) explanations
4. **AI safety monitoring:** Detecting deception, sycophancy, sandbagging, and other unsafe cognition patterns
5. **Model editing and unlearning:** Surgically modifying specific knowledge or capabilities without side effects
6. **Capability prediction:** Forecasting when capabilities emerge during training or can be elicited via finetuning
7. **Scientific knowledge extraction (microscope AI):** Using trained models as instruments to discover novel patterns in data
8. **Formal verification of AI:** Mathematically proving safety properties of neural networks
9. **Scaling interpretability:** Making methods work on frontier-scale models
10. **Cross-architecture generalization:** Ensuring methods transfer beyond transformers to SSMs, diffusion models, etc.

### Evaluation Method

As a survey/review paper, it does not present original empirical evaluations. However, it discusses evaluation approaches for the field:

- **Activation prediction:** Using natural language explanations of component function to predict activation levels on new inputs (automated via LLMs)
- **Counterfactual prediction:** Testing whether interpretations correctly predict effects of ablating or activating components
- **Adversarial validation:** Using interpretability insights to handcraft adversarial examples
- **Ground truth benchmarks:** Testing methods on networks with known algorithms (compiled programs into weights, or Interchange Intervention Training)
- **Engineering utility:** Assessing whether interpretability tools improve downstream tasks (model editing, debugging, red-teaming) competitively against non-interpretability baselines
- **Circuit evaluation metrics:** Faithfulness (how well circuit approximates full network), minimality (no unnecessary components), completeness (no missing important components)
- **Reconstruction quality for SDL:** Measuring performance degradation when replacing true activations with sparse dictionary reconstructions (e.g., GPT-4 with 16M latent SAE performed like a model with 10% of its pretraining compute)

### Strengths

- **Comprehensive scope with forward-looking orientation:** Unlike retrospective surveys, this review explicitly identifies what the field should prioritize, making it a roadmap rather than just a catalog
- **Honest assessment of limitations:** The paper is remarkably candid about the shortcomings of currently dominant methods (especially SDL/SAEs), avoiding the hype common in interpretability discourse
- **Multi-stakeholder perspective:** Synthesizes views from 30 researchers across safety-focused labs (Apollo, Anthropic), frontier labs (Google DeepMind), and academia (MIT, Harvard, Northeastern), providing a balanced perspective
- **Practical grounding:** Connects abstract interpretability goals to concrete governance mechanisms (EU AI Act compliance, GDPR, copyright law), making the work relevant beyond the research community
- **Clear taxonomization:** The three-category organization (methods, applications, socio-technical) and the identification of axes of progress (decomposition vs. description, extent of decomposition, task distribution scope, post- vs. during-training understanding) provide useful analytical frameworks
- **Interdisciplinary bridges:** Draws productive analogies to neuroscience (model organisms, the Neuron Doctrine) and philosophy of science

### Weaknesses/Limitations

- **No novel empirical contribution:** As a pure survey/position paper, it does not advance the state of the art with new methods or experiments
- **Transformer-centric despite calling for broader coverage:** While the paper advocates for studying diverse architectures, its discussion is heavily weighted toward transformer-based language models
- **Limited treatment of multimodal models:** Despite noting the importance of multimodality, the paper provides minimal guidance on interpretability for vision-language models, audio models, or other multimodal systems
- **Potentially premature systematization:** The field is evolving rapidly; some of the "open problems" identified may be resolved or become irrelevant as paradigms shift (e.g., if SDL is superseded)
- **Governance discussion is speculative:** The translation of interpretability into governance levers is discussed at a high level without concrete policy proposals or implementation roadmaps
- **Missing perspectives from deployment contexts:** The paper focuses on research challenges but says little about the practical engineering challenges of deploying interpretability tools in production AI systems
- **Consensus document trade-offs:** As a synthesis of 30 authors' views, the paper occasionally hedges rather than taking strong positions on contested questions

### Connections to Other Papers

Other papers in the set:
- **Empirical Standards for SE Research (Ralph et al., 2021):** Sharkey et al.'s emphasis on validation rigor and the danger of "interpretability illusions" parallels Ralph et al.'s push for empirical standards. The review explicitly criticizes the field for conflating hypotheses with conclusions and calls for benchmarks and ground-truth testing -- essentially advocating for the kind of methodological rigor that empirical standards codify. Both papers address the meta-question of how to ensure research claims are well-supported.

- **Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025):** Sharkey et al.'s Section 2.4 on "Automating steps in mechanistic interpretability research" directly connects to the theme of using LLMs as research tools. The paper discusses using LLMs to generate feature descriptions, validate interpretations, and automate circuit discovery -- essentially using AI to study AI. This is the interpretability-specific instance of the broader trend Trinkenreich et al. examine of LLMs transforming research methodology.

- **Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025):** The open problems identified by Sharkey et al. have direct implications for any empirical study involving LLMs. Understanding how LLMs internally represent knowledge (via the Linear Representation Hypothesis and superposition) is foundational context for researchers designing experiments that use LLMs. The interpretability perspective helps explain why LLM behavior can be unpredictable and why careful experimental design (as Baltes et al. advocate) is essential.

- **The Denario Project (Villaescusa-Navarro et al., 2025):** Sharkey et al.'s discussion of "microscope AI" -- using interpretability to extract scientific knowledge from trained models -- connects directly to projects like Denario that use neural networks on scientific data. The interpretability methods reviewed could potentially be applied to understand what cosmological or astrophysical patterns a model like Denario has learned, extracting novel scientific insights beyond what the model's predictions alone reveal.

- **KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025):** While Suryawanshi et al. focus on structuring external knowledge via knowledge graphs, Sharkey et al. address the complementary problem of understanding knowledge structured internally within neural networks. The concept-based interpretability approach (probing for specific concepts in hidden representations) is analogous to querying a knowledge graph -- both seek to locate and retrieve structured knowledge, but from different substrates. Together, they represent external vs. internal approaches to making AI knowledge accessible and auditable.

### Useful Quotes (with page numbers)

1. "Understanding a neural network's decision-making process [means] the ability to use knowledge about the mechanisms underlying a network's decision-making process in order to successfully predict its behavior (even on arbitrary inputs) or to accomplish other practical goals with respect to the network." (p. 4) -- Provides a concrete, operationalizable definition of interpretability that connects understanding to prediction and engineering utility.

2. "Even simple algorithmic tasks, like modular addition, which humans might solve with simple carries, were solved by a small transformer model by learning a Fourier transform strategy that researchers only understood in retrospect." (p. 7) -- Illustrates the "alien cognition" of neural networks and why reverse engineering is necessary.

3. "When a sparse dictionary with 16 million latents was inserted into GPT-4, the language modeling loss was equivalent to a model with only 10% of GPT-4's pretraining compute." (p. 10) -- Quantifies the significant reconstruction error limitation of current SDL methods.

4. "Mechanistic interpretability could allow us to make a certain type of claim, namely, 'there exists no mechanisms that would cause the model to deliberately behave undesirably.'" (p. 28) -- Articulates the "enumerative safety" vision that motivates much of the field.

5. "Interpretability is perhaps the only research area that attempts to understand the mechanisms of model cognition. This implies that it might be particularly fruitful for interpretability researchers to tackle problems that become easier to solve through improving such understanding: auditing for unsafe cognition, debugging unexpected behavior, and monitoring systems in deployment." (p. 26) -- Identifies the comparative advantage of mechanistic interpretability relative to other ML research areas.

6. "The recent definite -- but ultimately modest -- progress in mechanistic interpretability has been used to lobby against specific AI regulation by falsely claiming that [...] 'recent advancements in the AI sector have resolved this issue, thereby ensuring the integrity of open-source code models.'" (p. 35) -- Highlights the socio-technical risk of interpretability progress being misrepresented for policy purposes.
