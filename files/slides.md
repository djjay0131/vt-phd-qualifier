# PhD Oral Presentation: Agentic Knowledge Graphs for Research Progression

**Presenter:** Jason Cusati  
**Duration:** 15 Minutes  
**Total Slides:** 20  

---

## Slide 1: Research State Is Ephemeral

**Visual Concept:** A split screen: Left side shows a complex thought structure collapsing like a house of cards. Right side shows a "Session Closed" terminal window.

**Slide Content:**
- Research reasoning is fragmented and transient
- LLM-assisted workflows amplify volatility
- Structural memory is missing

**Speaker Notes:**
Good morning. My research is motivated by a fundamental problem in how we use AI for science today: Research state is ephemeral.

When we use LLMs for research, we are building reasoning on sand. We might have a brilliant, multi-step chain of thought, but as soon as the context window closes or the session ends, that structure is lost. The reasoning is fragmented and transient.

While LLMs have amplified our ability to generate text, they have also amplified this volatility. We lack a "structural memory" that persists between sessions, meaning we are constantly starting over rather than building up.

---

## Slide 2: The Structural Gaps

**Visual Concept:** Three pillars labeled "Persistence", "Traceability", "Evaluability". The pillars are cracked or fading at the top.

**Slide Content:**
- **Persistence:** State beyond session boundaries
- **Traceability:** Linkage from Claim $\to$ Evidence
- **Evaluability:** Empirical measurement of progression
- *These are infrastructure problems, not model-quality problems.*

**Speaker Notes:**
This manifests as three specific structural gaps.

First, **Persistence**: We lack state that survives beyond a single chat session.
Second, **Traceability**: When an agent makes a claim, we often cannot trace it back to the specific evidence that supported it.
Third, **Evaluability**: We lack the tools to empirically measure if our research knowledge is actually progressing over time.

Crucially, these are infrastructure problems, not model quality problems. Better models won't fix this; better architecture will.

---

## Slide 3: Guiding Question

**Visual Concept:** A bridge connecting a chaotic cloud of documents (left) to a structured, glowing crystal (right). The bridge is labeled "Infrastructure".

**Slide Content:**
**How can research state be made persistent, traceable, and empirically evaluable in AI-assisted workflows?**

**Speaker Notes:**
This leads to the guiding question of my proposal:

How can we transform this ephemeral interaction into something solid? How can research state be made persistent, traceable, and empirically evaluable in AI-assisted workflows?

To answer this, I've surveyed the current landscape to understand what pieces we already have and what is missing.

---

## Slide 4: Landscape Overview

**Visual Concept:** A landscape map with 5 distinct territories/regions.

**Slide Content:**
**Domains Surveyed:**
1. Mechanistic Interpretability
2. Retrieval-Augmented Generation (RAG)
3. Knowledge Graph Systems
4. Agentic Systems
5. Empirical Evaluation Standards

**Speaker Notes:**
I surveyed five key domains that contribute to this problem.

We look at **Mechanistic Interpretability** to understand how models represent knowledge internally.
We look at **RAG** and **Knowledge Graphs** as two ways of representing knowledge externally.
We look at **Agentic Systems** which act on that knowledge.
And finally, **Empirical Standards** to understand how we should evaluate these systems.

---

## Slide 5: Mechanistic Interpretability

**Visual Concept:** A magnifying glass focusing on the neurons of a neural network, revealing sparse features.

**Slide Content:**
- Reverse engineering internal representations
- Sparse dictionary learning (Sharkey et al., 2025)
- Structural decomposition
- **Limitation:** Focused on model internals, no persistent research-state

**Speaker Notes:**
Starting with Mechanistic Interpretability, work by Sharkey et al. focuses on reverse-engineering the "black box."

Techniques like sparse dictionary learning allow us to decompose model weights into understandable features. This is critical for understanding *how* a model thinks.

However, the limitation is that this focuses on the model's internal, static weights. It does not provide a mechanism for storing *new* research state that an agent generates during a workflow.

---

## Slide 6: Concept-Based Interpretability

**Visual Concept:** Vectors in a high-dimensional space aligning with labels like "Biology" or "Code".

**Slide Content:**
- Probes and representation alignment
- Correlation vs. causation concerns
- **Limitation:** Limited persistence mechanisms

**Speaker Notes:**
Similarly, concept-based interpretability uses probes to find directions in the latent space that correspond to concepts.

While this helps us align model representations with human concepts, these insights are often ephemeral. They tell us about the model's training data, but they don't give us a writable memory to store the results of a literature review we just conducted.

---

## Slide 7: RAG & Vector Memory Systems

**Visual Concept:** A massive library where all the books are torn out and thrown into a pile (unstructured vector soup).

**Slide Content:**
- **Strengths:** Scalable retrieval, Semantic similarity
- **Limitations:**
  - No structured reasoning
  - No canonical memory
  - No provenance chain
  - No longitudinal state

**Speaker Notes:**
Moving to external memory, we have RAG. RAG is powerful because it scales.

But as Suryawanshi et al. note, vector retrieval lacks structure. It gives us semantic similarity, not reasoning.

There is no "canonical" memory—if I retrieve a fact today, it might be different tomorrow. And crucially, there is no robust provenance chain linking a generated answer back to the specific span of text that justifies it.

---

## Slide 8: Knowledge Graph Research

**Visual Concept:** A clean, structured network of nodes and edges.

**Slide Content:**
- **Strengths:** Ontology-based structure, Provenance modeling, Logical relationships
- **Limitations:**
  - Manual curation
  - Static graphs
  - No automated maintenance

**Speaker Notes:**
Knowledge Graphs offer exactly the structure that RAG lacks. They provide explicit ontologies and logical relationships.

However, traditional KGs are high-friction. They are often static and require manual curation.

The gap here is automation: We have structure (KGs) and we have automation (LLMs), but they are rarely integrated in a way that allows the graph to evolve autonomously.

---

## Slide 9: Agentic Systems

**Visual Concept:** A robot (Agent) working at a desk that is completely cleared/erased every time the lights go out.

**Slide Content:**
- Autonomous task execution (Denario, Trinkenreich et al.)
- Tool orchestration
- **Limitations:**
  - Ephemeral memory
  - No structural persistence
  - Weak auditability

**Speaker Notes:**
This brings us to Agentic Systems, like the Denario project or the frameworks discussed by Trinkenreich.

These agents can execute complex, multi-step research tasks. But they suffer from "amnesia."

Their memory is limited to the context window. Once the session ends, the structural state of the research is lost. They lack a persistent substrate to anchor their reasoning over time.

---

## Slide 10: Empirical Evaluation Standards

**Visual Concept:** A clipboard with a checklist and a ruler.

**Slide Content:**
- Ralph et al. (2021): Empirical Standards for SE
- Baltes et al. (2025): Guidelines for LLM Studies
- **Observation:** Many systems lack structured validation frameworks
- **Need:** Longitudinal evaluation

**Speaker Notes:**
Finally, how do we evaluate these systems?

Ralph and Baltes provide excellent standards for Software Engineering and LLM experiments. But current agent research often falls short of these standards.

Evaluations are frequently single-pass or qualitative. We lack longitudinal evaluation frameworks that measure whether an agent is actually maintaining a coherent research state over weeks or months.

---

## Slide 11: Cross-Cutting Gaps in the Literature

**Visual Concept:** A Venn diagram of the surveyed fields with a gaping hole in the center labeled "The Gap".

**Slide Content:**
- **Retrieval** lacks structure
- **Graphs** lack automation
- **Agents** lack persistent memory rigor
- **Evaluation** lacks longitudinal validation
- *This fragmentation motivates new infrastructure.*

**Speaker Notes:**
Synthesizing this literature, we see a clear fragmentation.

Retrieval is unstructured. Graphs are static. Agents are amnesic. And evaluation is short-term.

No single system integrates persistent, structured memory with autonomous agency and rigorous provenance. This fragmentation is the core blocker to true autonomous research.

---

## Slide 12: Positioning My Work

**Visual Concept:** A puzzle piece labeled "Agentic KGs" fitting perfectly into the gap from the previous slide.

**Slide Content:**
- **Intersection:** Agentic systems + Knowledge graph persistence + Span-level traceability
- **Literature Refined:**
  - Need for stronger evaluation
  - Clearer scope (SE focus)
  - Explicit longitudinal testing

**Speaker Notes:**
My work positions itself directly in this gap.

I am proposing an architecture that sits at the intersection of Agentic Systems and Knowledge Graphs, with a specific focus on "span-level traceability."

I am refining the literature's approach by enforcing stronger evaluation standards, focusing specifically on the Software Engineering domain, and introducing explicit longitudinal testing.

---

## Slide 13: Proposed Architecture

**Visual Concept:** A cycle diagram: Human $\to$ Agent $\to$ Knowledge Graph $\to$ Agent $\to$ Human. The KG is central and glowing.

**Slide Content:**
- **Persistent Research State Loop**
- Human-in-the-loop
- Agent-mediated updates
- Knowledge Graph as the "Source of Truth"

**Speaker Notes:**
My proposed architecture is a "Persistent Research State Loop."

Instead of a linear chat, the human and agent collaborate to update a shared, persistent Knowledge Graph.

The Graph becomes the source of truth. The agent reads from the graph to reason, and writes to the graph to store conclusions. The human oversees this process, ensuring the state remains valid.

---

## Slide 14: Core Innovation

**Visual Concept:** A document on the left with a highlighted sentence connected by a line to a specific node in a graph on the right.

**Slide Content:**
- **Span-level evidence alignment**
- **Canonicalization Agent** (De-duplication)
- **Versioned provenance chains**

**Speaker Notes:**
The core innovation is "Span-Level Evidence Alignment."

Unlike standard RAG which retrieves vague chunks, our architecture links every node and edge in the graph back to the specific sentence or span in the source PDF.

We also introduce a "Canonicalization Agent" whose sole job is to ensure we don't have five different nodes for "LLM"—it merges duplicates to keep the graph clean and queryable.

---

## Slide 15: Evaluation Framework

**Visual Concept:** A table showing the validation matrix.

**Slide Content:**
| Claim | Metric | Baseline |
|-------|--------|----------|
| **Span-level alignment** | Precision/Recall/F1 | Standard RAG |
| **Canonicalization** | Cohen’s $\kappa$ | Embedding clustering |
| **Traceability** | Audit completeness % | RAG w/ citations |
| **Persistence** | Retention accuracy | Chat-only LLM |

**Speaker Notes:**
To validate this, I propose a rigorous evaluation matrix.

We will measure **Alignment** using Precision and Recall against human baselines.
We will measure **Canonicalization** using Cohen's Kappa to assess agreement.
Crucially, we measure **Persistence**: Does the system actually retain knowledge better than a long-context chat window over a 4-week period?

---

## Slide 16: Experimental Design Overview

**Visual Concept:** A timeline graphic spanning 4 weeks.

**Slide Content:**
- **Dataset:** Annotated span dataset from SE literature
- **Injection:** Synthetic duplicate injection to test canonicalization
- **Audit:** Human traceability audit
- **Task:** 4-week longitudinal retention task

**Speaker Notes:**
The experimental design involves a 4-week longitudinal study.

We will use a dataset of annotated SE papers. We'll inject synthetic duplicates to stress-test the canonicalization agent.

And we will perform human audits to verify that the provenance chains remain unbroken as the graph evolves.

---

## Slide 17: Contributions

**Visual Concept:** Three distinct icons: A Scroll (Definition), A Gear (Protocol), and A Server (Infrastructure).

**Slide Content:**
1. **Formal definition** of Research State
2. **Agentic Curation Protocol** for graph maintenance
3. **Reference infrastructure** implementation

**Speaker Notes:**
The expected contributions are threefold:

First, a formal definition of what "Research State" actually is in an AI context.
Second, a protocol for how agents should curate and maintain this state.
And third, a reference implementation of the infrastructure that others can build upon.

---

## Slide 18: Near-Term Work

**Visual Concept:** A roadmap graphic with "Now" and "Next" markers.

**Slide Content:**
- Controlled evaluation studies
- Artifact release (Code & Datasets)
- SE-focused deployment

**Speaker Notes:**
In the near term, my focus is on executing the controlled evaluation studies and releasing the artifacts.

I aim to deploy this specifically for Software Engineering literature reviews to demonstrate its utility in a concrete domain.

---

## Slide 19: Long-Term Vision

**Visual Concept:** A horizon line with multiple domain icons (Biology, Physics, CS).

**Slide Content:**
- Cross-domain expansion
- Persistent AI-assisted research infrastructure
- Structured memory for scientific discovery

**Speaker Notes:**
Long term, this vision extends beyond Software Engineering.

I see this as the foundation for persistent AI-assisted research infrastructure across all scientific domains. It is about creating the "structured memory" required for autonomous scientific discovery.

---

## Slide 20: Conclusion

**Visual Concept:** A simple arrow pointing from "Chat" to "Infrastructure".

**Slide Content:**
- **From:** Fragmented chat interaction
- **To:** Persistent, traceable research state
- **Goal:** Infrastructure for discovery

**Speaker Notes:**
To conclude:

We are moving from an era of fragmented, ephemeral chat interactions to an era of persistent, traceable research state.

This infrastructure is the missing link to enabling true AI-assisted discovery.

Thank you. I am happy to take your questions.
