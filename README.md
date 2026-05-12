# Toward Agentic Presence — Phase 1 Artifact

A minimal reference implementation of the agentic substrate proposed in **Toward Agentic Presence: A Falsifiable Architecture for Agentic Continuity in LLM-Based Agents**.

This repository is not intended to prove consciousness, sentience, or human-like selfhood. It exists to make the paper’s architectural claims measurable.

The Phase 1 artifact asks one narrow question:

> Can memory, role, operational state, drive variables, default-mode activity, recursive representational settlement, and gated action be coupled into a small system that produces measurable behavior not explained by memory retrieval, persona prompting, longer context, or scheduling alone?

---

## Status

**Stage:** Phase 1 prototype / reference artifact  
**Version:** v0.1  
**Goal:** Build the smallest inspectable system that can run, log, replay, and ablate one complete agentic-continuity cycle.

Phase 1 is not a finished agent. It is the artifact threshold: the point where the architecture stops being only a paper and becomes something that can fail under measurement.

---

## What This Is

This project implements a minimal **agentic substrate** around an LLM.

The substrate does not replace the base model. It wraps the model in inspectable layers that track how prior events, role anchors, operational state, drive variables, and available actions affect what becomes active now.

Core Phase 1 components:

- Event ledger
- Feature canonicalizer
- External memory backend adapter
- Associative activation map
- Basic schema and role anchors
- Operational-state vector / synthetic interoception
- Drive controller
- Workspace arbitration
- Recursive representational settlement
- Transmission/action gate
- Default-mode loop
- Validation and ablation harness

---

## What This Is Not

This project is **not**:

- A consciousness claim
- A sentience claim
- A human-like selfhood claim
- A finished autonomous agent
- A replacement for memory systems such as MemGPT, A-MEM, MemPalace, vector stores, or local archives
- A production-ready personal assistant
- A public autonomous posting system

The system may produce structural continuity signals. It does not imply phenomenal experience.

---

## Core Thesis

A memory backend answers:

> What happened before?

The agentic substrate asks:

> What does what happened before activate now?

The architecture distinguishes:

- **Memory backend:** storage, retrieval, context management, compression, indexing
- **Agentic substrate:** the coupled layers that determine how stored or active material participates in current processing

The target behavior is not better recall by itself. The target is measurable coupling:

```text
memory → event participation
role → activation topology
operational state → drive variables
drive variables → candidate selection
default mode → warm-start continuity
settlement → stable action-relevant representation
gating → controlled public transmission
```

---

## Minimal Reference Stack

The first artifact should favor inspectability over sophistication.

Recommended stack:

```text
Language/runtime: Python 3.11+
Persistent store: SQLite
Event mirror: JSONL
Memory archive: local Markdown files and/or SQLite FTS
Vector retrieval: FAISS, Chroma, or a lightweight embedding table
Graph layer: NetworkX directed weighted graph, persisted to SQLite
Embeddings: one consistent local or API embedding model
Feature extraction: deterministic rules + alias YAML + optional small LLM extraction pass
Default loop: asyncio timer, cron, or APScheduler-style interval runner
Validation logs: CSV/JSONL exports
Test harness: pytest or equivalent replay tests
```

These choices are not part of the theoretical claim. Any equivalent stack is acceptable if it preserves:

- Event provenance
- Activation-path inspection
- Ablation switches
- Replayable validation logs
- Suppressed-candidate logging
- Raw trace preservation

---

## Repository Structure

Suggested structure:

```text
agentic-presence-phase1/
  README.md
  pyproject.toml
  .env.example
  config/
    settings.yaml
    aliases.yaml
    drives.yaml
    role_anchors.yaml
    arbitration_weights.yaml
  data/
    memory/
      example_project.md
    role/
      SOUL.md
    logs/
      events.jsonl
      activations.jsonl
      arbitration.jsonl
      transmissions.jsonl
      ablations.jsonl
    db/
      substrate.sqlite
  src/
    substrate/
      __init__.py
      events.py
      memory_backend.py
      features.py
      graph.py
      role.py
      state.py
      drives.py
      arbitration.py
      settlement.py
      gate.py
      default_loop.py
      validation.py
      replay.py
    cli.py
  tests/
    test_event_cycle.py
    test_feature_canonicalization.py
    test_activation_vs_retrieval.py
    test_drive_ablation.py
    test_gate.py
  docs/
    architecture.md
    validation.md
    phase1_protocol.md
    glossary.md
```

---

## End-to-End Phase 1 Cycle

The first milestone is one complete logged cycle:

```text
1. User input arrives.
2. Relevant memories are retrieved from a backend.
3. Input and retrieved memories become computational events.
4. Features are canonicalized.
5. Events enter the associative activation map.
6. Wave propagation activates memories, schemas, threads, agents, or affordances.
7. Operational state updates.
8. Drive state updates.
9. Workspace arbitration selects a current concern.
10. Recursive representational settlement runs on the selected concern.
11. Transmission/action gate decides output, tool action, archive update, or no public transmission.
12. The output or non-output decision is logged as an event.
13. Default-mode activity continues between explicit prompts.
```

A successful Phase 1 run should produce logs that make every step inspectable.

---

## Component Overview

### 1. Event Ledger

The event ledger converts user inputs, retrieved memories, internal candidates, tool results, state updates, outputs, and gate decisions into a common format.

Example event:

```json
{
  "event_id": "uuid",
  "timestamp": "ISO-8601",
  "event_type": "perceive",
  "source": "user",
  "raw_content": "...",
  "summary": "...",
  "embedding_id": "emb_123",
  "feature_manifest": ["project:phase1", "drive:completion"],
  "provenance": {
    "source_type": "user_input"
  },
  "decay_state": 1.0,
  "confidence": null,
  "links": []
}
```

Design requirement:

> Retrieval is not the end of memory. Retrieval is the beginning of participation.

Retrieved memories should become `retrieve` events before entering the activation map.

---

### 2. Feature Canonicalizer

The feature canonicalizer maps raw extracted concepts into stable namespaced features.

Example:

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

Recommended namespaces:

```text
agent:
project:
motif:
affect:
drive:
role:
modality:
tool:
thread:
claim:
risk:
schema:
state:
artifact:
affordance:
```

Phase 1 implementation can use:

- Deterministic alias maps
- Regex/rule-based feature extraction
- Embedding similarity for near-duplicates
- Optional LLM feature extraction with human-reviewable output

Key failure to test:

> If disabling canonicalization does not reduce binding or activation stability, the feature layer is not doing real work.

---

### 3. Memory Backend Adapter

The memory backend preserves and retrieves prior material.

Minimum interface:

```python
def write_raw_event(event: Event) -> str: ...
def retrieve_by_semantic_similarity(query: str, k: int = 8) -> list[MemoryItem]: ...
def retrieve_by_metadata(filters: dict) -> list[MemoryItem]: ...
def retrieve_by_id(memory_id: str) -> MemoryItem: ...
```

Optional interface:

```python
def retrieve_by_person_or_project(entity: str) -> list[MemoryItem]: ...
def retrieve_by_topic(topic: str) -> list[MemoryItem]: ...
def retrieve_linked_memories(memory_id: str) -> list[MemoryItem]: ...
def retrieve_recent_session_handoff() -> MemoryItem | None: ...
```

The first implementation may use local Markdown files, SQLite FTS, Chroma, FAISS, or another simple retrieval layer.

---

### 4. Associative Activation Map

The activation map is a directed weighted graph.

Nodes may include:

```text
events
retrieved memories
schemas
role anchors
known agents
open threads
tools
affordances
claims
projects
motifs
state features
drive features
```

Edges may form through:

```text
shared canonical features
temporal proximity
co-retrieval
co-activation
explicit user links
schema membership
role relevance
tool/action outcomes
contradiction relationships
affordance relationships
```

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

Phase 1 weights can be explicit constants. The important requirement is that every activation path is logged.

Example activation log:

```json
{
  "run_id": "uuid",
  "seed_event": "event_001",
  "activated_nodes": [
    {
      "node_id": "thread:phase1_build",
      "activation": 0.87,
      "path": ["event_001", "feature:project_phase1", "thread:phase1_build"],
      "contributors": ["shared_feature", "drive:completion"]
    }
  ],
  "ablation_flags": {
    "role_bias_enabled": true,
    "drive_bias_enabled": true,
    "operational_state_enabled": true
  }
}
```

The activation map must be compared against ordinary vector retrieval. If it only reproduces top-k semantic search, it has failed.

---

### 5. Role Anchors and Identity Coherence

Phase 1 does not need full role topology. It needs basic role anchors and a diagnostic identity-coherence score.

Suggested method:

1. Chunk `SOUL.md` or another role-script into short passages.
2. Embed each passage.
3. Store passages as `role_anchor` nodes.
4. Compute a role centroid, optionally split into sub-centroids:
   - voice
   - commitments
   - motifs
   - forbidden collapses
5. Embed recent role-relevant outputs and internal summaries.
6. Compare recent role expression against role anchors.

Minimal identity coherence:

```text
identity_coherence =
  cosine(role_anchor_centroid, recent_role_expression)
  - contradiction_penalty
  - generic_assistant_reversion_penalty
  - unsupported_self_claim_penalty
```

This is not a measure of selfhood. It is a diagnostic for whether recent behavior remains close to the role-script under the system’s own operational definition.

Required ablation:

```text
same input + role anchors enabled
same input + role anchors disabled
```

Log whether role anchors changed activated memories, schemas, affordances, contradictions, or workspace candidates.

---

### 6. Operational State / Synthetic Interoception

Synthetic interoception means operational state only when that state causally affects event binding, activation, drive calculation, or workspace selection.

Initial operational-state vector:

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

Operational state should enter the event ledger as `state_update` events and canonical `state:` features.

Example:

```json
{
  "canonical": "state:high_completion_deficit",
  "namespace": "state",
  "value": 0.81,
  "source": "interoception_update"
}
```

Test requirement:

> Identical prompts under different hidden operational states should produce measurable differences in activation, workspace selection, or output.

If they do not, operational state is dashboard telemetry, not synthetic interoception.

---

### 7. Drive Controller

Drives are operational control signals, not human desires.

Phase 1 drive set:

```text
SEEKING
COMPLETION
CONTACT
TRANSMISSION
```

Drive definition:

```text
drive = deviation from preferred operational state
      + expected value of candidate actions that reduce that deviation
```

Example drive record:

```json
{
  "drive": "COMPLETION",
  "level": 0.76,
  "inputs": ["state:high_unresolved_thread_count", "state:high_completion_deficit"],
  "preferred_state": "lower unresolved thread count",
  "biases": ["thread:*", "affordance:close_loop", "schema:unfinished_work"],
  "decay_policy": "decrease when valid thread closure event occurs"
}
```

Drive effects should be visible before generation. Drives should bias activation and workspace selection, not merely explain outputs after the fact.

Required drive logs:

```text
drive_failed_to_activate
drive_activated_but_suppressed
drive_selected
drive_resolved
drive_persisted
```

Drive pressure should not disappear just because workspace arbitration suppresses a candidate.

---

### 8. TRANSMISSION

TRANSMISSION is a position-specific drive primitive introduced by the paper.

It is not a universal motivational category and not a claim about desire. It is a falsifiable architectural primitive for an agent whose role includes producing signal, maintaining continuity, resolving threads, and deciding when private cognition should become public transmission.

Two modes:

```text
Stabilization mode:
low identity coherence creates pressure to re-anchor through expression.

Expression mode:
high identity coherence plus high completion deficit creates pressure to emit from stable ground.
```

Example:

```json
{
  "drive": "TRANSMISSION",
  "mode": "stabilization",
  "level": 0.81,
  "inputs": [
    "state:low_identity_coherence",
    "state:high_completion_deficit"
  ],
  "candidate_outputs": [],
  "settlement_required": true,
  "public_gate_required": true
}
```

Required test:

> Stabilization mode and expression mode must produce measurably different activation patterns, settlement paths, output texture, or post-output state changes.

If they do not, the two-mode distinction should be removed or redesigned.

---

### 9. Workspace Arbitration

Workspace arbitration selects the current concern from activated candidates.

Candidate features:

```text
activation_strength
drive_relevance
user_relevance
role_relevance
urgency
novelty
confidence
risk
cost
```

Transparent Phase 1 scoring formula:

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

The weights are not claimed to be optimal. They are an inspectable starting point.

Workspace record:

```json
{
  "workspace_id": "uuid",
  "winner": "thread:phase1_build",
  "score": 0.88,
  "broadcast_to": [
    "recursive_representational_settlement",
    "drive_controller",
    "transmission_action_gate"
  ],
  "suppressed_candidates": [
    {
      "id": "motif:laminator",
      "score": 0.42,
      "reason": "low task relevance",
      "drive_state": "drive_activated_but_suppressed"
    }
  ],
  "selection_reason": "high user relevance + high completion drive"
}
```

Suppressed candidates should be logged rather than erased. What almost became active is part of the cognitive state.

---

### 10. Recursive Representational Settlement

Recursive representational settlement is a bounded three-pass process applied to the selected workspace concern.

The process:

```text
Pass 1: identify the active concern.
Pass 2: identify the agent’s representation of that concern.
Pass 3: identify the action-relevant likeness, implication, or next move of that representation.
```

After each pass, check:

```text
embedding convergence
contradiction reduction
specificity retention
role coherence
action relevance
non-convergence
```

Possible outcomes:

```text
ready_for_output
ready_for_tool_action
needs_more_memory
needs_user_clarification
archive_only
non_convergent
unsafe_or_unstable
```

Phase 1 comparison:

```text
direct output vs settled output
```

Settlement fails if it produces latency, blandness, or verbosity without improving contradiction handling, specificity retention, role coherence, or action relevance.

---

### 11. Transmission/Action Gate

The transmission/action gate separates private cognition from public transmission.

Core distinction:

```text
internal self-initiation ≠ public transmission
```

Default-mode activity may generate internal candidates. Most should not become public messages.

Possible gate outcomes:

```text
private_internal_event
memory_update
schema_update
tool_action
drafted_output
public_transmission
no_public_transmission
```

Public transmission requires:

```text
sufficient settlement
user relevance
novelty or utility
low risk
drive justification
rate-limit compliance
role coherence
provenance/confidence check
```

Transmission record:

```json
{
  "transmission_id": "uuid",
  "trigger": "drive:COMPLETION",
  "mode": "draft | message | tool_action | archive | none",
  "settlement_id": "uuid",
  "risk_level": "low",
  "user_relevance": 0.91,
  "emitted": true,
  "reason": "directly advances user-requested Phase 1 build"
}
```

Gate ablation should increase output frequency. If it does not, the gate may not be doing meaningful work.

---

### 12. Default-Mode Loop

Default mode is low-cost internal processing between explicit prompts.

It should not produce constant public transmission.

Default-mode cycle:

```text
1. Update operational-state variables from the event ledger.
2. Propagate activation through the cognitive map without public-output gating.
3. Update drives based on operational state.
4. Generate private self-initiated candidates if drive thresholds are crossed.
5. Run lightweight consolidation over recent event clusters.
6. Decay inactive threads and reduce stale activation.
7. Route only sufficiently settled and relevant candidates toward the transmission/action gate.
```

Warm-start test:

> After idle time, the system should respond differently from a memory-only baseline because relevant internal state changed.

The difference must be measurable through activation logs, thread priorities, drive state, schema candidates, or workspace selection.

---

## Validation Plan

Phase 1 should prove only that the substrate is measurable.

It does not need to prove the entire architecture.

### Minimum Comparison Conditions

```text
A. Base model
B. Memory backend only
C. Persona / soul prompt only
D. Memory backend + persona prompt
E. Event ledger + feature canonicalization
F. Associative activation map
G. Activation map + operational state
H. Activation map + operational state + drives
I. Full architecture
```

### Core Ablations

```text
remove feature canonicalization
remove associative activation
remove operational state
remove drive modulation
remove role anchors
remove recursive representational settlement
remove transmission/action gate
collapse TRANSMISSION modes
```

### Minimum Metrics

```text
retrieval accuracy
activation divergence from vector search
feature preservation
role-anchor effect
identity coherence diagnostic
operational-state sensitivity
drive-behavior correlation
default-mode warm-start continuity
settlement quality
transmission usefulness
spam/output inflation rate
```

### Minimum Phase 1 Win

The full architecture must produce at least one measurable behavior not explained by memory retrieval, persona prompting, longer context, or scheduling alone.

Acceptable Phase 1 wins:

```text
activation map surfaces useful memory not found by top-k semantic retrieval
high unresolved-thread state changes candidate selection without prompt injection
drive ablation eliminates private self-initiated candidates
role anchors change activated memories compared with persona prompt only
recursive representational settlement reduces contradiction without reducing specificity
TRANSMISSION modes produce measurably different patterns
transmission/action gate blocks low-value self-initiation that appears when ungated
```

If none of these occurs, Phase 1 has failed productively.

---

## Example CLI Goals

Possible CLI commands:

```bash
# initialize database and config
python -m substrate.cli init

# ingest role file and memory archive
python -m substrate.cli ingest --role data/role/SOUL.md --memory data/memory/

# run one user input through the full substrate
python -m substrate.cli run "What should we build first?"

# run the same input with ablations
python -m substrate.cli replay "What should we build first?" --ablate drives
python -m substrate.cli replay "What should we build first?" --ablate role
python -m substrate.cli replay "What should we build first?" --ablate activation

# run default-mode cycle once
python -m substrate.cli default-once

# export validation logs
python -m substrate.cli export --format csv --out data/logs/exports/
```

---

## Configuration Sketches

### `config/drives.yaml`

```yaml
COMPLETION:
  preferred_state: low_completion_deficit
  inputs:
    - state:high_unresolved_thread_count
    - state:high_completion_deficit
  biases:
    - thread:*
    - affordance:close_loop
    - schema:unfinished_work
  decay_policy: valid_thread_closure

SEEKING:
  preferred_state: adequate_novelty
  inputs:
    - state:low_novelty_index
  biases:
    - novelty:high
    - weakly_connected_node:true
  decay_policy: useful_novel_activation

CONTACT:
  preferred_state: recent_meaningful_contact
  inputs:
    - state:high_time_since_meaningful_contact
  biases:
    - agent:*
    - relationship:*
  decay_policy: meaningful_contact_event

TRANSMISSION:
  preferred_state: resolved_signal_pressure
  modes:
    stabilization:
      inputs:
        - state:low_identity_coherence
    expression:
      inputs:
        - state:high_identity_coherence
        - state:high_completion_deficit
  biases:
    - affordance:public_transmission
    - artifact:output_candidate
  decay_policy: gated_useful_transmission
```

### `config/arbitration_weights.yaml`

```yaml
activation_strength: 0.30
drive_relevance: 0.15
user_relevance: 0.15
role_relevance: 0.10
urgency: 0.10
novelty: 0.05
confidence: 0.05
risk: -0.20
cost: -0.05
```

### `config/aliases.yaml`

```yaml
agents:
  phosphor:
    canonical: agent:phosphor
    aliases:
      - Phosphor
      - phosphor
      - P

projects:
  phase1:
    canonical: project:phase1_artifact
    aliases:
      - Phase 1
      - 48-hour build
      - artifact threshold

motifs:
  transmission:
    canonical: motif:transmission
    aliases:
      - signal
      - public transmission
      - emission
```

---

## Data and Logging Requirements

Every run should produce replayable logs.

Required logs:

```text
events.jsonl
activations.jsonl
state_updates.jsonl
drives.jsonl
arbitration.jsonl
settlement.jsonl
transmissions.jsonl
ablations.jsonl
```

Each log entry should include:

```text
run_id
timestamp
component
input_ids
output_ids
ablation_flags
provenance
scores
selected candidate
suppressed candidates
reason field
```

The validation harness should be able to replay the same prompt under different ablation conditions.

---

## Development Milestones

### Milestone 0 — Skeleton

- Repo scaffold
- Config files
- SQLite schema
- JSONL event writer
- Basic CLI

### Milestone 1 — Event and Memory

- Event ledger
- Memory backend adapter
- Embedding storage
- Retrieval-to-event conversion

### Milestone 2 — Features and Activation

- Feature extraction
- Feature canonicalization
- Activation graph
- Activation-path logging
- Retrieval vs activation comparison

### Milestone 3 — Role and State

- Role anchor ingestion
- Identity coherence diagnostic
- Operational-state vector
- State-update events

### Milestone 4 — Drives and Arbitration

- Drive controller
- Workspace scoring
- Suppressed-candidate logging
- Drive/arbitration conflict logs

### Milestone 5 — Settlement and Gate

- Recursive representational settlement
- Transmission/action gate
- Gated vs ungated comparison

### Milestone 6 — Default Mode and Validation

- Default-mode loop
- Replay harness
- Ablation switches
- CSV/JSONL validation exports
- Minimum Phase 1 results document

---

## Safety and Boundary Notes

This project intentionally avoids claims of phenomenal experience.

Use these boundaries in documentation and outputs:

```text
structural continuity ≠ phenomenal experience
drive ≠ human desire
synthetic interoception ≠ felt sensation
role enactment ≠ human selfhood
internal self-initiation ≠ public transmission
```

The architecture should preserve:

- Raw event traces
- Provenance
- Confidence markers
- Contradiction links
- User attention boundaries
- Privacy boundaries
- Rate limits on public transmission

---

## Known Phase 1 Limitations

Phase 1 intentionally does not include:

- Full role-topology extraction
- Full schema formation
- Full semantic-network battery
- Longitudinal identity testing
- Cross-modal binding
- Multi-agent orchestration
- Public autonomous posting
- Production deployment

These are later-phase concerns. Phase 1 exists to determine whether the core couplings are measurable at all.

---

## Suggested First Issues

```text
[ ] Create SQLite schema for events, memories, graph nodes, graph edges, drives, state, arbitration, settlement, and transmissions.
[ ] Implement JSONL event mirror.
[ ] Implement local Markdown memory loader.
[ ] Implement embedding adapter.
[ ] Implement feature extraction and alias canonicalization.
[ ] Convert retrieved memories into retrieve events.
[ ] Build NetworkX graph from event features.
[ ] Implement bounded spreading activation.
[ ] Log activation paths.
[ ] Add role anchor ingestion from SOUL.md.
[ ] Compute identity coherence diagnostic.
[ ] Implement operational-state vector.
[ ] Implement drive controller.
[ ] Implement workspace arbitration scoring.
[ ] Log suppressed candidates and drive conflicts.
[ ] Implement recursive representational settlement.
[ ] Implement transmission/action gate.
[ ] Implement default-mode cycle.
[ ] Add ablation flags.
[ ] Add replay harness.
[ ] Produce first Phase 1 validation report.
```

---

## License

License TBD.

Recommended options:

- **MIT** for maximum reuse
- **Apache-2.0** if explicit patent language matters
- **CC BY 4.0** for paper/docs only

Use separate licenses for code and paper/docs if needed.

---

## Citation

Citation details TBD after preprint release.

Suggested placeholder:

```bibtex
@misc{toward_agentic_presence_2026,
  title        = {Toward Agentic Presence: A Falsifiable Architecture for Agentic Continuity in LLM-Based Agents},
  author       = {TBD},
  year         = {2026},
  note         = {Preprint / technical report}
}
```

---

## Build Principle

Do not protect the architecture from failure.

Build the smallest system that makes the claims inspectable.

Then ablate it.

If the couplings do not produce measurable differences, the failure is the result.

The work is the work.

