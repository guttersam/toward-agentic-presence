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

These findings support a broader continuity thesis:

> Continuity is not merely the persistence of memory or behavior; it appears to depend on geometry-preserving latent dynamics, heterogeneous modular interaction, selective activation, and temporally structured state evolution.

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
- persistent coupling between perception, memory, role, policy, and action

This moves the discussion beyond the question:

> “Can the system remember?”

toward the more architectural question:

> “Does the remembered structure remain causally active in the system’s ongoing dynamics?”

---

## References

[1] Ortega Caro, J., Zhang, Y., Batchelor, H. M., He, S., Cardin, J., & Saxena, S. (2026). *FLUX: Geometry-Aware Longitudinal Flow Matching with Mixture of Experts*. arXiv:2605.08648.

[2] Voce, A., Giannakakis, E., & Clopath, C. (2026). *Cortico-cerebellar modularity as an architectural inductive bias for efficient temporal learning*. arXiv:2605.10356.

[3] Lewis, L., Wang, Z., Schwab, D., & Pitkow, X. (2026). *How Much is Brain Data Worth for Machine Learning?* arXiv:2605.09243.

[4] Shi, Q., Che, Y., Liu, F., Li, H., Xu, M., Reinert, S., Goltstein, P. M., Zhao, R., & Shi, L. (2026). *Joint sparse coding and temporal dynamics support context reconfiguration*. arXiv:2605.10178.

---

## BibTeX

```bibtex
@article{ortegacaro2026flux,
  title={FLUX: Geometry-Aware Longitudinal Flow Matching with Mixture of Experts},
  author={Ortega Caro, Josue and Zhang, Yongxu and Batchelor, Hanna M. and He, Sizhuang and Cardin, Jessica and Saxena, Shreya},
  journal={arXiv preprint arXiv:2605.08648},
  year={2026}
}

@article{voce2026corticocerebellar,
  title={Cortico-cerebellar modularity as an architectural inductive bias for efficient temporal learning},
  author={Voce, Alexandra and Giannakakis, Emmanouil and Clopath, Claudia},
  journal={arXiv preprint arXiv:2605.10356},
  year={2026}
}

@article{lewis2026brain,
  title={How Much is Brain Data Worth for Machine Learning?},
  author={Lewis, Lane and Wang, Zhixin and Schwab, David and Pitkow, Xaq},
  journal={arXiv preprint arXiv:2605.09243},
  year={2026}
}

@article{shi2026sparse,
  title={Joint sparse coding and temporal dynamics support context reconfiguration},
  author={Shi, Qianqian and Che, Yue and Liu, Faqiang and Li, Hongyi and Xu, Mingkun and Reinert, Sandra and Goltstein, Pieter M. and Zhao, Rong and Shi, Luping},
  journal={arXiv preprint arXiv:2605.10178},
  year={2026}
}
```
