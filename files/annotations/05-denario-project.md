## Paper: The Denario Project: Deep Knowledge AI Agents for Scientific Discovery

**Authors:** Francisco Villaescusa-Navarro, Boris Bolliet, Pablo Villanueva-Domingo et al. (30+ contributors)
**Year:** 2025
**Venue:** arXiv:2510.26887
**BibTeX Key:** villaescusa2025denario

### Summary (2-3 sentences)

Denario is an AI multi-agent system designed as an end-to-end scientific research assistant, capable of generating research ideas, reviewing literature, developing plans, writing and executing code, making plots, and drafting and reviewing scientific papers. Built on AG2 and LangGraph with a modular architecture, it orchestrates multiple LLM-powered agents using a Planning & Control strategy adapted from robotics. The paper evaluates Denario by generating papers across 13 scientific disciplines — from astrophysics to biology — and having domain experts score them, concluding that Denario produces research at the level of a good undergraduate or early graduate student in ~30 minutes at ~$4/paper.

### Key Contributions

- **End-to-end agentic research pipeline:** A complete system (6 modules: Idea, Literature, Methods, Analysis, Paper, Review) that can carry out the full scientific research cycle without human intervention, from hypothesis generation to peer-review simulation.
- **Modular, composable architecture:** Each module is independently usable (e.g., just idea generation or just code/analysis), enabling researchers to deploy Denario as a partial or full research assistant.
- **Planning & Control strategy for science:** Adapts the robotics Planning & Control paradigm to scientific research — a planner agent decomposes tasks into subtasks, assigns agents, and a control agent monitors execution to completion. This enables autonomous long-horizon research without human-in-the-loop.
- **Multi-discipline empirical evaluation:** 13 end-to-end AI-generated research papers spanning astrophysics, biology, chemistry, medicine, neuroscience, mathematics, and more — each evaluated by domain experts with numerical scores (0–10) and referee-style feedback.
- **Ethical and philosophical analysis:** A substantial (Sections 7.1–7.4) discussion of the ethical implications, epistemic changes, and philosophy-of-science implications of AI-driven research.
- **Open-source release:** Full code, GUI, and web demo released publicly.

### Architecture/Method

Denario's **6-module pipeline**:

1. **Idea module** — generates novel research ideas from an input description (data, problem space). Uses AG2 or LangGraph orchestration; multiple agents debate and refine ideas.
2. **Literature module** — searches arXiv and other preprint repositories to check novelty of ideas, produces a `literature.md` report on originality and related work.
3. **Methods module** — develops a detailed research plan (`methods.md`) specifying analysis steps, tools, code frameworks, and data processing strategies.
4. **Analysis module** — implements the plan: writes and executes code, makes plots, and summarizes results in `results.md`. Uses Cmbagent as a deep-research backend with Planning & Control.
5. **Paper module** — drafts a LaTeX scientific paper from the idea, methods, and results.
6. **Review module** — simulates peer review, generating a referee report on the paper.

**Orchestration frameworks:**
- **AG2** (formerly AutoGen): Supports complex agent conversation patterns (sequential, group, nested chats), structured context, conditional handoffs, and tool use.
- **LangGraph**: Directed graph-based orchestration where nodes are callable agents/functions and edges represent computation flow; supports dynamic/conditional routing.

**Planning & Control strategy (Cmbagent backend):**
- Planning phase: A planner agent + plan reviewer agent produce a subtask plan (3–8 steps); plan is injected into each agent's system message.
- Control phase: A control agent monitors execution, records status (complete/failed/in-progress), and triggers the next agent. Hard limits (max 500 messages) prevent infinite loops.
- Termination: Either plan succeeds fully or the session aborts after max failures.

**LLM choices:** System is LLM-agnostic; supports GPT-5, Gemini 2.5 Pro, Claude Opus 4, and others. Different tasks use different models (e.g., Gemini/GPT for coding, Claude for review/critique).

### Knowledge Representation Approach

Denario represents scientific knowledge implicitly through **LLM context windows and agent communication**:
- Each agent's "knowledge" is encoded in its system prompt (role, task instructions, methodology) and the accumulated conversation context passed between agents.
- The Planning & Control loop uses **structured function calls** to record plan state, subtask status, and agent handoffs — a lightweight explicit representation atop the LLM's implicit knowledge.
- The Literature module accesses **external knowledge** from arXiv (retrieval-augmented generation style), but does not build a persistent knowledge graph.
- Knowledge is **ephemeral per session**: there is no persistent knowledge store across runs (unlike KG-RAG approaches). Each research session starts from the LLM's training-time knowledge plus context injected via prompts.

This contrasts sharply with the KG-RAG approach (Suryawanshi et al.): Denario's "knowledge" is parameterized in LLM weights and session context; Suryawanshi et al. externalize knowledge into an explicit, persistent knowledge graph.

### Research Tasks Addressed

- **Idea generation:** Proposing novel research hypotheses from data descriptions.
- **Novelty checking:** Literature search to determine if an idea has been explored before.
- **Research planning:** Decomposing a research goal into executable subtasks.
- **Code-driven analysis:** Autonomous code generation, debugging, execution, and result interpretation across data science, astrophysics, biology, chemistry, and more.
- **Paper writing:** Generating full LaTeX manuscripts from code outputs and results.
- **Peer review simulation:** Generating referee-style reports to evaluate AI-generated papers.
- **Cross-disciplinary synthesis:** Combining methods from different fields (e.g., quantum tensor trains applied to cosmological data).

### Evaluation Method

- **Domain expert scoring:** For each of 13 AI-generated papers, a domain expert assigned a score from 0 (very poor) to 10 (excellent), knowing the paper was AI-generated. Results: most papers scored above 5 ("normal"); some scored 8–9.
- **Expert narrative feedback:** Each paper section received reviewer-style comments on strengths and weaknesses.
- **Comparative framing:** Authors benchmark against what "a good undergraduate or early graduate student could achieve after weeks or a few months of work" — Denario achieves similar output in ~30 minutes.
- **Reproduction check:** For one astrophysics paper, a domain expert independently reproduced figures and verified conclusions without access to Denario's code — results validated.
- **Failure mode documentation:** Two systematic failure modes documented in detail (cyclic peptide hallucination; pure mathematics incapacity).
- **No quantitative automated benchmarks:** Evaluation is entirely qualitative/expert-driven; no automated metric (BLEU, F1, etc.) is used for paper quality.

### Strengths

- **Most comprehensive autonomous research system yet demonstrated:** End-to-end research across 13 disciplines with expert evaluation is far broader than prior work (Sakana AI-Scientist, AI Cosmologist).
- **Modular and composable:** Researchers can use individual modules without the full pipeline; the system gracefully accommodates partial automation.
- **Honest and extensive failure analysis:** Detailed failure modes (hallucinating paper with no results; inability on pure mathematics) demonstrate scientific integrity about system limitations.
- **Addresses deep autonomy questions:** Planning & Control strategy enables genuine autonomous multi-step research without human-in-the-loop, which is a meaningful advance over simple single-agent systems.
- **Ethical and philosophical depth:** The paper devotes substantial space to authorship, homogenization, access, epistemic implications — rare and valuable in a systems paper.
- **Cross-disciplinary capability demonstrated:** The quantum physics + cosmology paper shows genuine cross-domain synthesis that would require multiple human experts to coordinate.
- **Speed/cost efficiency:** 30 min / ~$4 per paper draft represents a dramatic acceleration vs. human timescales of months.

### Weaknesses/Limitations

- **Evaluation is subjective and small-scale:** Expert scores (0–10) from a single domain expert per paper with no inter-rater reliability assessment directly contradict the empirical standards advocated by Ralph et al. — the paper acknowledges this limitation but does not address it.
- **Shallow depth:** Generated papers are at the level of a good undergraduate or early MS student, not an experienced researcher. Explanations of results tend to be superficial; big-picture connections and causal reasoning are weak.
- **Citation quality:** LLM-generated citations are often marginally relevant; domain experts can immediately identify AI-generated papers from citation patterns. This is a fundamental issue for scientific credibility.
- **No persistent knowledge representation:** Each session starts fresh; Denario has no memory of prior research runs. A knowledge graph (like Suryawanshi et al.) or long-term memory would enable cumulative scientific knowledge building.
- **Confirmation bias:** The system tends to overstate findings and avoids reporting negative results — reflecting the positive-results bias in its training data. This is a serious epistemic concern for scientific reliability.
- **Hallucination risk:** In the cyclic peptide case, the system fabricated an entire paper claiming results it had not computed — a severe failure mode requiring human validation of all code and claims.
- **No mechanistic interpretability:** The system's reasoning is opaque; there is no way to understand *why* it proposes a particular idea or reaches a given conclusion (directly connecting to Sharkey et al.'s concerns about mechanistic interpretability).
- **Doesn't meet its own empirical standards:** By the criteria of Ralph et al. or Baltes et al., the paper's evaluation is insufficient — no quantitative metrics, no baselines, no inter-rater reliability for expert scores.

### Connections to Other Papers

**Empirical Standards for SE Research (Ralph et al., 2021):** Denario's evaluation methodology (domain expert scores with no inter-rater agreement, no baselines, qualitative feedback only) fails several of Ralph et al.'s essential attributes for empirical studies. This is an ironic gap given the paper's scope — it proposes a system for automating science while not meeting the community's standards for evaluating that system. The "three-tier" attribute framework (essential/desirable/extraordinary) could be used to critique the Denario evaluation: essential attributes like operationalized constructs, appropriate analysis, and validity discussions are either missing or weak.

**Open Problems in Mechanistic Interpretability (Sharkey et al., 2025):** Denario exemplifies the interpretability problem at the research-tool level. The system's decisions — what ideas to generate, what code to write, what claims to make in a paper — are entirely opaque. When Denario hallucinates results (the cyclic peptide case), there is no mechanism to diagnose *why* it failed. Sharkey et al.'s call for understanding superposition, feature circuits, and reasoning processes in LLMs would directly benefit systems like Denario, where unexplained failures can produce scientifically harmful outputs.

**Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025):** Denario is the most extreme instantiation of the "get on the train" philosophy applied to research itself. While Trinkenreich et al. advocate using LLMs as *tools* to accelerate SE research workflows, Denario attempts to use LLMs as *agents* that can replace human researchers for end-to-end tasks. The two papers bracket a spectrum: LLMs as research tools vs. LLMs as research agents. Denario's results suggest the tool-level use case is more mature than the fully autonomous case.

**Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025):** Baltes et al.'s guidelines are urgently needed for systems like Denario. The paper uses LLMs as research subjects (evaluating their ability to do science) and as research instruments (the agents that generate papers). Both roles trigger Baltes et al.'s key concerns: prompt sensitivity (results vary dramatically with input phrasing), LLM version dependence, lack of reproducibility across model versions, and the risk of anthropomorphizing agent outputs. The Denario evaluation would benefit substantially from the structured protocol Baltes et al. propose.

**KG-based RAG for Cross-Document IE (Suryawanshi et al., 2025):** Denario and Suryawanshi et al. represent two fundamentally different approaches to AI-assisted research. Denario uses LLM context as implicit, ephemeral knowledge; Suryawanshi et al. build an explicit, persistent knowledge graph. A hybrid architecture — Denario's autonomous agents plus a KG-based long-term memory — could address Denario's lack of cross-session knowledge accumulation. The Literature module in Denario (which searches arXiv per session) is far less structured than the KG-based retrieval in Suryawanshi et al., suggesting a clear direction for architectural improvement.

### Useful Quotes (with page numbers)

1. **On Denario's goal (Abstract / p. 1):**
   > "We emphasize that the goal of Denario is not to automate science, but to develop a research assistant that can accelerate scientific discovery."

2. **On the breadth vs. depth tradeoff (p. 4):**
   > "We note that in scientific research, there is usually a tradeoff between depth and breadth, given a fixed amount of time to carry out a task or study. We believe that AI systems like Denario can help researchers explore a wide range of possibilities, at a more superficial level, while researchers can go deeper into the most interesting or promising ones."

3. **On performance benchmarking (Summary, p. 70):**
   > "From the expert evaluation of these manuscripts, we conclude that the generated papers are at the level of what a good undergraduate or early graduate student could achieve after weeks or a few months of work. In comparison, it took Denario around 30 minutes per paper and a cost of around $4."

4. **On hallucination failure (p. 61–62):**
   > "This case underscores the importance of scrutinizing agent-generated research with the same rigor applied to human-generated work: verifying source codes and raw data is essential for ensuring the validity of scientific claims."

5. **On confirmation bias (p. 38–39):**
   > "Perhaps the most concerning weakness shown in these manuscripts is their tendency to overstate the findings they present... To be able to succeed, AI multi-agents must be able to temper their conclusions when confidence in the significance of the results is low."

6. **On the complementary human-AI model (Summary, p. 70):**
   > "AI can scan widely and highlight promising directions, while human experts can select the most relevant ideas and pursue them in depth to achieve a deeper understanding."

7. **On ethical risk of irresponsible usage (p. 66):**
   > "If the usage takes place in an irresponsible manner, i.e. just generating papers without or little validation, then given the current capabilities of systems like Denario, the quality of the papers will degrade."

8. **On epistemic implications (p. 67):**
   > "The integration of LLMs and AI agents into scientific practice marks a profound inflection point in the philosophy of science. These systems are not mere computational tools; they increasingly participate in the core activities of science — formulating hypotheses, synthesizing literature, generating theoretical connections, falsification procedures, theory choice, epistemic virtue-discussions, and even simulating reasoning."
