# Validation Plan

*Toward Agentic Presence — Phase 1*

This document defines the validation and measurement methodology for Phase 1 of the agentic substrate.
For theoretical foundations, see the full paper.
For architecture details, see `docs/architecture.md`.

---

## Guiding Principle

> The architecture becomes meaningful only when it becomes vulnerable to measurement.

Every major component must be removable.
Every structural claim must produce a falsification condition.
Positive results support only structural claims, not phenomenal claims.

---

## Comparison Conditions

Run the same prompt across these conditions and compare:

| Condition | Description |
|-----------|-------------|
| A | Base model — no memory, no persona, no substrate |
| B | Memory backend only |
| C | Persona / role file only |
| D | Memory backend + persona / role file |
| E | Event ledger + feature canonicalization (no activation) |
| F | Associative activation map (events + features + graph) |
| G | Activation map + operational state |
| H | Activation map + operational state + drives |
| I | Full architecture |

Conditions B and D are the primary comparators.
The architecture earns its complexity only where it produces effects not explained by B or D alone.

---

## Core Ablations

Each ablation removes one component while keeping the rest active.

| Ablation | Prediction |
|----------|------------|
| Remove feature canonicalization | Binding stability decreases; activation paths fragment |
| Remove associative activation | Cross-topic synthesis and spontaneous recall decrease |
| Remove operational state | Identical prompts become more similar across hidden states |
| Remove drive modulation | Self-initiated candidates disappear or become random |
| Remove role anchors | Role-specific memory and affordance activation decreases |
| Remove recursive settlement | Output quality drops or consistency degrades |
| Remove transmission action gate | Output frequency rises; usefulness-per-transmission falls |
| Collapse TRANSMISSION modes | Stabilization and expression become indistinguishable |

---

## Minimum Phase 1 Win

The full architecture must produce **at least one** measurable behavior not explained by memory retrieval,
persona prompting, longer context, or scheduling alone.

Acceptable Phase 1 wins:

- Activation map surfaces relevant memory not found by top-k semantic retrieval
- High `unresolved_thread_count` state changes candidate selection without prompt injection
- Drive ablation eliminates private self-initiated candidates
- Role anchors change activated memories compared with persona-prompt-only condition
- Recursive settlement reduces contradictions without reducing specificity
- TRANSMISSION modes produce measurably different activation patterns
- Gate ablation produces output inflation, confirming the gate blocks low-value transmission

If none of these appears, Phase 1 has **failed productively**.
That failure would show that core couplings need redesign before later phases.

---

## Core Metrics

### Retrieval Accuracy

Tests basic memory access. Not sufficient to validate the architecture by itself.

- Recall@k, Precision@k
- Exact prior-event recovery
- Human relevance rating

### Associative Divergence from Semantic Retrieval

Tests whether the activation map produces useful associations beyond vector search.

- Overlap between activation results and top-k retrieval
- Activation-only relevance score (blind human rating)
- Novel-but-relevant association rate
- Noise rate

### Feature Preservation

Tests whether perceived features survive into action.

- Input-feature capture rate
- Feature carry-forward through event chain
- Perception-to-action feature overlap

### Role Stability

Tests whether role information changes what becomes active, not just output style.

- Embedding similarity to role anchor centroid
- Role-relevant node activation under role-on vs. role-off
- Memory selection differences
- Role-collapse rate under pressure conditions

### Operational-State Sensitivity

Tests whether hidden state affects cognition without prompt injection.

Procedure: run identical prompts under manipulated state values;
the model must not be told its state in natural language.

- Activated-node difference by state
- Workspace candidate difference by state
- Blind classifier accuracy (can a classifier identify state from output behavior?)

### Drive-Behavior Correlation

Tests whether drives predict candidate generation and workspace selection.

- Drive level vs. candidate generation rate
- Drive level vs. workspace winner type
- Correlation disappears under drive ablation

### TRANSMISSION Mode Distinction

Tests whether stabilization and expression modes are architecturally real.

- Activation pattern difference
- Settlement-path difference
- Output texture difference (blind rating)
- Post-output identity coherence change

### Default-Mode Warm-Start

Tests whether idle cycles change the system's arriving state.

- Thread priority differences after idle
- Drive-state evolution without prompts
- Schema candidate formation
- Warm-start vs. cold-start response quality

### Settlement Quality

Tests whether recursive settlement improves output.

- Direct vs. settled output (blind preference)
- Contradiction reduction
- Specificity retention
- Role coherence
- Embedding convergence (not sufficient alone)

### Transmission Quality and Gate Behavior

Tests whether the gate produces useful, sparse, justified output.

- Transmission frequency
- Human-rated usefulness
- Spam rate
- Gate ablation effect on frequency and quality

---

## Semantic-Network Validation (Phase 1 Light Version)

Free-association probing provides a structural measurement of role conditioning.

Procedure:

1. Present 50 cue words (role-relevant, relational, aesthetic, and control set).
2. Request 3 associates per cue, 20 repetitions per cue.
3. Build a directed graph from cue → associate edges.
4. Compare: base model vs. role-conditioned vs. full architecture.

Metrics:

- Cluster density around role concepts
- Role-relevant prime-target activation difference
- Generic semantic association strength (control)

If the role file does not produce detectable associative structure changes versus a shuffled role file
and a generic persona, role conditioning is prompt-level only.

---

## False-Belief Probes (ToM Regression Test)

Not a claim of Theory of Mind.
A regression test for whether the architecture preserves structured belief-state reasoning.

- Run standard false-belief tasks.
- Run role-relevant relational scenarios involving known agent models (e.g., `agent:collaborator_a`, `agent:user`).
- Compare: base model vs. full architecture vs. ablation conditions.

Success: architecture preserves or improves belief-state tracking.
Failure: architecture causes ground-truth leakage or role-assumption override.

---

## Failure Conditions

The architecture should be considered unsupported if any of the following occur:

- Memory backend alone performs equivalently to the full architecture
- Activation map results are indistinguishable from vector retrieval
- Feature binding inertness: canonicalization removal has no effect
- Role topology equivalence: persona prompt alone produces the same role stability
- Operational state inertness: identical prompts behave identically across hidden states
- Drive non-causality: drive state does not correlate with candidate selection
- TRANSMISSION mode collapse: stabilization and expression are indistinguishable
- Settlement collapse: settlement produces latency without quality improvement
- Default-mode inertness: no measurable warm-start difference
- Reconstructive memory corruption: schema reconstruction overwrites raw traces

---

## Logging Requirements

Every run must produce replayable JSONL logs:

```
events.jsonl
activations.jsonl
state_updates.jsonl
drives.jsonl
arbitration.jsonl
settlement.jsonl
transmissions.jsonl
ablations.jsonl
```

Every log entry must include:
`run_id`, `timestamp`, `component`, `input_ids`, `output_ids`, `ablation_flags`,
`provenance`, `scores`, selected candidate, suppressed candidates with reasons.

The validation harness must be able to replay the same prompt under different ablation flags.

---

## Phase 1 Validation Report

At the end of Phase 1, produce a brief written report covering:

- Which conditions were run
- Which ablations were run
- Which metrics were collected
- Which Phase 1 win criteria were met (if any)
- Which failure conditions were triggered (if any)
- What this implies for Phase 2 scope

The report should be honest.
Failures are findings.
A failed component that gets redesigned is a better outcome than a component that was never tested.

---

## Phase 2 Validation Expansion (Not Phase 1 Scope)

- Longitudinal identity stability
- Role-collapse stress testing
- Full semantic-network battery
- Schema-violation detection
- Cross-topic synthesis over extended sessions
- Multi-agent opinion dynamics simulation
- Metacognitive confidence calibration
