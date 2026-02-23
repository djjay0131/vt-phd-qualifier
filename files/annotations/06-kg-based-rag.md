## Paper: A Knowledge Graph-based RAG for Cross-Document Information Extraction

**Authors:** Sudhanshu Suryawanshi, Shreyas Waghmode, Ritesh Sawant, Dr. Megha Gupta
**Year:** 2025
**Venue:** ICPCSN-2025 (IEEE), 5th International Conference on Pervasive Computing and Social Networking
**BibTeX Key:** suryawanshi2025kgrag

### Summary (2-3 sentences)

This paper proposes a Knowledge Graph-based Retrieval-Augmented Generation (RAG) system that constructs a domain-specific knowledge graph from research papers and combines vector search with graph-based retrieval to extract cross-document information. The system addresses the limitations of LLMs' finite context windows and their difficulty in linking concepts scattered across multiple documents by building structured, interpretable representations of research knowledge. Evaluated on a corpus of 10 RAG-related research papers, the system constructs a graph of 2,601 entities and 3,052 relations organized into 311 communities, demonstrating that structured graph-aided retrieval outperforms traditional vector-only techniques for cross-document context management.

### Key Contributions

- **Hybrid retrieval architecture:** Combines vector search (semantic similarity over entity embeddings) with graph-based retrieval (relationship traversal in a knowledge graph), providing both precision and contextual breadth.
- **Domain-specific KG construction pipeline:** Defines a structured process for extracting research-specific entity types (concepts, topics, persons, papers, models, methods, equations, variables) and relationship types (co-author, affiliation, citation, methodology, result, tool/resource) from academic papers.
- **Enhanced entity descriptions for vector searchability:** Augments KG nodes with natural language descriptions that serve as a bridge between diverse queries and structured graph entities, improving hybrid search coherence.
- **Hierarchical KG summarization:** Introduces a method for generating structured summaries from the knowledge graph by identifying central nodes, extracting sub-graphs, detecting communities (Louvain method), and organizing content into subtopics.
- **Community detection for knowledge structuring:** Applies the Louvain algorithm to partition the KG into meaningful sub-graphs, enabling divide-and-conquer summarization of large knowledge bases.

### Architecture/Method

The system follows a multi-stage pipeline:

1. **Document Loading and Chunking:** 10 research papers (PDFs) are converted to text using LangChain's PyPDFLoader and split into chunks of 2,560 characters with 250-character overlap using RecursiveCharacterTextSplitter. Chunk size was tuned experimentally to balance coherence with model context limits.

2. **Knowledge Graph Construction:**
   - *Entity Recognition:* An LLM identifies and categorizes entities into domain-specific types: concepts, topics, persons, papers, models, methods, equations, and variables. Each entity is augmented with a brief natural language description to improve vector search accuracy.
   - *Relation Extraction:* Relationships between entities are extracted and classified into types such as Co-author, Affiliation, Citation, Result, Methodology, Funding, Research Area, and Tool/Resource. Each relationship also receives a description.

3. **Community Detection:** The Louvain method partitions the knowledge graph into communities of related entities, revealing hidden structures and enabling sub-graph-level processing.

4. **Hierarchical KG Summarization:**
   - Select the highest-degree central node as the focal point.
   - Extract a sub-graph around it (depth of 3).
   - Filter out non-conceptual nodes (people, organizations, locations).
   - Use an LLM to generate subtopics from the child nodes' neighborhoods.
   - Compile node-level summaries, aggregate by subtopic, and merge into a final structured summary.

5. **Vector Search-Aided Retrieval (for query answering):**
   - *Keyword Extraction:* An LLM extracts keywords from the user query.
   - *Vector Search:* KG entities (stored as embeddings with name, type, description) are retrieved by semantic similarity to the query keywords.
   - *Graph-Based Retrieval:* Retrieved entities are mapped back to the KG; neighboring relationships are extracted for contextual enrichment.
   - *Contextual Summarization:* An LLM synthesizes the retrieved knowledge into a coherent response.

### Knowledge Representation Approach

The paper represents knowledge through a **domain-specific knowledge graph** tailored to academic literature. Key aspects:

- **Entity types** are chosen specifically for research papers (not generic NER categories like Person/Organization/Location): concepts, topics, persons, papers, models, methods, equations, and variables.
- **Relationship types** capture academic-specific connections: co-authorship, affiliation, citation, methodology, results, funding, research area, and tools/resources.
- **Entity descriptions** serve as a critical bridge between the structured graph and the unstructured vector space. By attaching natural language descriptions to every entity, the system enables vector similarity search to find relevant graph nodes even when queries use different terminology.
- **Community structure** provides a meso-level organizational layer between individual entities and the full graph, enabling hierarchical summarization.
- The resulting KG from 10 papers contained 2,601 entities, 3,052 relations, and 311 communities (average 8.36 nodes per community, max 172 nodes).

### Research Tasks Addressed

- **Cross-document information extraction:** Linking concepts, methods, and findings across multiple research papers that cannot fit within a single LLM context window.
- **Multi-document question answering:** Answering queries that require synthesizing information from multiple sources.
- **Research literature summarization:** Generating structured, hierarchical summaries of a corpus of research papers.
- **Knowledge organization for academic literature:** Structuring the implicit knowledge in research papers into an explicit, navigable graph.
- **Reducing LLM hallucination:** Using RAG with structured knowledge to ground LLM outputs in actual source content.

### Evaluation Method

The evaluation is primarily **qualitative and descriptive** rather than quantitative with benchmarks:

- **Graph analysis metrics:** Reports structural properties of the constructed KG: 2,601 entities, 3,052 relations, 311 communities, average 8.36 nodes/community, max 172 nodes in a community.
- **Distribution analysis:** Examines distributions of node types (People nodes dominate, followed by Concept, Model, Paper, Topic, Method, Variables, Dataset, Equations) and relationship types (Venue/Publication, Author Role, Methodology, Tools/Resources are most common).
- **Degree distribution:** Analyzes the top-10 highest-degree nodes to validate that the KG structure aligns with the domain (RAG-related nodes are most connected, matching the paper corpus topic).
- **Summarization output analysis:** Reports that the hierarchical summarization produced a document of 12,356 words and 85,910 characters covering various subtopics with cross-document contextualization.
- **Qualitative observations on retrieval quality:** States that the vector search-aided retrieval "consistently produced well-structured, comprehensive responses" but does not provide quantitative retrieval metrics (precision, recall, F1, etc.).
- **No formal baselines or comparative benchmarks** are reported.

### Strengths

- **Practical and well-defined pipeline:** The multi-stage architecture (chunking, entity extraction, relation extraction, community detection, hierarchical summarization, hybrid retrieval) is clearly described and implementable.
- **Domain-specific entity and relation types:** Tailoring entity/relation categories to academic literature (rather than using generic NER) captures richer, more relevant structure for research knowledge management.
- **Entity description augmentation:** The insight that adding natural language descriptions to KG nodes bridges the gap between structured graph search and unstructured vector search is valuable and practically useful.
- **Hybrid retrieval combining vector and graph search:** Leveraging both semantic similarity (vector) and structural relationships (graph traversal) provides complementary retrieval capabilities.
- **Interpretability:** The knowledge graph provides a transparent, traceable representation of how information is organized and retrieved, unlike black-box retrieval approaches.
- **Hierarchical summarization approach:** The community detection and subtopic-based summarization provides a principled method for generating structured overviews of large knowledge bases.

### Weaknesses/Limitations

- **Weak evaluation:** The paper lacks quantitative evaluation with standard metrics (precision, recall, F1, BLEU, ROUGE, etc.) and has no comparison against baselines. The claims of superiority over "traditional techniques" are not substantiated with empirical evidence.
- **Small scale:** Only 10 research papers were used, all on the same topic (RAG), which limits generalizability claims. Real-world research synthesis tasks involve hundreds or thousands of papers across diverse topics.
- **Entity normalization problems:** The authors themselves acknowledge that semantically equivalent terms (e.g., "Retrieval-Augmented Generation" vs. "RAG," "LLM" vs. "LLMs") are classified as distinct entities, indicating a significant knowledge graph quality issue.
- **Limited search depth:** The sub-graph extraction is constrained to a depth of 3, and the authors acknowledge this may impact summary completeness.
- **Rudimentary node selection:** Central node selection is based solely on degree (number of connections), which may miss important but less-connected concepts.
- **No agentic capabilities:** The system is a static pipeline with no autonomous decision-making, planning, or iterative refinement. It does not qualify as an "agent" in the agentic AI sense -- it is a tool that must be manually invoked.
- **LLM dependency not characterized:** The system relies heavily on LLMs for entity extraction, relation extraction, subtopic generation, and summarization, but the specific models used and their impact on quality are not discussed.
- **Scalability concerns:** Community detection and hierarchical summarization may not scale well to much larger corpora.

### Connections to Other Papers

**Empirical Standards for SE Research (Ralph et al., 2021):**
This KG-RAG paper would benefit from the empirical standards framework. Its evaluation methodology falls short of the rigor that Ralph et al. advocate for -- it lacks formal baselines, quantitative metrics, and reproducibility details. This contrast is useful for arguing that AI-for-research tools need to be evaluated with the same rigor they aim to support.

**Open Problems in Mechanistic Interpretability (Sharkey et al., 2025):**
The KG-RAG paper's emphasis on interpretability (users can trace reasoning through sub-graph matching and semantic similarity) connects to the broader theme of understanding AI systems. While Sharkey et al. focus on interpreting neural network internals, this paper addresses interpretability at the retrieval/knowledge organization level -- a complementary perspective on making AI systems transparent.

**Get on the Train: Using LLMs for SE Research (Trinkenreich et al., 2025):**
Both papers explore how LLMs can augment research workflows. Trinkenreich et al. provide a broad roadmap for LLM use in SE research, while this paper provides a concrete implementation of one such use case -- LLM-powered cross-document information extraction. The KG-RAG system exemplifies the kind of LLM-based research tool that Trinkenreich et al. envision.

**Guidelines for Empirical Studies in SE involving LLMs (Baltes et al., 2025):**
The KG-RAG paper is an example of work that would benefit from the guidelines Baltes et al. propose. Its reliance on LLMs for entity extraction, relation extraction, and summarization introduces quality dependencies that are not characterized or controlled for, which Baltes et al. would flag as a methodological concern.

**The Denario Project (Villaescusa-Navarro et al., 2025):**
Both papers use knowledge graphs for organizing research knowledge, creating a direct architectural parallel. The Denario Project uses agentic KGs for autonomous scientific discovery across domains, while this paper uses a KG for cross-document extraction within a single research topic. Denario represents a more ambitious vision (autonomous agents navigating knowledge graphs), while this paper provides a simpler, more focused implementation of KG-based retrieval. Together, they illustrate a spectrum from tool-level KG use to agent-level KG use in research contexts.

### Useful Quotes (with page numbers)

1. **On the core problem and approach (p. 1, Abstract):**
   > "Extracting information from multiple complex documents, such as research papers is challenging due to LLMs' limited context size and their difficulty linking distant concepts. To address this, [we] propose a Knowledge-Graph-based Retrieval-Augmented Generation (RAG) system that builds a knowledge graph from research papers and uses task-specific retrieval methods -- combining vector and graph search."

2. **On interpretability advantage (p. 1, Introduction):**
   > "The graph-aided system excels in explainability, enabling users to trace the reasoning behind generated outputs through sub-graph matching and semantic similarity, thereby enhancing trust and usability."

3. **On domain-specific KG construction (p. 1, Introduction):**
   > "A key aspect of our approach is the creation of a domain-specific knowledge graph that organizes the concepts, methodologies, and relationships extracted into a structured format. This graph not only improves the accuracy of the retrieval, but also provides a more interpretable framework for research findings, allowing users to quickly navigate relevant methodologies, compare technologies, and identify optimal approaches within a specific domain."

4. **On entity description augmentation for vector searchability (p. 2, Section III-B):**
   > "The integration of descriptions facilitates more accurate similarity assessments by aligning nodes with their intended roles and related concepts... These descriptions act as a bridge between different data sources and queries, ensuring that searches across various inputs remain coherent and relevant."

5. **On entity normalization challenges (p. 5, Results):**
   > "Inconsistencies in entity recognition were observed, where semantically equivalent terms (e.g., 'Retrieval-Augmented Generation' and 'RAG', 'LLM' and 'LLMs') were classified as distinct entities, indicating a need for improved entity normalization techniques to ensure consistency in knowledge representation."

6. **On hierarchical summarization results (p. 5, Results):**
   > "The summarization process resulted in a document containing 12,356 words and 85,910 characters, effectively capturing various subtopics discussed in the input papers while demonstrating strong cross-document contextualization."
