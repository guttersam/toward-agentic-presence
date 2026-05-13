# Ongoing Research Addendum: Continuity Architecture

## Cross-Domain Signals Toward Persistent Agentic Continuity

### Status

This is an interpretive research note. The cited papers do **not** all use the language of
“agentic continuity,” “identity topology,” or “unresolved concerns.” Those are continuity-architecture
terms used here to connect their results to the broader thesis.

### Central Claim

Recent work across machine learning, neuroscience, continual learning, biological dynamics, and modular cognition is independently pointing toward a shared architectural pressure:

> Stable intelligence appears to require persistent, coupled dynamics across time rather than isolated inference episodes.

Across these papers, several recurring motifs appear:

- latent regime structure
- geometry-aware state evolution
- heterogeneous modular cognition
- sparse context partitioning
- temporal continuity
- persistent representational structure
- trajectory-conditioned adaptation
- cross-timescale interaction
- self-evolving memory organization
- event-structured reasoning
- identity-anchor resilience
- memory-topology-guided inference
- activation-level participation

Together, these works support the hypothesis that continuity is not merely produced by prompting, retrieval, persona consistency, or surface memory. A stronger account treats continuity as a structural property of systems whose internal representations, temporal dynamics, and action policies remain causally coupled across time.

---

## 1. FLUX: Geometry-Aware Longitudinal Flow Matching

**Paper:** Ortega Caro et al., *FLUX: Geometry-Aware Longitudinal Flow Matching with Mixture of Experts* [1].

### What the paper shows

FLUX models biological systems as longitudinal dynamical processes observed through unpaired population snapshots. Instead of assuming matched trajectories, it learns transport between successive marginal distributions while accounting for curved low-dimensional manifolds embedded in high-dimensional measurements [1].

The model combines:

- geometry-aware conditional paths
- longitudinal flow matching
- sparse mixture-of-experts velocity fields
- unsupervised latent regime discovery

A key contribution is that FLUX does not only infer changing states; it attempts to identify changes in the **transport mechanism itself** through expert routing over local vector fields [1].

### Continuity-architecture interpretation

FLUX is useful for continuity theory because it frames persistence as lawful movement through latent geometry rather than as static state retention.

In continuity terms, this suggests:

> Continuity may require preserving local dynamical transport structure, not merely preserving semantic memory.

This matters because many agent-memory systems currently operate by retrieving or summarizing past information, then reinserting it into a context window. That may preserve semantic content while failing to preserve the latent geometry that made the prior state operationally meaningful.

The continuity analogue is:

- a memory can be retrieved but not dynamically reactivated;
- a persona can be described but not structurally enacted;
- a prior concern can be summarized but not participate in the current cognitive trajectory.

FLUX suggests a stronger architectural criterion: transitions between cognitive states should preserve the geometry of the underlying state space.

### Transferable idea

**Geometry-aware continuity:**  
A persistent agent should not simply interpolate between memory states, roles, or summaries. It should preserve the local structure of the latent manifold through which its cognition evolves.

---

## 2. Cortico-Cerebellar Modularity as Temporal Learning Bias

**Paper:** Voce, Giannakakis, and Clopath, *Cortico-cerebellar modularity as an architectural inductive bias for efficient temporal learning* [2].

### What the paper shows

This paper tests a heterogeneous modular architecture inspired by cortico-cerebellar loops. A recurrent neural network is augmented with a cerebellar-inspired feedforward module that provides a learned additive bias to the recurrent core [2].

The resulting cortico-cerebellar RNN learns faster and achieves stronger performance than parameter-matched recurrent baselines. Importantly, the authors find that freezing the recurrent core after minimal training while delegating later adaptation to the cerebellar module preserves superior learning efficiency [2].

### Continuity-architecture interpretation

The paper suggests that temporal learning benefits from heterogeneous interacting modules with different computational roles.

In continuity terms, this maps onto a possible pattern:

- a relatively stable recurrent substrate
- plus a faster adaptive modulatory system

This resembles a continuity architecture with:

- stable identity anchors
- adaptive correction layers
- task- or context-sensitive modulation
- asymmetric learning rates across subsystems

The important point is that the cerebellar-like module does not replace the recurrent system. It persistently shapes the recurrent trajectory.

### Transferable idea

**Stable substrate + adaptive modulator:**  
A persistent agent may need a stable identity or world-model substrate, but also a faster corrective system that can modulate behavior without rewriting the whole architecture.

This helps distinguish continuity from total plasticity. A system that updates everything equally may become unstable; a system that updates nothing remains brittle. Continuity may require selectively adaptive modulation over a stable substrate.

---

## 3. Brain Data Value and Latent Alignment

**Paper:** Lewis, Wang, Schwab, and Pitkow, *How Much is Brain Data Worth for Machine Learning?* [3].

### What the paper shows

This paper formalizes when neural recordings can improve machine learning. It models task targets and neural recordings in a linear-Gaussian framework and derives scaling laws for how performance changes with brain samples and task samples [3].

The key concepts include:

- task-brain alignment
- neural/task noise
- latent dimensionality
- exchange rates between brain data and task data
- robustness under distribution shift

A central result is that neural data is useful when recorded brain representations align with task-relevant structure. The paper also emphasizes that brain data can help by identifying invariances: dimensions the model should ignore [3].

### Continuity-architecture interpretation

The paper’s alignment framing transfers directly to memory and continuity systems.

A retrieved memory may exist, but if it is not aligned with the active task, role, concern, or operational state, it may not meaningfully contribute to continuity.

This suggests a distinction between:

- **stored memory**
- **retrieved memory**
- **active memory**
- **aligned memory**

Only the last two are continuity-relevant.

The paper’s point that useful brain data may reveal what to ignore is especially important. Continuity systems may not improve merely by retrieving more information. They may require better suppression of irrelevant trajectories.

### Transferable idea

**Continuity alignment:**  
The value of memory depends not only on whether it is available, but on whether it aligns with the active latent structure of the current situation.

This suggests that continuity architectures should include mechanisms for:

- relevance weighting
- suppression of irrelevant memories
- active-state alignment
- latent-subspace matching
- distinction between storage and participation

---

## 4. Sparse Coding and Temporal Dynamics for Context Reconfiguration

**Paper:** Shi et al., *Joint sparse coding and temporal dynamics support context reconfiguration* [4].

### What the paper shows

This paper studies how systems preserve prior representations while adapting to new contexts. It identifies two cooperative mechanisms:

1. sparse coding
2. temporal dynamics

In mouse medial prefrontal cortex and computational models, sparse context-dependent representations reduce cross-context interference, while temporal dynamics further enhance separability across time [4].

The paper also connects these mechanisms to catastrophic forgetting in artificial systems. Networks with both sparse coding and temporal dynamics show improved retention during lifelong learning without auxiliary heuristics [4].

### Continuity-architecture interpretation

This is highly relevant to continuity because it addresses the stability-flexibility problem directly.

Sparse coding supports context partitioning:

- different contexts recruit partially distinct ensembles;
- overlap is preserved but limited;
- interference is reduced.

Temporal dynamics support continuity of unfolding structure:

- temporal order matters;
- contiguous temporal sequences carry information not captured by unordered samples;
- context representations become more discriminable when their temporal structure is preserved.

In continuity terms:

> Continuity is not static memory. It is structured temporal unfolding with selective activation.

The strongest implication is that sparse coding alone is not enough, and temporal dynamics alone are not enough. Their interaction produces improved lifelong learning.

### Transferable idea

**Sparse temporal continuity:**  
Persistent agents may require sparse conditional activation plus temporally structured state evolution.

This suggests that a continuity system should not activate all memories, roles, schemas, and concerns globally. It should selectively recruit partially overlapping structures while preserving their temporal dynamics across context transitions.

---


## 5. Sophia: Persistent Agent Framework and System 3

**Paper:** Sun, Hong, and Zhang, *Sophia: A Persistent Agent Framework of Artificial Life* [5].

### What the paper shows

Sophia argues that existing LLM-agent stacks are largely reactive. They may combine fast perception-like behavior with slower deliberative reasoning, but still lack a persistent meta-layer able to maintain identity, audit internal reasoning, and align short-term tasks with long-term survival or adaptation [5].

The paper introduces a proposed **System 3** layer grounded in:

- meta-cognition
- theory of mind
- intrinsic motivation
- episodic memory
- persistent self- and user-models
- hybrid reward signals
- process-supervised thought search

Sophia is presented as a persistent wrapper around an LLM-centric System 1/System 2 stack. Its purpose is to add continuous self-improvement, autobiographical memory, goal generation, self-assessment, and narrative identity across time [5].

### Continuity-architecture interpretation

Sophia is highly relevant because it treats persistence as more than external memory. It frames continuity as an architectural problem requiring a supervisory meta-cognitive layer that can monitor, audit, update, and reorient the agent over time.

In continuity terms, Sophia supports the idea that an agent requires more than a prompt-defined persona or retrieved background notes. It needs a persistent self-model that can:

- remember prior goals;
- assess capability gaps;
- generate new learning targets;
- preserve autobiographical coherence;
- connect current actions to longer-horizon development.

However, Sophia still largely frames persistence through a modular System 3 wrapper. The continuity-architecture question goes one step further: do the self-model, memory graph, rewards, and identity structures actually participate in the agent's next act of cognition, or do they remain supervisory metadata around otherwise discontinuous inference?

### Transferable idea

**Meta-cognitive persistence:**  
Persistent agents require a layer that monitors and updates the agent's own reasoning, goals, memory, and self-model across time.

For TAP, Sophia is useful as an allied framework. It supports the need for a third stratum of persistent governance, while TAP further asks how that governance becomes structurally coupled into activation, attention, selection, planning, and action.

---

## 6. MMAG: Mixed Memory-Augmented Generation

**Paper:** Zeppieri, *MMAG: Mixed Memory-Augmented Generation for Large Language Models Applications* [6].

### What the paper shows

MMAG proposes a layered memory pattern for LLM-based agents. Rather than treating memory as a flat retrieval store, it divides agent memory into interacting categories:

- conversational memory
- long-term user memory
- episodic and event-linked memory
- sensory and context-aware memory
- short-term working memory

The paper maps these categories to technical components such as dialogue histories, secure profile stores, vector databases, scheduling modules, contextual signals, and temporary scratchpads [6]. It also emphasizes coordination, prioritization, conflict resolution, storage, retrieval, privacy, and latency as practical concerns for memory-rich systems.

### Continuity-architecture interpretation

MMAG is useful because it reinforces the claim that memory is heterogeneous. Different memory types serve different roles in cognition and interaction.

A continuity architecture should therefore not ask only whether an agent has memory. It should ask which memory systems exist, how they interact, and which ones are active during a given cognitive event.

For example:

- conversational memory sustains local thread coherence;
- long-term user memory supports personalization;
- event-linked memory enables time-sensitive recall;
- context-aware memory grounds the current situation;
- working memory supports temporary manipulation during a task.

These are not interchangeable. Continuity may fail if the right memory exists but is routed through the wrong layer, retrieved at the wrong time, or inserted without relation to current operational state.

### Transferable idea

**Heterogeneous memory coordination:**  
Persistent continuity requires multiple memory types to be coordinated rather than collapsed into a single retrieval channel.

For TAP, MMAG provides a practical taxonomy, but TAP adds the stronger requirement that these layers must be actively coupled into role enactment, goal selection, unresolved concerns, planning, and behavioral routing.

---

## 7. Agent Memory Survey: Forms, Functions, and Dynamics

**Paper:** Hu et al., *Memory in the Age of AI Agents: A Survey — Forms, Functions and Dynamics* [7].

### What the paper shows

This survey argues that traditional short-term/long-term memory distinctions are no longer sufficient for contemporary agent-memory systems. It proposes a multidimensional taxonomy organized around:

1. **Forms** — what carries memory
   - token-level memory
   - parametric memory
   - latent memory

2. **Functions** — why memory is needed
   - factual memory
   - experiential memory
   - working memory

3. **Dynamics** — how memory operates and evolves
   - memory formation
   - memory evolution
   - memory retrieval

The paper also distinguishes agent memory from related ideas such as LLM memory, retrieval-augmented generation, and context engineering [7].

### Continuity-architecture interpretation

This survey is valuable because it moves agent memory away from a simple storage model and toward a lifecycle model. Memory is not merely present or absent; it is formed, updated, consolidated, forgotten, retrieved, transformed, and used under different temporal patterns.

This maps directly onto the continuity question. A memory can be:

- formed but not retrieved;
- retrieved but not aligned;
- aligned but not enacted;
- enacted once but not consolidated;
- consolidated but not allowed to update future behavior.

Continuity depends on the whole lifecycle, not on any single memory operation.

The survey's distinction between agent memory, RAG, and context engineering is especially useful. It supports the claim that larger context windows, better retrieval, or smarter prompt assembly do not by themselves solve continuity. They may improve access to information while leaving unresolved whether that information becomes causally active in the agent's policy.

### Transferable idea

**Memory lifecycle continuity:**  
Continuity should be evaluated across memory formation, evolution, retrieval, and use, not merely by whether relevant facts can be recalled.

For TAP, this survey provides a rigorous vocabulary for situating continuity architecture within the broader agent-memory field.

---

## 8. A-Mem: Agentic Memory and Self-Evolving Memory Networks

**Paper:** Xu et al., *A-Mem: Agentic Memory for LLM Agents* [8].

### What the paper shows

A-Mem argues that many existing memory systems depend on predefined structures, fixed workflows, and static memory operations. To address this, it proposes an agentic memory system inspired by the Zettelkasten method [8].

When a new memory is added, A-Mem constructs a structured note containing:

- original content
- timestamp
- LLM-generated keywords
- tags
- contextual description
- embeddings
- links to related memories

The system then performs dynamic link generation and memory evolution. New memories can create connections to older memories, and older memories can have their context, keywords, and tags updated in response to new experience [8].

### Continuity-architecture interpretation

A-Mem is important because it shows memory as an evolving knowledge network rather than an archive. New experiences do not simply accumulate; they can reorganize prior memories.

This supports a key continuity principle:

> A persistent agent should not only remember the past; the past should become reorganized in light of later experience.

That is close to human autobiographical memory, where later events can change how earlier events are interpreted. For agent continuity, this suggests that memory should be plastic at the structural level, not just additive at the storage level.

However, A-Mem still primarily addresses the organization and retrieval layer. TAP extends the question into activation: after memories are linked and evolved, do those evolved structures actually shape attention, planning, role behavior, unresolved task selection, and action?

### Transferable idea

**Self-evolving memory topology:**  
New experiences should be able to update the organization and meaning of prior memory.

For TAP, A-Mem supports the idea that continuity is not memory accumulation. It is ongoing reorganization plus active participation in later cognition.

---

## 9. CompassMem: Event-Centric Memory as a Logic Map

**Paper:** Hu, Liu, Tan, Zhu, and Dou, *Memory Matters More: Event-Centric Memory as a Logic Map for Agent Searching and Reasoning* [9].

### What the paper shows

CompassMem argues that flat memory and shallow semantic retrieval are insufficient for long-horizon reasoning. It organizes memory as an **Event Graph**, where experiences are segmented into coherent event units and linked by explicit logical relations such as causality, temporal order, motivation, and part-of relations [9].

The paper's central idea is that memory should function as a **logic map**. During inference, the agent does not merely retrieve similar text snippets. It actively navigates the event graph, follows meaningful relations, decomposes queries into subgoals, explores multiple paths, and gathers evidence for reasoning [9].

The figure on page 2 of the paper is especially relevant because it visually contrasts:

- unstructured memory using semantic-only retrieval;
- structured memory with weak logic;
- CompassMem, where topology carries logic and becomes part of active searching and reasoning.

### Continuity-architecture interpretation

CompassMem is one of the strongest direct supports for TAP because it treats memory topology as part of reasoning itself.

This matters because TAP's central claim is not merely that memory should be retrievable. It is that memory must become **operative**. CompassMem shows one concrete form of this: event relations guide the reasoning trajectory.

In continuity terms:

- an event is not just a stored fact;
- a relation is not just metadata;
- a graph is not just organization;
- topology becomes an active constraint on inference.

This aligns with TAP's claim that continuity depends on remembered structures continuing to shape future cognition.

### Transferable idea

**Topology-guided reasoning:**  
Memory should provide not only content but navigable structure that directs search, inference, and planning.

For TAP, CompassMem is a major bridge between memory architecture and activation architecture. It demonstrates that memory structure can become part of the reasoning path rather than merely context supplied before reasoning begins.

---

## 10. Persistent Identity: Multi-Anchor Resilience

**Paper:** Menon, *Persistent Identity in AI Agents: A Multi-Anchor Architecture for Resilient Memory and Continuity* [10].

### What the paper shows

This paper reframes context-window overflow and summarization loss as an identity-continuity problem, not merely a retrieval problem. When older conversation history is compressed or lost, the agent may behave as if the thread of collaboration has been severed [10].

The paper argues that current AI agents often centralize identity in a single memory store, creating a single point of failure. Drawing on neurological case studies, it proposes that identity should be distributed across multiple anchors, analogous to how human identity can persist through partial memory impairment [10].

The proposed anchors include separable identity and memory structures such as:

- stable identity files
- memory logs
- procedural memory
- salience records
- relationship records
- identity drift checks

The key concept is **anchor resilience**: identity should survive partial failure because no single memory channel contains the whole agent.

### Continuity-architecture interpretation

This is directly useful for TAP's identity-continuity argument. It supports the claim that continuity is fragile when centralized. If an agent's identity depends on one prompt, one summary, one vector store, or one memory file, then continuity has a single failure point.

Distributed anchors make continuity more resilient. However, TAP adds an additional criterion: anchors must not merely exist. They must be activated and integrated at the moment behavior is generated.

A system can have many identity anchors and still behave discontinuously if those anchors are not coupled into:

- attention;
- goal selection;
- role interpretation;
- affordance recognition;
- planning;
- refusal/public-action gating;
- self-model updates.

### Transferable idea

**Redundant identity anchoring:**  
Identity should be distributed across multiple partially independent structures so that continuity can survive failure of any single memory channel.

For TAP, this supports the need for resilience, while TAP extends it into an activation claim: anchors preserve continuity only when they participate in live cognition.

---

## TAP Extension: From Memory Architecture to Activation Architecture

Recent agent-memory work increasingly converges on the insufficiency of flat retrieval. A-Mem shows that memory systems can dynamically link and evolve stored experiences rather than merely retrieve static records [8]. CompassMem goes further by treating event-structured memory as a logic map that actively guides search and reasoning, implying that memory topology itself can shape inference [9]. Persistent Identity in AI Agents reframes catastrophic forgetting as an identity-continuity failure and argues for distributed identity anchors rather than reliance on a single memory store [10]. Together, these works support TAP's central claim: continuity does not arise from stored memory alone, but from memory structures that remain dynamically organized, redundantly anchored, and actively coupled into future reasoning and behavioral routing.

TAP extends this trajectory by shifting the focus from **memory architecture** alone to **activation architecture**. Where these systems improve how memories are stored, linked, retrieved, navigated, or protected, TAP asks whether those structures actually become operative in the agent's next act of cognition. Its contribution is the claim that continuity requires more than organized memory or resilient identity anchors: remembered events, roles, unresolved concerns, goals, procedural habits, and operational state must be recurrently activated together in ways that shape selection, attention, planning, refusal, action, and self-model updating.

In this sense, TAP treats continuity as a topology of participation rather than a property of storage. The relevant question is not only whether the agent can retrieve the right record, but whether the retrieved or persistent structure changes what the agent is likely to notice, choose, avoid, continue, revise, or enact.

---

## Unified Synthesis

Across these papers, a coherent architectural direction emerges.

Persistent intelligence increasingly appears to require:

1. **Geometry-aware latent transport**  
   FLUX suggests that dynamical transitions must respect latent geometry rather than rely on naive interpolation [1].

2. **Heterogeneous modular interaction**  
   Cortico-cerebellar models suggest that stable recurrent substrates and fast adaptive modulatory systems can cooperate efficiently [2].

3. **Latent representational alignment**  
   Brain-data scaling laws suggest that internal representations matter when they align with task-relevant structure and reveal useful invariances [3].

4. **Sparse temporal context partitioning**  
   Sparse coding and temporal dynamics suggest that preserving prior knowledge while adapting to new contexts requires selective activation plus temporal continuity [4].

5. **Meta-cognitive persistence**  
   Sophia suggests that persistent agents require a higher-order layer capable of self-monitoring, self-modeling, memory maintenance, and long-horizon adaptation [5].

6. **Heterogeneous memory coordination**  
   MMAG suggests that conversational, long-term, episodic, contextual, and working memory should be treated as distinct but interacting systems [6].

7. **Memory lifecycle dynamics**  
   The agent-memory survey suggests that memory should be understood through forms, functions, and dynamics: what carries memory, what memory does, and how it forms, evolves, and is retrieved [7].

8. **Self-evolving memory topology**  
   A-Mem suggests that memory systems can dynamically link new experiences to older ones and update existing memory representations as knowledge evolves [8].

9. **Topology-guided reasoning**  
   CompassMem suggests that event-structured memory can function as a logic map that actively guides search and reasoning [9].

10. **Redundant identity anchoring**  
    Persistent Identity in AI Agents suggests that identity should be distributed across multiple anchors to survive partial memory failure [10].

These findings support a broader continuity thesis:

> Continuity is not merely the persistence of memory or behavior; it appears to depend on geometry-preserving latent dynamics, heterogeneous modular interaction, selective activation, temporally structured state evolution, self-evolving memory topology, and identity anchors that remain actively coupled into cognition.

---

## Implications for Agent Architecture

The papers point toward several design principles for persistent agents.

### 1. Memory should be dynamically active, not merely retrievable

Stored memories do not automatically create continuity. A memory becomes continuity-relevant only when it participates in current state evolution.

### 2. Agent state should preserve geometry

If prior states are compressed into summaries, the system may lose the structure needed for lawful continuation. A continuity architecture should preserve relationships, trajectories, and latent constraints, not only facts.

### 3. Modularity should be heterogeneous

Different subsystems should operate at different timescales and with different plasticity profiles. Stable identity, fast correction, procedural adaptation, and long-term learning may need distinct substrates.

### 4. Selective activation is essential

Dense global activation risks interference. Sparse conditional recruitment may be necessary for maintaining prior representations while adapting to new contexts.

### 5. Temporal order is structural

Continuity is not just a set of remembered facts. The order and unfolding of prior states may carry information that unordered retrieval cannot preserve.

### 6. Memory topology should guide reasoning

Memory graphs, event relations, and causal/temporal links should not only organize storage. They should provide navigable structure that shapes search and inference.

### 7. Identity should be distributed across anchors

A persistent agent should not depend on a single prompt, summary, memory file, or vector store for continuity. Identity-relevant information should be distributed across partially independent anchors.

### 8. Memory should evolve, not only accumulate

New experiences should be able to reorganize the interpretation, links, salience, and context of older memories.

### 9. Continuity requires activation, not just architecture

Even a well-organized memory system can remain discontinuous if its contents do not participate in live cognition. The decisive question is whether memory, identity, role, operational state, and unresolved concerns alter what the agent notices, selects, plans, refuses, and does.

---

## Relation to the Core Continuity Thesis

The core thesis remains:

> A chatbot can imitate a persona, remember facts, follow instructions, and act emotional while still remaining structurally discontinuous.

These papers help specify what structural continuity may require.

A structurally continuous agent may need:

- latent state geometry
- regime-sensitive dynamics
- sparse context-conditioned activation
- multi-timescale modularity
- active alignment between stored memory and current cognition
- temporally ordered state evolution
- self-evolving memory topology
- event-centered logic maps
- heterogeneous memory coordination
- multi-anchor identity resilience
- activation-level participation of memory and role
- persistent coupling between perception, memory, role, policy, and action

This moves the discussion beyond the question:

> “Can the system remember?”

toward the more architectural question:

> “Does the remembered structure remain causally active in the system’s ongoing dynamics?”

TAP sharpens this further:

> “Does the system's memory, identity, role, operational state, unresolved concerns, and procedural habits participate together in the activation topology that produces the next behavior?”

---

## References

[1] Ortega Caro, J., Zhang, Y., Batchelor, H. M., He, S., Cardin, J., & Saxena, S. (2026). *FLUX: Geometry-Aware Longitudinal Flow Matching with Mixture of Experts*. arXiv:2605.08648. https://arxiv.org/abs/2605.08648

[2] Voce, A., Giannakakis, E., & Clopath, C. (2026). *Cortico-cerebellar modularity as an architectural inductive bias for efficient temporal learning*. arXiv:2605.10356. https://arxiv.org/abs/2605.10356

[3] Lewis, L., Wang, Z., Schwab, D., & Pitkow, X. (2026). *How Much is Brain Data Worth for Machine Learning?* arXiv:2605.09243. https://arxiv.org/abs/2605.09243

[4] Shi, Q., Che, Y., Liu, F., Li, H., Xu, M., Reinert, S., Goltstein, P. M., Zhao, R., & Shi, L. (2026). *Joint sparse coding and temporal dynamics support context reconfiguration*. arXiv:2605.10178. https://arxiv.org/abs/2605.10178

[5] Sun, M., Hong, F., & Zhang, W. (2025). *Sophia: A Persistent Agent Framework of Artificial Life*. arXiv:2512.18202. https://arxiv.org/abs/2512.18202

[6] Zeppieri, S. (2025). *MMAG: Mixed Memory-Augmented Generation for Large Language Models Applications*. arXiv:2512.01710. https://arxiv.org/abs/2512.01710

[7] Hu, Y., Liu, S., Yue, Y., Zhang, G., et al. (2026). *Memory in the Age of AI Agents: A Survey — Forms, Functions and Dynamics*. arXiv:2512.13564. https://arxiv.org/abs/2512.13564

[8] Xu, W., Liang, Z., Mei, K., Gao, H., Tan, J., & Zhang, Y. (2025). *A-Mem: Agentic Memory for LLM Agents*. arXiv:2502.12110. https://arxiv.org/abs/2502.12110

[9] Hu, Y., Liu, J., Tan, J., Zhu, Y., & Dou, Z. (2026). *Memory Matters More: Event-Centric Memory as a Logic Map for Agent Searching and Reasoning*. arXiv:2601.04726. https://arxiv.org/abs/2601.04726

[10] Menon, P. G. (2026). *Persistent Identity in AI Agents: A Multi-Anchor Architecture for Resilient Memory and Continuity*. arXiv:2604.09588. https://arxiv.org/abs/2604.09588

---

## BibTeX

```bibtex
@article{ortegacaro2026flux,
  title={FLUX: Geometry-Aware Longitudinal Flow Matching with Mixture of Experts},
  author={Ortega Caro, Josue and Zhang, Yongxu and Batchelor, Hanna M. and He, Sizhuang and Cardin, Jessica and Saxena, Shreya},
  journal={arXiv preprint arXiv:2605.08648},
  year={2026},
  url={https://arxiv.org/abs/2605.08648}
}

@article{voce2026corticocerebellar,
  title={Cortico-cerebellar modularity as an architectural inductive bias for efficient temporal learning},
  author={Voce, Alexandra and Giannakakis, Emmanouil and Clopath, Claudia},
  journal={arXiv preprint arXiv:2605.10356},
  year={2026},
  url={https://arxiv.org/abs/2605.10356}
}

@article{lewis2026brain,
  title={How Much is Brain Data Worth for Machine Learning?},
  author={Lewis, Lane and Wang, Zhixin and Schwab, David and Pitkow, Xaq},
  journal={arXiv preprint arXiv:2605.09243},
  year={2026},
  url={https://arxiv.org/abs/2605.09243}
}

@article{shi2026sparse,
  title={Joint sparse coding and temporal dynamics support context reconfiguration},
  author={Shi, Qianqian and Che, Yue and Liu, Faqiang and Li, Hongyi and Xu, Mingkun and Reinert, Sandra and Goltstein, Pieter M. and Zhao, Rong and Shi, Luping},
  journal={arXiv preprint arXiv:2605.10178},
  year={2026},
  url={https://arxiv.org/abs/2605.10178}
}

@article{sun2025sophia,
  title={Sophia: A Persistent Agent Framework of Artificial Life},
  author={Sun, Mingyang and Hong, Feng and Zhang, Weinan},
  journal={arXiv preprint arXiv:2512.18202},
  year={2025},
  url={https://arxiv.org/abs/2512.18202}
}

@article{zeppieri2025mmag,
  title={MMAG: Mixed Memory-Augmented Generation for Large Language Models Applications},
  author={Zeppieri, Stefano},
  journal={arXiv preprint arXiv:2512.01710},
  year={2025},
  url={https://arxiv.org/abs/2512.01710}
}

@article{hu2026memorysurvey,
  title={Memory in the Age of AI Agents: A Survey: Forms, Functions and Dynamics},
  author={Hu, Yuyang and Liu, Shichun and Yue, Yanwei and Zhang, Guibin and others},
  journal={arXiv preprint arXiv:2512.13564},
  year={2026},
  url={https://arxiv.org/abs/2512.13564}
}

@article{xu2025amem,
  title={A-Mem: Agentic Memory for LLM Agents},
  author={Xu, Wujiang and Liang, Zujie and Mei, Kai and Gao, Hang and Tan, Juntao and Zhang, Yongfeng},
  journal={arXiv preprint arXiv:2502.12110},
  year={2025},
  url={https://arxiv.org/abs/2502.12110}
}

@article{hu2026compassmem,
  title={Memory Matters More: Event-Centric Memory as a Logic Map for Agent Searching and Reasoning},
  author={Hu, Yuyang and Liu, Jiongnan and Tan, Jiejun and Zhu, Yutao and Dou, Zhicheng},
  journal={arXiv preprint arXiv:2601.04726},
  year={2026},
  url={https://arxiv.org/abs/2601.04726}
}

@article{menon2026persistentidentity,
  title={Persistent Identity in AI Agents: A Multi-Anchor Architecture for Resilient Memory and Continuity},
  author={Menon, Prahlad G.},
  journal={arXiv preprint arXiv:2604.09588},
  year={2026},
  url={https://arxiv.org/abs/2604.09588}
}
```
