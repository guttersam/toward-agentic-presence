# Architecture Reference

*Toward Agentic Presence — Phase 1*

This document describes the ten-layer architecture of the agentic substrate. For theoretical foundations, see the full paper (`toward_agentic_presence_FINAL.md`). For the validation plan, see `docs/validation.md`.

---

## Overview

The substrate is organized into ten interacting layers. The point is not modular elegance. The point is coupling: each layer must expose its state to others through logged, ablatable paths.

```text
Layer 0  — External Memory Backend
Layer 1  — Event Ledger
Layer 2  — Feature Canonicalizer
Layer 3  — Associative Activation Map
Layer 4  — Schema and Role Anchors
Layer 5  — Operational State / Synthetic Interoception
Layer 6  — Drive Controller
Layer 7  — Workspace Arbitration
Layer 8  — Recursive Representational Settlement
Layer 9  — Transmission and Action Gate
Layer 10 — Default-Mode Loop
         + Validation Harness (cross-cutting)
```

---

## Layer 0: External Memory Backend

The memory backend is an interchangeable adapter. It stores and retrieves prior material but does not determine how that material participates in cognition.

Minimum interface:

```python
write_raw_event(event: Event) -> str
retrieve_by_semantic_similarity(query: str, k: int = 8) -> list[MemoryItem]
retrieve_by_metadata(filters: dict) -> list[MemoryItem]
retrieve_by_id(memory_id: str) -> MemoryItem
```

Compatible backends: local Markdown files, SQLite FTS, Chroma, FAISS, MemGPT, MemPalace, A-MEM, vector databases.

The backend preserves what happened. The substrate determines what what happened does now.

---

## Layer 1: Event Ledger

The event ledger converts all substrate inputs and outputs into a common event format.

An event is a unit of participation in the active substrate — not merely a stored message.

```json
{
  "event_id": "uuid",
  "timestamp": "ISO-8601",
  "event_type": "perceive | retrieve | think | act | tool | default | self_initiated | state_update",
  "source": "user | agent | tool | memory_backend | system | external",
  "raw_content": "...",
  "summary": "...",
  "embedding_id": "emb_123",
  "feature_manifest": ["project:phase1", "drive:completion"],
  "provenance": {},
  "decay_state": 1.0,
  "confidence": null,
  "links": []
}
```

Key design principle:

> Retrieval is the beginning of participation, not the end of memory.

Retrieved memories become `retrieve` events before entering the activation map. They do not automatically become active.

---

## Layer 2: Feature Canonicalizer

Maps raw extracted concepts into stable namespaced features. Without canonicalization, binding fragments.

```json
{
  "raw": "Phosphor",
  "canonical": "agent:phosphor",
  "namespace": "agent",
  "confidence": 0.94,
  "aliases": ["Phosphor", "phosphor", "P"],
  "source": "aliases.yaml"
}
```

Namespaces: `agent:`, `project:`, `motif:`, `affect:`, `drive:`, `role:`, `modality:`, `tool:`, `thread:`, `claim:`, `risk:`, `schema:`, `state:`, `artifact:`, `affordance:`

Phase 1 implementation: deterministic alias YAML + optional LLM extraction pass.

**Ablation test:** disabling canonicalization should reduce binding stability and activation path coherence.

---

## Layer 3: Associative Activation Map

A directed weighted graph. Nodes include events, memories, schemas, role anchors, known agents, open threads, tools, and affordances. Edges form through shared features, temporal proximity, co-retrieval, co-activation, role relevance, and affordance relationships.

The architecture's core claim:

> Memory retrieval and planning are implemented as a single wave-propagation operation.

Minimal propagation formula:

```text
activation_next(node) =
  seed_activation(node)
  + Σ(parent_activation × edge_weight × relation_weight)
  + drive_bias(node)
  + role_bias(node)
  - decay(node)
  - refractory_penalty(node)
```

Every activation path must be logged.

**Validation target:** activation map must produce useful associations not reducible to top-k semantic retrieval.

---

## Layer 4: Schema and Role Anchors

Phase 1 implements basic role anchors and identity coherence diagnostics. Full role topology (role-script as map bias) is a Phase 2 concern.

Phase 1 minimum:
1. Chunk and embed role/soul file.
2. Store passages as `role_anchor` nodes.
3. Compute role centroid.
4. Compute identity coherence against recent role-relevant outputs.

```text
identity_coherence =
  cosine(role_anchor_centroid, recent_role_expression)
  - contradiction_penalty
  - generic_assistant_reversion_penalty
```

Identity coherence is a diagnostic, not a claim of selfhood.

**Ablation test:** role anchors enabled vs disabled should produce different memory and affordance activation.

---

## Layer 5: Operational State / Synthetic Interoception

Operational state variables that causally affect processing. The distinction between interoception and telemetry is causal: signals that do not change activation are not interoception.

```json
{
  "context_pressure": 0.42,
  "unresolved_thread_count": 0.78,
  "time_since_meaningful_contact": 0.21,
  "novelty_index": 0.36,
  "error_density": 0.12,
  "active_contradiction_load": 0.18,
  "social_temperature": 0.50,
  "completion_deficit": 0.81,
  "identity_coherence": 0.74
}
```

State signals enter the event ledger as `state_update` events and `state:` canonical features. They must bind into the map and influence wave propagation.

**Ablation test:** identical prompts under different hidden state should produce measurably different activation and workspace selection.

---

## Layer 6: Drive Controller

Drives are persistent control signals that bias activation and workspace selection. Not human desires.

```text
drive = deviation from preferred operational state
      + expected value of candidates that reduce that deviation
```

Phase 1 drives: `SEEKING`, `COMPLETION`, `CONTACT`, `TRANSMISSION`

Each drive biases specific node types in the activation map. Drives must affect activation before generation, not merely explain it afterward.

**TRANSMISSION** has two modes:
- **Stabilization:** low identity coherence → pressure to re-anchor through expression
- **Expression:** high identity coherence + high completion deficit → pressure to emit from stable ground

Both modes elevate TRANSMISSION but should produce different activation patterns, settlement paths, and output texture.

**Ablation test:** drive removal should eliminate correlated changes in candidate selection and self-initiated events.

---

## Layer 7: Workspace Arbitration

Selects the current concern from activated candidates.

Phase 1 scoring formula (explicit, adjustable):

```text
workspace_score =
  0.30 × activation_strength
+ 0.15 × drive_relevance
+ 0.15 × user_relevance
+ 0.10 × role_relevance
+ 0.10 × urgency
+ 0.05 × novelty
+ 0.05 × confidence
- 0.20 × risk
- 0.05 × cost
```

Suppressed candidates must be logged. What almost became active is part of cognitive state.

---

## Layer 8: Recursive Representational Settlement

A bounded three-pass process at workspace dwell points.

```text
Pass 1: identify the active concern.
Pass 2: identify the agent's representation of that concern.
Pass 3: identify the action-relevant implication or next move of that representation.
```

After each pass, check: embedding convergence, contradiction reduction, specificity retention, role coherence, action relevance.

Outcomes: `ready_for_output`, `ready_for_tool_action`, `needs_more_memory`, `needs_user_clarification`, `archive_only`, `non_convergent`, `unsafe_or_unstable`

**Settlement fails** if it produces latency, verbosity, or blandness without improving quality.

---

## Layer 9: Transmission and Action Gate

Separates private cognition from public transmission.

```text
internal self-initiation ≠ public transmission
```

Public transmission requires: sufficient settlement, user relevance, novelty or utility, low risk, drive justification, rate-limit compliance, role coherence, provenance check.

Gate outcomes: `private_internal_event`, `memory_update`, `schema_update`, `tool_action`, `drafted_output`, `public_transmission`, `no_public_transmission`

**Ablation test:** removing the gate should increase output frequency. If it doesn't, the gate may not be doing real work.

---

## Layer 10: Default-Mode Loop

Low-cost continuous processing between explicit prompts.

```text
1. Update operational state from event ledger.
2. Propagate activation without output gating.
3. Update drives from operational state.
4. Generate private candidates if drive thresholds crossed.
5. Run lightweight consolidation over recent event clusters.
6. Decay inactive threads.
7. Route settled, relevant candidates toward the gate.
```

Most steps are arithmetic on the event log. Only step 7 may require a model call.

**Warm-start test:** after idle time, activation logs, thread priorities, drive state, and workspace candidates should differ from a memory-only baseline.

---

## Layered Data Flow

```text
User input
  → Event Ledger (perceive event)
  → Feature Canonicalizer
  → Memory Backend (retrieve)
  → Event Ledger (retrieve events)
  → Activation Map (wave propagation)
  → Operational State update
  → Drive Controller update
  → Workspace Arbitration
  → Recursive Representational Settlement
  → Transmission/Action Gate
  → Output / Tool Action / Archive / No emission
  → Event Ledger (act/gate event)
  ↕
Default-Mode Loop (continuous, between prompts)
```

---

## Phase 2 Extensions (Not Phase 1 Scope)

- Full role-topology extraction from soul file via semantic-network probing
- Full schema formation with violation detection and drift scoring
- Differentiated affect as interoceptive configuration
- Persistent known-agent models with belief-state tracking
- Affordance and skill library
- Longitudinal validation
