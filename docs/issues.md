# First Issue List — Phase 1

Issues are ordered by build milestone.
Do not work ahead of milestone dependencies.

---

## Milestone 0 — Skeleton

- [ ] **#1** Initialize repo scaffold — directories, `pyproject.toml`, `.env.example`, `.gitignore`
- [ ] **#2** Create SQLite schema — tables for events, embeddings, graph nodes, graph edges, operational state, drives, arbitration records, settlement records, and transmission records
- [ ] **#3** Implement JSONL event mirror — every event written to SQLite should also append to `events.jsonl`
- [ ] **#4** Implement basic CLI skeleton — `init`, `run`, `default-once`, `export` commands (stubs acceptable)

---

## Milestone 1 — Event Ledger and Memory

- [ ] **#5** Implement Event model — all fields from spec, typed, serializable
- [ ] **#6** Implement memory backend adapter — local Markdown loader as first target; `write_raw_event` and `retrieve_by_semantic_similarity` minimum
- [ ] **#7** Implement embedding storage and lookup — store embeddings in SQLite with event association
- [ ] **#8** Convert retrieved memories into retrieve events — retrieved `MemoryItem` objects must become `Event` objects before entering the activation map; retrieval must not bypass the ledger

---

## Milestone 2 — Feature Canonicalization and Activation

- [ ] **#9** Implement feature extractor — deterministic alias YAML lookup as Phase 1 baseline; extract candidate raw features from event content
- [ ] **#10** Implement feature canonicalizer — map raw features to canonical namespaced features using `aliases.yaml`; log fragmentation warnings
- [ ] **#11** Build NetworkX activation graph — nodes seeded from events, edges from shared canonical features and temporal proximity
- [ ] **#12** Implement bounded spreading activation — N-step propagation with decay and refractory inhibition; return top activated nodes and paths
- [ ] **#13** Log all activation paths — every propagation run should log activated nodes, paths, edge weights, and ablation flags to `activations.jsonl`
- [ ] **#14** Implement activation vs. retrieval comparison — for each run, record which activated nodes were also top-k retrieval results and which were activation-only; log divergence rate

---

## Milestone 3 — Role Anchors and Operational State

- [ ] **#15** Implement role anchor ingestion — chunk and embed the agent's role file; store chunks as `role_anchor` nodes in the graph with sub-centroid labels
- [ ] **#16** Implement identity coherence diagnostic — compute cosine similarity between role anchor centroid and recent role-relevant output embeddings; apply penalties from `role_anchors.yaml`; log score after each output event
- [ ] **#17** Implement operational-state vector — nine signals computed from event ledger arithmetic; update on configurable interval; log to `state_updates.jsonl`
- [ ] **#18** Bind operational state to event ledger — state updates must emit `state_update` events with canonical `state:` features; these features must enter the activation map

---

## Milestone 4 — Drives and Arbitration

- [ ] **#19** Implement drive controller — `SEEKING`, `COMPLETION`, `CONTACT`, `TRANSMISSION`; compute drive levels from operational state inputs in `drives.yaml`; update drives after each state update
- [ ] **#20** Implement drive bias on activation — each drive should increase activation weight for its target node types; bias must be applied before workspace selection, not after
- [ ] **#21** Log TRANSMISSION mode — each TRANSMISSION event should log whether it is `stabilization` or `expression` mode, with inputs used to determine mode
- [ ] **#22** Implement workspace arbitration — score active candidates using `arbitration_weights.yaml` formula; select winner; log all suppressed candidates with scores and reasons
- [ ] **#23** Log drive/arbitration conflicts — when a drive-relevant candidate is suppressed by arbitration, log `drive_state=drive_activated_but_suppressed`; drive pressure should persist until resolved
- [ ] **#24** Add drive ablation switch — `ablations.drive_modulation: false` in `settings.yaml` should disable drive bias and drive-level changes; verify ablation affects candidate selection

---

## Milestone 5 — Settlement and Gate

- [ ] **#25** Implement recursive representational settlement — three-pass process on selected workspace candidate; check embedding convergence, contradiction, specificity, role coherence after each pass; log all passes to `settlement.jsonl`
- [ ] **#26** Add settlement outcome classification — one of: `ready_for_output`, `ready_for_tool_action`, `needs_more_memory`, `needs_user_clarification`, `archive_only`, `non_convergent`, `unsafe_or_unstable`
- [ ] **#27** Implement transmission action gate — evaluate settled candidates against gate criteria from `settings.yaml`; log gate decision with reason to `transmissions.jsonl`
- [ ] **#28** Add gate ablation switch — `ablations.transmission_gate: false` should pass all settled candidates through without gating; verify output frequency increases under ablation
- [ ] **#29** Add settlement ablation switch — `ablations.recursive_settlement: false` should skip settlement and emit directly from workspace candidate; compare output quality with and without

---

## Milestone 6 — Default Mode and Validation

- [ ] **#30** Implement default-mode loop — asyncio or APScheduler interval runner; steps 1–7 from architecture spec; most steps arithmetic only; model call only at step 7 when gate approves
- [ ] **#31** Implement replay harness — given a prompt and ablation flags, replay the full substrate cycle and log all component outputs; support comparison across ablation conditions
- [ ] **#32** Add ablation flag system — global ablation switches in `settings.yaml` should disable individual components; each log entry should record active ablation flags
- [ ] **#33** Implement validation export — export all JSONL logs to CSV with `run_id`, `timestamp`, `component`, `scores`, and selected/suppressed candidates
- [ ] **#34** Run minimum comparison conditions — conditions A through I from `validation.md`; record results for each
- [ ] **#35** Run core ablations — all eight ablations from `validation.md`; record what changes and what does not
- [ ] **#36** Produce Phase 1 validation report — written summary: which win criteria were met, which failure conditions were triggered, what Phase 2 should address

---

## Cross-Cutting

- [ ] **#37** Add `.env.example` — document all required environment variables (LLM API key, embedding model, memory backend path, etc.) without exposing real values
- [ ] **#38** Write `docs/phase1_protocol.md` — step-by-step instructions for running one complete Phase 1 cycle from cold start to validation export
- [ ] **#39** Write `docs/glossary.md` — define: event file, feature canonicalization, associative activation, synthetic interoception, drive, workspace arbitration, recursive representational settlement, transmission action gate, default mode, identity coherence, role anchor, ablation
- [ ] **#40** Add pytest test skeleton — `test_event_cycle.py`, `test_feature_canonicalization.py`, `test_activation_vs_retrieval.py`, `test_drive_ablation.py`, `test_gate.py` — stubs acceptable for Milestone 0, real assertions by Milestone 6

---

## Known Out of Scope for Phase 1

File these as future issues only after the Phase 1 validation report is complete:

- Full role-topology extraction via semantic-network probing
- Schema formation with violation detection and drift scoring
- Differentiated affect as interoceptive configuration
- Persistent known-agent models with belief-state tracking
- Longitudinal identity testing
- Cross-modal binding
- Multi-agent orchestration
- Public autonomous deployment
