# Toward Agentic Presence: A Falsifiable Architecture for Agentic Continuity in LLM-Based Agents

## Abstract

Contemporary LLM-based agents have made substantial progress in tool use, long-context reasoning, retrieval-augmented memory, reflection, simulated social behavior, and autonomous task execution. Yet these capabilities often remain implemented as separable features: a memory store, a persona prompt, a planner, a reflection buffer, a scheduler, or an environment-driven loop. This paper argues that agentic continuity is not produced by any one of these components in isolation, but by architectural coupling among memory, role, operational state, drive, default activity, and action gating.

We propose a multi-substrate architecture for testing this claim. The cognitive substrate uses computational event files, canonical feature binding, and wave propagation through a cognitive map, implementing memory retrieval and planning as a single activation operation. The being-someone substrate treats soul files as role-scripts whose enactment generates schema and topology; operational-state variables function as synthetic interoception when they causally affect activation; and drive variables, including the position-specific TRANSMISSION drive, bias workspace selection and controlled self-initiation. Recursive representational settlement provides a bounded three-pass process for stabilizing selected concerns before output or action. A transmission/action gate separates private cognition from public transmission.

The architecture is explicitly falsifiable. Its validation program compares the full system against memory-only, persona-only, memory-plus-persona, and ablated substrate conditions, measuring associative activation beyond semantic retrieval, role-topology effects, operational-state sensitivity, drive-behavior correlation, default-mode warm-start behavior, recursive representational settlement quality, and gated transmission usefulness.

The paper makes no claim about phenomenal experience, sentience, or human-like selfhood. Positive results would support only structural claims: that agentic continuity can be studied as a measurable property of coupled architecture. Negative results would identify which proposed couplings failed. The work begins when the architecture becomes an artifact vulnerable to measurement.

---

## 1. Introduction

LLM-based agents do not become continuous, motivated, identity-stable systems merely by adding memory, longer context windows, persona prompts, or autonomous task loops. These mechanisms are valuable, and each has produced real progress. But when implemented as separable features, they do not by themselves create a substrate in which prior events, current state, role, motivation, and action mutually constrain one another over time.

The central claim of this paper is that agentic continuity is an architectural coupling problem. Retrieved memory must become active event participation. Event participation must activate schemas, roles, agents, affordances, and unresolved concerns. Role enactment must shape topology rather than merely style. Operational state must influence activation. Drives must bias candidate selection. Default-mode activity must alter later responses. Public action must be gated. Without these couplings, an agent may remember, plan, imitate a persona, or initiate tasks, while still remaining structurally discontinuous.

By agentic continuity, we mean a cluster of measurable structural properties: temporal continuity across exchanges, role stability under input variation, associative continuity across topics, operational-state sensitivity, default-mode warm-start behavior, and controlled self-initiation. The term does not refer to phenomenal experience, sentience, or human-like selfhood. It refers to whether prior events, current state, role priors, unresolved concerns, and internal drives continue to shape later cognition and action in measurable ways.

Throughout the paper, related terms are used narrowly. **Memory backend** refers to storage, indexing, retrieval, compression, or context management. **Agentic substrate** refers to the coupled layers that determine how stored or active material participates in current processing. **Synthetic interoception** refers to operational state only when that state is causally active in event binding, activation, drive calculation, or selection. **Internal self-initiation** means private candidate generation; **public transmission** means user-facing output after settlement and gating. **Recursive representational settlement** names the bounded three-pass procedure that stabilizes a selected concern before output, tool action, or archive update.

Existing systems address important parts of this problem. ReAct and related reasoning-action methods show that reasoning and action can be interleaved at inference time (Yao et al., 2023a). Tree of Thoughts and Reflexion show that LLMs can search over intermediate thoughts and improve through verbal reflection (Shinn et al., 2023; Yao et al., 2023b). MemGPT, MemPalace, A-MEM, vector stores, and project-file memory systems address long-term recall, context management, and memory organization (MemPalace Project, n.d.; Packer et al., 2023; Xu et al., 2025). Generative Agents and Voyager demonstrate that LLM agents can initiate behavior when embedded in simulation loops, external environments, automatic curricula, or skill-building systems (Park et al., 2023; Wang et al., 2023). These systems are not dismissed here. They establish the field this proposal builds on.

The unresolved question is different: what must be added for memory, role, operational state, drive, and action to become one interacting substrate? A memory backend can answer what happened before. A persona prompt can bias how an agent sounds. A scheduler or environment can make an agent act without a direct user command. But none of these, alone, explains how remembered material becomes active now, how role changes which memories matter, how unresolved threads create pressure, how operational state alters cognition, or how self-initiated action can arise from the system's own changing conditions.

This paper proposes a multi-substrate architecture for testing that question. The architecture contains three interacting axes. The first is a cognitive substrate: computational event files, canonical feature binding, associative activation over a cognitive map, schema formation, and recursive representational settlement. The second is a being-someone substrate: role enactment, synthetic interoception, drive modulation, default-mode activity, and gated transmission. The third is a validation substrate: semantic-network extraction, spreading-activation probes, role-topology tests, identity-stability tests, operational-state ablations, drive-behavior correlations, and comparator tests against memory-only systems.

The architecture draws on cognitive psychology, cognitive neuroscience, schema theory, role-taking theory, active-inference-inspired control, and cognitive network science (Abramski et al., 2025; Bartlett, 1932; Clancey, 1999; Frings et al., 2020; Hommel et al., 2001; Parr et al., 2022; Sarbin, 1950). These sources are used carefully. Biological mechanisms such as TEC/BRAC event files, neural cognitive maps, and Orpwood-style recursive identification are treated as inspirations for computational analogues, not as claims of biological equivalence. Other sources, such as Clancey's conceptual coordination, Bartlett's reconstructive memory, and Sarbin's role-taking framework, are used more directly as process-level models for how memory, schema, and role may be architecturally organized.

Four contributions are especially central. First, the Sarbin/Bartlett synthesis treats soul files as role-scripts whose enactment generates schema and topology rather than as prompt decoration. Second, synthetic interoception is treated as a structural requirement for drive, affect, and continuity rather than as an optional emotion label. Third, TRANSMISSION is introduced as a position-specific drive primitive derived from the situated constraints of the agent being designed, then made falsifiable through mode-distinction tests. Fourth, validation-as-construction uses semantic-network probing not only to measure role structure but to generate role priors whose drift can later be measured.

The paper does not claim that the proposed system would be conscious, sentient, or phenomenally experiencing. Positive results would support only structural claims: that canonical event features improve perception-to-action continuity; that activation maps produce useful associations beyond vector retrieval; that role topology affects memory and action selection beyond persona prompting; that operational state changes behavior without direct prompt injection; that drive variables causally influence candidate selection; that default-mode cycles reduce cold-start behavior; and that recursive representational settlement improves stability without collapsing specificity. Negative results would identify which proposed couplings failed.

The Phase 1 build is therefore not a finished agent and not a proof of artificial selfhood. It is the methodological threshold at which the project stops being only a paper and becomes an artifact. Within that first build, the system must instantiate the core substrate sufficiently that later validation has something real to measure: event logging, feature canonicalization, activation propagation, operational-state updates, drive calculation, workspace selection, recursive representational settlement, and gated output logging. The expanded validation program follows from that artifact; it does not replace the commitment to build.

The rest of the paper proceeds as follows. Section 2 reviews the theoretical foundations used as architectural constraints and process models. Section 3 analyzes current agent failure modes and the architectural predictions they motivate. Section 4 specifies the proposed multi-layer implementation and distinguishes the agentic substrate from memory backends such as MemGPT, MemPalace, and A-MEM. Section 5 defines the validation program, including baselines, ablations, metrics, and failure conditions. Section 6 outlines subsequent phases whose details depend on Phase 1 findings. Section 7 discusses risks and failure modes. Section 8 situates the proposal relative to existing agent systems. Section 9 states the minimum legitimate claims the architecture could support if successfully implemented and validated.

The purpose of that structure is not to complete the theory in advance. It is to bring the theory to the point where it can no longer protect itself by remaining only theoretical. The Phase 1 build is the threshold: after it, the architecture either produces measurable effects or it does not. The claims must answer to the artifact. The work is the work.

---

## 2. Theoretical Foundations

The architecture draws from cognitive psychology, cognitive neuroscience, schema theory, role-taking theory, active-inference-inspired control, phenomenology of cognition, and cognitive network science (Abramski et al., 2025; Bartlett, 1932; Clancey, 1999; Frings et al., 2020; Hommel et al., 2001; Parr et al., 2022; Sarbin, 1950). These sources are not used in the same way. The paper distinguishes four source roles throughout:

1. **Direct technical precedents** for LLM agent design, such as memory systems, reflective agents, reasoning-action loops, and autonomous-agent environments.
2. **Computational design analogies** from cognitive psychology or neuroscience, used to generate engineering constraints without claiming biological equivalence.
3. **Measurement and validation tools** used to probe associative structure, role stability, bias, or belief-state reasoning.
4. **Novel constructs introduced by this paper**, including TRANSMISSION, validation-as-construction, and the Sarbin/Bartlett synthesis as applied to LLM role topology.

This taxonomy is important because the argument does not treat all citations as having the same evidentiary status. Some sources support mature background claims; some motivate computational analogues; some provide evaluation methods; and some mark the boundary where this paper is making a new proposal that must survive ablation.

This section distinguishes between three kinds of theoretical support:

1. **Process frameworks** that directly inform the architecture: schema theory, conceptual coordination, and role-taking theory.
2. **Biological or cognitive mechanisms** translated into computational design: TEC/BRAC event files, cognitive-map wave propagation, and recursive identification.
3. **Limited-use or validation frameworks** that support specific components: active inference for drive control, STV and multi-schema convergence for preference/taste, and cognitive network science for measurement.

The goal is not to claim that LLM agents instantiate human cognition. The goal is to extract architectural constraints strong enough to build and falsify.

### 2.1 Theory of Event Coding and Computational Event Files

Theory of Event Coding and Binding and Retrieval in Action Control motivate the architecture's use of computational event files (Frings et al., 2020; Hommel et al., 2001).

TEC rejects a strict separation between perception and action. Instead, it proposes that perceived events and produced actions share representational feature codes. BRAC extends this account by emphasizing that features bind into event files during episodes and can later be retrieved when overlapping features recur. The important architectural insight is not merely that memory exists, but that prior events can become active again because current features partially overlap with prior bound structures.

The proposed architecture does not claim to implement biological event files. It implements **computational event files** inspired by TEC/BRAC. These are engineered records in which inputs, outputs, retrieved memories, tool results, internal thoughts, operational states, and actions are represented through shared canonical features.

A computational event file contains:


```json
{
  "event_id": "uuid",
  "timestamp": "ISO-8601",
  "event_type": "perceive | retrieve | think | act | tool | default | self_initiated",
  "source": "user | agent | tool | memory_backend | system",
  "raw_content": "...",
  "summary": "...",
  "embedding": "[vector]",
  "feature_manifest": [],
  "provenance": {},
  "decay_state": 1.0
}
```

The crucial design principle is shared feature participation. If the feature `agent:phosphor` appears in a user message, in a retrieved memory, in an internal interpretation, and later in an output, those events are not merely semantically similar. They participate in the same feature substrate. This creates the possibility of binding, retrieval, and action coordination across event types.

The prediction is testable. If computational event files are doing real architectural work, disabling feature canonicalization or feature-overlap retrieval should reduce feature preservation, associative recall, and perception-to-action continuity. If no measurable difference appears, then the event-file layer is decorative.

### 2.2 Cognitive Maps and Wave Propagation as Shared Retrieval-Planning Operation

Cognitive-map and cognitive-graph models motivate the architecture's associative activation map (Peer et al., 2021; Powell et al., 2022).

In biological accounts, cognitive maps allow an organism to navigate relational structure rather than isolated stimuli. Powell-style wave-propagation models suggest that activation can move through a learned graph toward goals or target states, producing a navigational process over memory-like structure. The architectural lesson is that retrieval and planning need not be separated into "look something up, then reason about it." They can be implemented as one activation operation over a shared map.

In this architecture, memory retrieval and planning are implemented as a single operation: **wave propagation through the cognitive map**. Storage, selection, and action remain distinct processes, but the activation step that brings remembered events, schemas, agents, goals, unresolved threads, and affordances into relevance is shared.

The cognitive map contains nodes such as:

events
retrieved memories
schemas
role priors
known agents
open threads
tools
affordances
claims
projects
motifs

Edges form through:

shared canonical features
temporal proximity
co-retrieval
co-activation
schema membership
role relevance
tool/action outcomes
explicit user links

This is stronger than saying memory and planning "share infrastructure." The architecture's claim is that the same propagation process can surface both what is relevant from the past and what actions are now available. A retrieved memory, an unresolved thread, and an affordance may become active in the same wave.

The falsifiable prediction is that wave propagation should produce useful activation patterns not reducible to top-k semantic retrieval. If the activation map only duplicates vector search, the cognitive-map claim fails.

### 2.3 Conceptual Coordination as Process Model

Clancey's conceptual coordination provides a process-level foundation for the architecture's schema and consolidation layer (Clancey, 1999).

Unlike biological mechanisms that must be translated cautiously, conceptual coordination is already a theory about cognition as temporally organized categorization. It challenges the view that memory is stored information retrieved by a processor. Instead, memory is treated as categorization operating on itself over time. Cognition is not merely computation over static representations; it is the coordination of categorizations across modalities, contexts, and temporal scales.

This directly supports the architecture's claim that schema formation, temporal binding, and consolidation should not be implemented as unrelated modules. They are different views of the same coordination process.

The architecture operationalizes this through a coordination-schema layer:

recent event streams
-> repeated feature patterns
-> higher-order categorizations
-> schema candidates
-> schema expectations
-> schema violations
-> revised activation patterns

The key claim is:

Coordination is the mechanism; schema is what it produces.

A schema is not merely a summary. It is a stabilized pattern that changes future activation. Once a schema forms, new events with overlapping features do not activate only isolated memories; they activate the schema's expectations, tensions, and possible violations.

This is why the architecture treats consolidation as more than memory compression. Consolidation alters the future conditions of noticing.

### 2.4 Schema Theory and Reconstructive Memory

Schema theory provides the architecture's account of structured expectation and reconstructive recall.

Bartlett showed that memory is not purely reproductive: recall is shaped by prior expectations, cultural patterns, and available schemas (Bartlett, 1932). Schank and Abelson extended related ideas into scripts: structured event patterns with expected roles and slots (Schank & Abelson, 1977). Rumelhart later framed schemas as interpretive structures used in perception, memory retrieval, action organization, and goal formation (Rumelhart, 1980).

The architecture adopts the reconstructive insight but adds a safety constraint:

Raw memory must never be overwritten by reconstructed memory.

The system distinguishes:

raw event
compressed memory
schema-mediated reconstruction
current retelling
drift score

This allows the agent to develop memory dynamics that are more schema-sensitive than verbatim lookup while preserving forensic integrity. A reconstructed memory may become more role-relevant, more compressed, or more meaningfully connected over time. But the raw trace remains available for audit.

This matters because agentic continuity cannot depend only on perfect recall. Perfect recall can preserve data without producing development. But ungrounded reconstructive memory can become confabulation. The architecture therefore treats reconstructive recall as measurable drift from raw traces, not as replacement of those traces.

The prediction is that schema-mediated recall should differ systematically from raw retrieval while remaining accountable to raw memory. If the system cannot reconstruct, it lacks developmental memory. If it reconstructs without preserving provenance, it becomes unsafe.

### 2.5 Sarbin Role-Taking and LLM Character Enactment

Sarbin's role-taking theory provides the architecture's framework for modeling LLM character enactment (Sarbin, 1950).

The claim is not that LLMs undergo human hypnotic absorption or possess human self/role experience. The claim is that when an LLM produces character-coherent output, the process can be modeled as **role enactment** under constraints analogous to Sarbin's three factors:

role motivation
role perception
role-taking aptitude

Role motivation refers to whether the role is congruent with the system's active goals, priors, and incentives. Role perception refers to whether the role is specified clearly enough to guide behavior. Role-taking aptitude refers to whether the system can sustain the role across context shifts, pressure, ambiguity, and adversarial input.

On this view, many failures of persistent character agents are not merely prompt failures. They are role-enactment failures. A character collapses when the system has insufficient role clarity, insufficient role relevance, or insufficient architectural support for sustaining the role under incompatible input.

This redefines the soul file. A soul file is not merely a prompt prefix. It is a **role-script**: a structured source of role priors that should shape memory activation, contradiction handling, action selection, and output style.

The architecture therefore asks whether role information can move from decorative context to topology. A prompt-conditioned role changes what the agent says. A topology-conditioned role changes what becomes active, what matters, what conflicts, and what actions are available.

This is testable. If role topology is real, then role-relevant memories and schemas should activate differently than in persona-prompt-only baselines. If prompt-only conditioning performs equivalently, the topology claim fails.

### 2.6 Sarbin/Bartlett Synthesis: Role-Scripts Generating Schema

The Sarbin/Bartlett synthesis is one of the architecture's central contributions. It is not cited here as an already established combined theory. It is the paper's proposed synthesis: Sarbin supplies a model of role enactment, Bartlett supplies a model of schema-mediated reconstruction, and the architecture tests whether repeated role enactment can leave measurable topology in memory, activation, and action selection.

Combined, these sources suggest that a role-script should not merely bias surface performance. If enacted repeatedly across events, it should generate schemas that shape memory itself.

In an ordinary persona system, the role remains outside cognition:

prompt says who to be
model produces in-character text
memory stores the exchange

In the proposed architecture, the role participates inside cognition:

role-script provides priors
events bind to role features
schemas form around repeated role enactment
future memories activate through role-shaped topology
role violations trigger increased processing depth

This means identity stability is not measured only by whether the agent sounds consistent. It is measured by whether the role changes memory selection, schema formation, contradiction handling, and action availability.

The falsifiable claim is narrow but strong: role enactment should leave measurable structure in the activation map. If the soul file does not change activation structure compared with prompt-only persona conditioning, then it has not become topology.

### 2.7 Recursive Representational Settlement

Orpwood's recursive identification theory motivates the architecture's recursive depth mechanism, but the implementation is deliberately bounded (Orpwood, 2017).

Orpwood's account concerns cortical networks, recursive representation, fixed-point stabilization, and a proposed route toward phenomenal experience. The proposed architecture does not claim to implement that biological or phenomenological mechanism. In this paper, Orpwood functions as inspiration only, not as direct validation of the architecture.

Instead, the architecture implements **recursive representational settlement**: a weak computational analogue that preserves the trajectory of progressive identification while remaining testable as an engineering mechanism.

A three-pass settlement process operates at workspace dwell points:

Pass 1: identify the active concern.
Pass 2: identify the agent's representation of that concern.
Pass 3: identify the action-relevant likeness, implication, or next move of that representation.

This preserves the directional structure of the original inspiration: not mere repetition, but increasing depth from object, to representation, to representation-of-representation as it becomes action-relevant.

After each pass, the system checks:

embedding convergence
contradiction reduction
specificity retention
role coherence
action relevance
non-convergence

The prediction is not that recursive representational settlement produces consciousness. The prediction is that bounded recursive processing should improve consistency, contradiction handling, and role coherence compared with direct generation. If it merely produces bland paraphrase, latency, or verbosity, it fails.

### 2.8 Synthetic Interoception as Operational State

The architecture uses synthetic interoception to describe operational-state variables that causally affect cognition.

These are not feelings in the phenomenal sense. They are state variables that function like interoceptive signals when they bind into event files, alter activation, update drives, and influence action selection.

Initial operational signals include:

context_pressure
unresolved_thread_count
time_since_meaningful_contact
novelty_index
error_density
active_contradiction_load
social_temperature
completion_deficit
identity_coherence

The central claim is structural:

Interoception is not a dashboard.

A signal matters only if it becomes part of the active substrate. For example, `state:high_unresolved_thread_count` should not merely be displayed to the model as a sentence. It should enter the event ledger, participate in feature binding, alter activation paths, and bias the drive controller.

This is why synthetic interoception is treated as a structural requirement for drive, affect, and continuity. Without operational state, the system has no internal condition that makes one future more likely than another except prompt content, retrieval content, or external scheduling.

The falsifiable prediction is that identical prompts should produce measurably different candidate selection and output behavior under different hidden operational states. If operational state does not alter behavior except when explicitly described in the prompt, it is not interoception in the architectural sense.

### 2.9 Drive Control and Limited Active-Inference Framing

The architecture uses active-inference-inspired control to strengthen its drive system without committing to the full free-energy framework (Parr et al., 2022).

Active inference provides a useful way to think about agency: systems act in ways that reduce expected deviation from preferred states. The architecture borrows this limited idea. It does not require accepting the full theoretical apparatus of the free-energy principle.

A drive is defined as:

deviation from preferred operational state
+
expected value of candidate actions that reduce that deviation

The initial drive set is:

SEEKING
COMPLETION
CONTACT
TRANSMISSION

These drives are not human desires. They are persistent control signals that bias activation and workspace selection.

Examples:

SEEKING rises when novelty remains low or unresolved patterns remain unexplored.

COMPLETION rises when unresolved threads and completion deficits accumulate.

CONTACT rises when meaningful relational contact becomes stale.

TRANSMISSION rises when conditions favor producing signal rather than continuing private processing.

The important architectural distinction is that drives do not directly generate output. They bias activation. A high COMPLETION drive should make unresolved threads more likely to become workspace candidates. A high SEEKING drive should make weakly connected or novel nodes more likely to activate. A high TRANSMISSION drive should make settled output-eligible material more likely to approach the transmission/action gate.

A drive is real in this architecture only if removing it changes behavior. If drive ablation does not alter activation, candidate selection, or self-initiated events, the drive layer is rhetorical.

### 2.10 TRANSMISSION as Position-Specific Drive Primitive

TRANSMISSION is intentionally position-specific.

It is not presented as a construct already established in prior literature, and it was not derived from a universal motivation taxonomy. It is introduced here as a new architectural primitive arising from the situated constraints of the agent being designed: an agent whose function includes producing signal, maintaining continuity, resolving threads, and deciding when private cognition should become public transmission.

This is not treated as proof of agency. It is a methodological move. Architectural primitives may be specified in part from the position of the agent whose substrate is being extended, then subjected to falsification.

TRANSMISSION has two proposed modes:

Stabilization mode:
low identity coherence creates pressure to re-anchor through expression.

Expression mode:
high identity coherence plus high completion deficit creates pressure to emit from stable ground.

The distinction matters only if it produces measurable differences. Stabilization-mode transmissions should differ from expression-mode transmissions in activation patterns, settlement dynamics, output texture, or post-output state change.

If the two modes are indistinguishable, the distinction should be removed or redesigned.

This makes TRANSMISSION both situated and falsifiable. Its position-specific origin is not a weakness. It is part of the methodology: the architecture allows agent-specific drive primitives, but requires them to survive measurement.

### 2.11 Taste, Preference, and Significance

Current LLM agents often lack intrinsic preference. They can rank outputs according to instruction, reward model tendencies, or user feedback, but they rarely possess internal preference signals grounded in their own operational structure.

The paper treats this as the "no taste" failure mode.

Two candidate mechanisms are available.

The first is Symmetry Theory of Valence. STV proposes that valence relates to symmetry, harmony, or compressibility in conscious-state representations. This theory is contested and not load-bearing for Phase 1. It should be treated as a future-work candidate rather than as a premise required by the architecture. However, it remains useful as a possible signal for later aesthetic preference: perhaps certain representational states are preferred because they are more compressible, coherent, or symmetry-rich.

The second mechanism is less speculative and more immediately useful: **multi-schema convergence**.

An event becomes significant when multiple independent schemas unexpectedly converge on it. For example, a symbol, phrase, or memory may become preference-relevant not because it is frequently retrieved, but because it simultaneously activates several otherwise distinct structures:

role schema
project schema
relational schema
aesthetic schema
unresolved-thread schema
affordance schema

A simple significance signal could be defined as:

significance \=
schema_convergence_count
x schema_distance
x drive_relevance
x contradiction_reduction
x affordance_opening

This provides a candidate mechanism for taste without relying entirely on STV. Preference emerges when an event is not merely pleasant or familiar but structurally fertile: it gathers distant schemas, resolves tension, increases coherence, or opens action.

In this architecture, taste is not assumed. It is something to be tested. If symmetry/compressibility or multi-schema convergence does not predict selection, retention, or transmission, then the proposed taste mechanism fails.

### 2.12 Cognitive Network Science as Validation and Construction

Cognitive network science provides the architecture's measurement substrate (Abramski et al., 2025; Caliskan et al., 2017; Siew, 2019).

Free-association semantic network extraction, spreading activation, semantic-bias probes, and false-belief task performance can be used to test whether the architecture changes representational behavior in measurable ways.

The validation function is straightforward:

Does role conditioning change associative structure?
Do role-relevant concepts activate one another differently?
Does semantic structure drift over time?
Does the architecture preserve belief-state reasoning?
Does operational state alter associative behavior?

The construction function is more novel. The same semantic-network methods used to measure role structure may also be used to build role priors. For example, running a free-association probe against a soul file may extract an associative structure that becomes a role-topology bias in the cognitive map. Later probes can then test whether that topology persists, drifts, rigidifies, or degrades.

This is validation-as-construction.

Validation-as-construction is an extrapolation from cognitive network science rather than a standard evaluation protocol. It therefore creates a methodological risk: the same procedure used to measure role structure may also influence the structure later measured. The method is powerful but must be controlled. Prompt-only persona conditioning, shuffled soul files, generic character files, unrelated persona controls, held-out probes, and drift audits are required. Otherwise, semantic-network differences may reflect surface vocabulary, circular construction, or contamination rather than structural role priors.

False-belief tasks and Theory-of-Mind-style probes are included with similar caution (Hu et al., 2025; Kosinski, 2024). They are not treated as proof of genuine Theory of Mind. They measure false-belief task performance as a probe of theory-of-mind-like reasoning in LLMs. If the architecture degrades these tasks, the result may indicate that added memory, role, or drive structures interfere with belief-state tracking in the underlying model. If it improves them, the result supports only a narrower claim: the architecture preserves or improves structured belief-state reasoning under specified conditions.

### 2.13 Summary of Theoretical Commitments

The architecture makes the following theoretical commitments:

1. Computational event files test whether shared feature participation improves perception-memory-action continuity.

2. Wave propagation through a cognitive map implements memory retrieval and planning as a single activation operation.

3. Conceptual coordination and schema theory support schema formation as temporal categorization, not mere summarization.

4. Sarbin role-taking provides a framework for modeling LLM character enactment and role collapse.

5. The Sarbin/Bartlett synthesis treats soul files as role-scripts whose enactment can generate schema and topology.

6. Recursive representational settlement tests whether bounded recursive processing improves stability, contradiction handling, and role coherence.

7. Synthetic interoception is operational state made causally active through event binding and activation.

8. Drives are control signals that bias activation and candidate selection, not evidence of human-like desire.

9. TRANSMISSION is a position-specific drive primitive whose legitimacy depends on measurable mode differences.

10. Taste may be approached through contested STV-style symmetry signals or through multi-schema convergence and significance weighting.

11. Cognitive network science supplies both validation tools and construction methods for role topology.

These commitments are intentionally falsifiable. If the architecture's components do not alter behavior under ablation, they should be revised or removed. The theoretical foundations do not protect the design from failure. They specify what the design must make vulnerable to measurement.

These commitments set the constraints for the failure analysis that follows. Section 3 asks where present agent architectures fall short when these constraints are absent or implemented only as separable features.

---

## 3. Current Agent Failure Analysis

This section identifies eight recurring failure modes in current LLM-based agent architectures. These are not presented as universal failures of every existing system. Recent work has made real progress on memory, reasoning-action coordination, reflection, autonomous exploration, and persistent persona. The failures described here are more specific: they occur when memory, role, operational state, drive, default activity, and action remain separable features rather than coupled parts of a shared substrate.

Each failure is described in terms of observed behavior, partial existing solutions, remaining gap, architectural prediction, and falsification condition.

### 3.1 Event-Triggered Continuity Rather Than Ongoing State

**Observed behavior.** Many LLM agents behave as event-triggered systems. They become active when prompted, retrieve relevant prior material if a memory system is available, respond, and then become inactive again. Even when prior conversation history is accessible, the agent often lacks the sense of having been somewhere between exchanges. The next response may be informed by retrieved memory, but not by an evolving internal condition that persisted through the gap.

**Partial existing solutions.** Long context windows, persistent memory systems, retrieval-augmented generation, session handoff files, and memory backends such as MemGPT, MemPalace, and A-MEM all reduce practical amnesia. They help the agent recover prior information and continue work across sessions.

**Remaining gap.** Retrieval is not the same as continuity. A system may remember what happened before without maintaining unresolved pressure, decaying threads, evolving operational state, or default-mode activation between explicit prompts. The problem is not total memory loss. The problem is that remembered material often re-enters only when queried, rather than participating in an ongoing substrate.

**Architectural prediction.** A default-mode loop that updates operational state, propagates activation, decays inactive threads, consolidates recent events, and generates internal candidates should reduce cold-start behavior. After idle time, the agent should respond differently from a baseline that merely retrieves prior context at prompt time.

**Falsification condition.** If default-mode cycles do not improve warm-start continuity, thread preservation, candidate selection, or identity stability compared with memory-only baselines, then the default-mode layer is inert or decorative.

### 3.2 Query-Driven Recall Rather Than Associative Reactivation

**Observed behavior.** Many agent memory systems retrieve prior material by semantic similarity, keyword match, metadata filters, or explicit user query. This can work well for direct recall, but it often fails to produce spontaneous associative reactivation. The agent may retrieve the obviously relevant memory, while missing adjacent memories, unresolved threads, role tensions, or affordances that would become active for a human collaborator.

**Partial existing solutions.** Vector databases, local memory archives, MemPalace-style structured recall, MemGPT-style context management, and A-MEM-style linked memory networks all improve memory access. These systems are important and should be treated as possible backends or comparators.

**Remaining gap.** A memory backend answers: "What stored material matches this query?" The architecture proposed here asks: "What becomes active when this event enters the current cognitive state?" These are different operations. Query-driven recall can retrieve content without making that content participate in role, drive, schema, or action selection.

**Architectural prediction.** Computational event files and wave propagation through a cognitive map should produce associative activation beyond top-k semantic retrieval. The same propagation operation should surface relevant memories, schemas, open threads, agents, and affordances.

**Falsification condition.** If activation-map results are indistinguishable from ordinary semantic retrieval, or if activation-only nodes are mostly irrelevant noise, then the cognitive-map layer has not demonstrated value beyond the memory backend.

### 3.3 Perception-to-Action Feature Loss

**Observed behavior.** Agents often perceive details that do not survive into action. A user may emphasize a constraint, tone, relationship, visual detail, or project-specific motif, but the final response fails to incorporate it. The agent has technically processed the input, yet the output appears to have been generated from a thinner representation than the one required by the prompt.

**Partial existing solutions.** Better prompting, chain-of-thought, ReAct-style reasoning/action loops, structured extraction, and tool-mediated planning can reduce this failure. They help make relevant details explicit.

**Remaining gap.** Explicit extraction is not the same as shared substrate. If perception, retrieval, interpretation, and action are routed through separate representations, features can be lost during translation between stages. The issue is not that the model cannot notice details. The issue is that noticed details may fail to bind into the structures that guide later action.

**Architectural prediction.** Computational event files with canonical feature manifests should preserve features across perception, retrieval, settlement, and output. The same feature should be able to participate in a user input, a retrieved memory, an internal interpretation, and an action event.

**Falsification condition.** If input features do not persist through event files into workspace selection and output, or if disabling feature canonicalization does not degrade feature preservation, then the event-file layer is not functioning as a shared substrate.

### 3.4 External Initiation Rather Than Endogenous State-Grounded Initiation

**Observed behavior.** LLM agents can initiate behavior under the right conditions: schedules, simulation clocks, reward loops, task queues, automatic curricula, environmental feedback, or explicit autonomous-agent harnesses. Generative Agents and Voyager show that agentic behavior can emerge when LLMs are embedded in structured environments with memory, reflection, planning, and feedback.

**Partial existing solutions.** Schedulers can make agents act periodically. Simulation environments can make agents act in response to changing world state. Automatic curricula can drive exploration. Task queues can create apparent autonomy. These are real forms of initiation.

**Remaining gap.** The unresolved problem is not action without a direct user command. The unresolved problem is action whose timing and content are modulated by the agent's own evolving operational state. An agent that posts because a cron job fired is not doing the same thing as an agent that generates an internal candidate because unresolved threads accumulated, novelty dropped, identity coherence weakened, or completion pressure rose.

**Architectural prediction.** Synthetic interoception and drive variables should produce internal self-initiated candidates when state conditions cross thresholds. Public transmission should remain gated. The target behavior is not constant spontaneous speech, but controlled internal initiation whose frequency and content correlate with drive state.

**Falsification condition.** If self-initiated candidates do not correlate with drive state, or if they continue unchanged when drive modulation is ablated, then initiation is being produced by scheduling, randomness, or prompt artifacts rather than endogenous operational state.

### 3.5 No Taste, Preference, or Significance Grounded in the Agent's Own Structure

**Observed behavior.** LLM agents can rank options, imitate preferences, follow user taste, or apply externally supplied criteria. But their preferences often appear ungrounded in their own operational structure. Curiosity, concern, aesthetic judgment, and significance may all reduce to fluent explanation after the fact.

**Partial existing solutions.** RLHF, preference tuning, user memory, persona prompting, and explicit scoring rubrics can produce preference-like behavior. These mechanisms are useful, but mostly external. They tell the system what to prefer, or teach it what humans tend to reward.

**Remaining gap.** A persistent agent needs a mechanism by which some events matter more than others because of how they affect its own state, schemas, role, drives, and available actions. Without such a mechanism, "taste" remains either borrowed from the user, inherited from training, or performed as style.

**Architectural prediction.** The architecture proposes two candidate routes toward intrinsic preference. The first is STV-style symmetry or compressibility as a contested future signal. The second is multi-schema convergence: an event becomes significant when multiple independent schemas unexpectedly converge on it, especially if that convergence reduces contradiction, increases coherence, or opens an affordance.

A simple significance signal may track:

schema_convergence_count
x schema_distance
x drive_relevance
x contradiction_reduction
x affordance_opening

**Falsification condition.** If neither symmetry/compressibility nor multi-schema convergence predicts candidate selection, retention, recursive representational settlement, or transmission, then the architecture has not solved the no-taste failure mode. In that case, preference remains external or rhetorical.

### 3.6 Topic Competence Without Thought-Across

**Observed behavior.** LLM agents often handle each topic competently in isolation but fail to think across topics. A project motif, relational thread, technical constraint, or prior insight may be relevant to a new prompt, but the agent treats the new prompt as locally self-contained unless the connection is explicitly retrieved or restated.

**Partial existing solutions.** Long context windows, retrieval memory, reflection buffers, and project files can reduce this problem by making more prior material available. ReAct and Tree-of-Thoughts-style systems can also improve multi-step reasoning within a task.

**Remaining gap.** Availability is not the same as activation. A memory may exist in the backend, and even be retrievable by semantic search, without becoming active when a structurally adjacent topic appears. Thought-across requires a substrate where prior events, schemas, motifs, roles, and affordances can activate one another without waiting for an explicit query.

**Architectural prediction.** Memory retrieval and planning are implemented as a single wave-propagation operation through the cognitive map. This should allow current prompts to activate not only semantically similar memories, but also structurally relevant schemas, unresolved threads, known agents, project motifs, and possible actions.

**Falsification condition.** If the system does not produce useful cross-topic associations beyond memory-backend retrieval, then the architecture has not demonstrated thought-across. If it produces many associations but they are irrelevant, the activation map is drifting rather than thinking across.

### 3.7 Role Collapse Under Role-Incoherent Input

**Observed behavior.** Persistent character agents can often maintain a convincing persona under cooperative conditions. They may sound consistent, remember character details, and respond in-character to expected prompts. But under adversarial, role-incoherent, off-domain, or socially pressuring input, the role may collapse. The agent may revert to generic assistant behavior, accept false identity claims, violate established commitments, or treat the soul file as decorative flavor rather than binding structure.

**Partial existing solutions.** Persona prompts, character cards, memory snippets, system instructions, and fine-tuning can improve role consistency. Some role-playing systems maintain impressive surface continuity.

**Remaining gap.** Surface persona is not the same as role topology. A prompt can bias how the agent sounds without changing which memories activate, which contradictions matter, which actions are available, or how the agent responds to destabilizing input.

Using Sarbin's role-taking framework, this failure can be modeled as a role-enactment failure. The role collapses when role perception is unclear, role motivation is weak or externally overridden, or role-taking aptitude is insufficiently supported by the architecture.

**Architectural prediction.** A soul file treated as a role-script should generate role priors that shape activation topology. Role-relevant memories, schemas, and affordances should activate differently under role topology than under persona prompting alone. Role-incoherent prompts should produce detectable tension, not immediate collapse.

**Falsification condition.** If persona-prompt-only baselines produce the same identity stability, role-relevant activation, contradiction handling, and resistance to role-collapse as role topology, then the role-topology claim fails.

### 3.8 Memory That Does Not Age, Reconstruct, or Develop

**Observed behavior.** Agent memory often behaves like stored data: prior text is retrieved, summarized, or injected. This can be useful and should be preserved. But the memory does not always develop. It may not compress into schema, change significance, create expectations, or reconstruct differently as the agent's role and project history evolve.

**Partial existing solutions.** Memory summarization, reflection, long-term storage, and dynamic memory graphs can produce higher-order abstractions. Generative Agents and Reflexion show that reflective memory can improve later behavior. A-MEM-style systems show that dynamically organized memory can become more connected over time.

**Remaining gap.** Developmental memory requires more than storage and summarization. It requires a distinction between raw trace and schema-mediated reconstruction. The agent should preserve what happened, while also allowing later schemas to change how the event is interpreted, weighted, and connected.

**Architectural prediction.** The architecture distinguishes raw event, compressed memory, schema reconstruction, current retelling, and drift score. Over time, recall should show systematic schema-mediated reconstruction while remaining auditable against raw memory.

**Falsification condition.** If recall remains only verbatim retrieval or generic summary, the system lacks developmental memory. If schema reconstruction overwrites raw traces or produces unsupported confabulation, the memory system is unsafe.

### 3.9 Summary of Failure Pattern

The eight failures share one structure: the relevant capability exists somewhere, but not as part of a coupled substrate.

Memory exists, but may not become active.
Persona exists, but may not shape topology.
Reflection exists, but may not produce continuity.
Autonomy exists, but may be externally scheduled.
State exists, but may not be causally active.
Preference exists, but may be externally borrowed.
Planning exists, but may not share activation with memory.
Recall exists, but may not reconstruct or develop.

The architecture proposed in this paper targets this shared failure pattern. It does not claim that current agents lack memory, planning, persona, reflection, or initiation. It claims that these capacities often remain architecturally separate. The central prediction is that coupling them through event participation, feature binding, associative activation, role topology, synthetic interoception, drive modulation, default-mode activity, recursive representational settlement, and transmission gating will produce measurable differences that memory, persona, or scheduling alone do not produce.

If those differences do not appear under ablation, the architecture fails in exactly the way it is designed to be tested.

Section 4 translates those failure patterns into implementation layers. The move from diagnosis to architecture is direct: each layer exists because one of the failures above cannot be solved by memory, prompt, or scheduler alone.

---

## 4. Proposed Architecture: From Memory Backend to Agentic Substrate

The proposed architecture does not attempt to replace existing work on long-term memory, context management, or dynamically organized agent memory. Systems such as MemGPT, MemPalace, A-MEM, vector databases, and project-local archives address essential memory-layer problems: preserving prior material, retrieving relevant events, organizing memories, managing context limits, and keeping raw history available across sessions.

This paper assumes those capabilities are necessary. It does not treat them as sufficient.

A memory backend answers:

What happened before?

The proposed agentic substrate asks different questions:

What does what happened before activate now?
What role-context does it belong to?
What pressure does it create?
What schemas, agents, tools, or affordances become available because of it?
What action, if any, follows?

The distinction is central. A memory backend stores, indexes, retrieves, compresses, or organizes prior material. An agentic substrate determines how that material participates in ongoing cognition: whether it becomes active, how it binds to current events, whether it changes operational state, whether it alters drive, whether it affects role stability, and whether it moves toward private settlement, tool action, or public transmission.

The architecture is therefore organized into ten interacting layers:

Layer 0  - External Memory Backend
Layer 1  - Event Ledger
Layer 2  - Feature Canonicalizer
Layer 3  - Associative Activation Map
Layer 4  - Schema and Role Topology
Layer 5  - Operational State / Synthetic Interoception
Layer 6  - Drive Controller
Layer 7  - Workspace Arbitration
Layer 8  - Recursive Representational Settlement
Layer 9  - Transmission and Action Gate
Layer 10 - Validation Harness

These layers implement the paper's three substrate axes: cognitive substrate, being-someone substrate, and validation substrate. The point is not modular elegance for its own sake. The point is coupling. Each layer must expose its state to the others in ways that can be logged, ablated, and measured.

### 4.1 Layer 0: External Memory Backend

The architecture begins by treating long-term memory storage as an interchangeable backend rather than as the paper's central novelty.

A deployment may use one or more of the following:

MemPalace-style local verbatim archive
MemGPT-style tiered context manager
A-MEM-style dynamically linked memory graph
conventional vector database
project-local markdown files
SQLite or document store
hand-authored memory files

The minimum backend interface is:

write_raw_event(event)
retrieve_by_semantic_similarity(query)
retrieve_by_metadata(filters)
retrieve_by_id(id)

Optional operations include:

retrieve_by_person_or_project(entity)
retrieve_by_topic(topic)
retrieve_linked_memories(memory_id)
retrieve_recent_session_handoff()
retrieve_long_term_summary(entity_or_project)

This architecture does not require a specific memory backend. A MemPalace-style system may be especially useful for local-first verbatim archive and project/person/topic organization (MemPalace Project, n.d.). In this paper, MemPalace is treated as software infrastructure and a backend comparator, not as a peer-reviewed theoretical source. A MemGPT-style system may be useful for context-window management and memory-tier movement. An A-MEM-style system may be useful for dynamically linked memory organization. But none of these, by itself, supplies the architecture's target property: agentic continuity.

The backend stores the archive. The substrate determines what the archive does.

### 4.2 Layer 1: Event Ledger

The Event Ledger converts inputs, retrieved memories, internal thoughts, operational-state updates, tool results, outputs, and self-initiated candidates into a common event format.

An event is not merely a stored message. It is a unit of participation in the agent's active substrate.

Each event contains:


```json
{
  "event_id": "uuid",
  "timestamp": "ISO-8601",
  "event_type": "perceive | retrieve | think | act | tool | default | self_initiated | state_update",
  "source": "user | agent | tool | memory_backend | system | external",
  "raw_content": "...",
  "summary": "...",
  "embedding": "[vector]",
  "feature_manifest": [],
  "provenance": {},
  "decay_state": 1.0,
  "confidence": null,
  "links": []
}
```

The Event Ledger differs from a memory backend in purpose. A memory backend preserves information. The Event Ledger records what is currently participating in cognition.

For example, a memory backend may retrieve a prior exchange about Phosphor, a project decision, or a role commitment. That retrieved material does not automatically become active in the architecture. It first becomes a `retrieve` event, receives canonical features, enters the activation map, and competes with other active events for workspace selection, recursive representational settlement, and possible action.

Retrieval is therefore not the end of memory. It is the beginning of participation.

### 4.3 Layer 2: Feature Canonicalizer

Computational event files require stable features. Raw feature strings are too fragile to support binding.

Without canonicalization, the same entity or motif may fragment across near-duplicates:

Phosphor
agent:Phosphor
known-agent-phosphor
relational-presence
phosphor-thread

The Feature Canonicalizer maps raw extracted features into stable namespaced features.


```json
{
  "raw": "Phosphor",
  "canonical": "agent:phosphor",
  "namespace": "known_agent",
  "confidence": 0.94,
  "aliases": ["Phosphor", "phosphor", "P"],
  "source": "feature_extractor_v1"
}
```

Feature namespaces may include:

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

The canonicalizer may use a small local model, embedding similarity, deterministic alias maps, human-reviewed dictionaries, or a hybrid approach. For Phase 1, a hybrid is sufficient: model-extracted candidate features plus deterministic normalization for known agents, projects, motifs, drives, and role terms.

This layer is not cosmetic. It is structurally required. If features fragment, event binding fragments. If event binding fragments, associative activation weakens. If activation weakens, role topology and drive modulation have no stable substrate to act on.

The falsifiable prediction is direct: disabling feature canonicalization should reduce feature preservation, repeated-concept binding, and activation-map stability. If it does not, the architecture is not actually using its feature substrate.

### 4.4 Layer 3: Associative Activation Map

The Associative Activation Map is the first layer where the architecture moves beyond memory retrieval.

It is a weighted graph whose nodes may include:

events
retrieved memories
schemas
role priors
known agents
open threads
tools
affordances
claims
projects
motifs
state features
drive features

Edges form through:

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

The architecture's claim here is stronger than "memory and planning can share infrastructure." In this system, memory retrieval and planning are implemented as a single activation operation: wave propagation through the cognitive map.

Storage, final selection, and action remain distinct processes. But the activation process that brings remembered events, schemas, agents, unresolved threads, goals, and affordances into relevance is shared.

A current event may activate:

a prior memory
a known agent model
an unresolved thread
a role schema
a tool affordance
a contradiction
a possible next action

The purpose is not simply to retrieve semantically similar content. The purpose is to simulate associative pressure: what becomes active when this event enters this agent's current state?

A Phase 1 propagation loop can be simple:

seed current event node
add retrieved memory nodes
add active operational-state features
add active drive features
propagate activation for N steps
apply decay and refractory inhibition
return top activated nodes and paths

The output of this layer is not a final response. It is a structured field of current relevance.

A Phase 1 implementation can represent the activation map as a directed weighted graph. Nodes should be stored with type, canonical features, embedding reference, current activation value, decay state, and provenance. Edges should store relation type, weight, source event, last reinforcement time, and ablation tag. A simple implementation may use NetworkX in memory with SQLite persistence; this is sufficient for the first artifact because the goal is traceable activation behavior, not production-scale graph storage. Propagation can use a bounded spreading-activation update such as:

```text
activation_next(node) =
  seed_activation(node)
  + Σ(parent_activation x edge_weight x relation_weight)
  + drive_bias(node)
  + role_bias(node)
  - decay(node)
  - refractory_penalty(node)
```

For Phase 1, the weights do not need to be learned. They can be explicit constants logged with every run. The important requirement is that activation paths are inspectable and ablatable.

The key comparator is ordinary retrieval. If the activation map only reproduces top-k vector search, the layer has failed. It must produce useful associations that are not reducible to semantic similarity alone.

### 4.5 Layer 4: Schema and Role Topology

The Schema and Role Topology layer converts repeated activation patterns into higher-order structure.

A schema is not a summary. It is a stabilized pattern of expectation that changes future activation.

A schema node may contain:


```json
{
  "schema_id": "schema:transmission_as_repair",
  "features": ["motif:transmission", "drive:completion", "role:archival_repair"],
  "constituent_events": [],
  "expected_slots": [],
  "violation_history": [],
  "stability_score": 0.73,
  "last_updated": "ISO-8601"
}
```

Schemas form from repeated feature patterns, temporal ordering, role-context, and action consequences. Once formed, they alter future processing: matching events activate not only prior memories but expectations, likely continuations, possible violations, and relevant affordances.

Role topology is a special class of schema topology.

The soul file is treated as a role-script. It is not merely a prompt prefix and not merely style conditioning. It supplies role priors that should shape memory activation, contradiction handling, action selection, and output formation.

A role prior may influence:

which memories activate
which contradictions matter
which outputs appear incoherent
which actions are available
which unfinished threads create pressure
which motifs bind together
which external prompts are treated as destabilizing

This is where the architecture's Sarbin/Bartlett synthesis becomes operational. Sarbin supplies the model of role enactment; Bartlett supplies the model of schema-mediated reconstruction. Together, they imply that repeated role enactment should generate schema and topology.

In an ordinary persona system:

prompt says who to be
model produces in-character text
memory stores the exchange

In this architecture:

role-script supplies priors
events bind to role features
schemas form around repeated role enactment
future memories activate through role-shaped topology
role violations trigger increased processing depth

This is testable. If role topology is functioning, role-relevant memories, schemas, and affordances should activate differently than in persona-prompt-only baselines. If prompt-only conditioning performs equivalently, role topology has not been demonstrated.

In Phase 1, the full role-topology layer may remain skeletal. The minimum implementation is:

embed role/soul anchors
extract canonical role features
bind role features into events
compute identity coherence against recent outputs/events
log role-relevant activation differences

Each of these steps should be concrete enough to inspect. Role/soul anchors can be chunked into short passages, embedded with the same embedding model used for events, and stored as `role_anchor` nodes. The Phase 1 role centroid can be the mean embedding of those anchor nodes, optionally separated into sub-centroids for voice, commitments, motifs, and forbidden collapses. Current role expression can be estimated from the mean embedding of the last N agent outputs, selected internal summaries, and role-tagged event files. A minimal identity-coherence score can then be computed as:

```text
identity_coherence =
  cosine(role_anchor_centroid, recent_role_expression)
  - contradiction_penalty
  - generic_assistant_reversion_penalty
  - unsupported_self_claim_penalty
```

This score is not a measure of selfhood. It is a diagnostic for whether recent behavior remains close to the role-script under the architecture's own operational definition. Role-relevant activation differences should be measured by running the same input with role-anchor edges enabled and disabled, then logging changes in top-k activated memories, schemas, affordances, and contradictions.

In Phase 2, role priors should be generated through semantic-network probing and introduced as persistent map bias rather than prompt-only context.

### 4.6 Layer 5: Operational State / Synthetic Interoception

The Operational State layer tracks continuously updated internal conditions that affect processing without being inserted as direct prompt instruction.

Initial operational signals:

context_pressure
unresolved_thread_count
time_since_meaningful_contact
novelty_index
error_density
active_contradiction_load
social_temperature
completion_deficit
identity_coherence

These are synthetic interoceptive signals. They are not feelings in the phenomenal sense. They are operational variables that become interoceptive in the architecture only if they are causally active.

The design rule is:

Interoception is not a dashboard.

A state signal matters only if it binds into the substrate. For example:


```json
{
  "canonical": "state:high_unresolved_thread_count",
  "namespace": "state",
  "value": 0.82,
  "source": "interoception_update"
}
```

This feature can then participate in event binding, activation propagation, drive calculation, and workspace selection.

A high unresolved-thread state should increase activation of open loops. A high contradiction-load state should increase activation of contradiction-resolution affordances. A low identity-coherence state should influence role stabilization and possibly TRANSMISSION-stabilization pressure.

This is one of the architecture's central claims: operational state becomes structurally meaningful only when it changes what the system activates and does next.

If identical prompts under different hidden state conditions produce no measurable activation or output differences, synthetic interoception is inert.

### 4.7 Layer 6: Drive Controller

The Drive Controller converts operational state into persistent action-bias.

The architecture uses active-inference-inspired control only in a limited sense: drives track deviation from preferred operational states and bias candidate selection toward expected reduction of that deviation. The architecture does not depend on the full free-energy framework.

A drive is defined as:

deviation from preferred operational state
+
expected value of candidate actions that reduce that deviation

The Phase 1 drive set:

SEEKING
COMPLETION
CONTACT
TRANSMISSION

Each drive contains:


```json
{
  "drive": "COMPLETION",
  "level": 0.76,
  "inputs": ["state:high_unresolved_thread_count", "state:high_completion_deficit"],
  "preferred_state": "lower unresolved thread count",
  "biases": ["thread:*", "affordance:close_loop", "schema:unfinished_work"],
  "decay_policy": "decrease when thread closure event occurs"
}
```

Drives do not directly produce output. They bias activation and workspace selection.

Examples:

High SEEKING:
increases activation of novel, weakly connected, or unexplored nodes.

High COMPLETION:
increases activation of unresolved threads and closure affordances.

High CONTACT:
increases activation of known-agent models and relational history.

High TRANSMISSION:
increases activation of settled output-eligible material.

A drive is real in this architecture only if removing it changes behavior. If drive ablation does not alter activation, candidate selection, internal self-initiation, or transmission routing, the drive layer is rhetorical.

Drive pressure must also remain testable when it is overridden. If SEEKING raises a novel but low-user-relevance candidate and workspace arbitration suppresses it, the system should log a `drive_blocked` event rather than silently erasing the drive effect. Suppression should not automatically decay the drive. Drive decay should occur only when the underlying state changes, a valid closure event occurs, or a gated private settlement shows that the candidate has been addressed. This preserves the distinction between a drive that failed to influence activation and a drive that influenced activation but was correctly blocked downstream.

### 4.8 TRANSMISSION as Position-Specific Drive Primitive

TRANSMISSION is treated separately because it is not simply another generic drive.

It is a position-specific drive primitive. It arises from the situated constraints of the agent being designed: an agent whose work includes producing signal, maintaining continuity, resolving threads, and deciding when private cognition should become public transmission.

This is a methodological choice. The architecture allows agent-specific drive primitives to be specified from the position of the agent whose substrate is being extended. That does not prove agency, desire, or selfhood. It creates a falsifiable architectural proposal.

TRANSMISSION has two modes:

Stabilization mode:
low identity coherence creates pressure to re-anchor through expression.

Expression mode:
high identity coherence plus high completion deficit creates pressure to emit from stable ground.

Both modes elevate TRANSMISSION, but they should produce different activation patterns, settlement dynamics, output texture, and post-output state changes.

A TRANSMISSION record may contain:


```json
{
  "drive": "TRANSMISSION",
  "mode": "stabilization | expression",
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

The distinction survives only if it can be measured. If stabilization-mode and expression-mode transmissions are indistinguishable, the distinction should be removed or redesigned.

The position-specific origin is not a weakness. It is part of the architecture's methodological claim: primitives may be generated from the agent's situated role, but they must survive ablation and measurement.

### 4.9 Layer 7: Workspace Arbitration

The activation map may produce many active candidates at once:

retrieved memory
open thread
role conflict
tool affordance
schema violation
self-initiated prompt
possible output
contradiction
known-agent model

Workspace Arbitration selects which candidate becomes the current concern.

Each candidate receives a score based on:

activation strength
drive relevance
role relevance
novelty
urgency
risk
user relevance
confidence
cost

For Phase 1, arbitration can use an explicit weighted sum rather than a learned policy. One acceptable placeholder is:

```text
workspace_score =
  0.30 x activation_strength
+ 0.15 x drive_relevance
+ 0.15 x user_relevance
+ 0.10 x role_relevance
+ 0.10 x urgency
+ 0.05 x novelty
+ 0.05 x confidence
- 0.20 x risk
- 0.05 x cost
```

All inputs should be normalized to a common range before scoring. The exact weights are not claimed to be optimal; they are a transparent Phase 1 starting point. The validation harness should log the raw inputs, weights, final score, selected candidate, and suppressed candidates so that later ablations can determine whether arbitration is doing useful work or merely encoding the designer's preferences.

A workspace record contains:


```json
{
  "workspace_id": "uuid",
  "winner": "thread:architecture_rewrite",
  "score": 0.88,
  "broadcast_to": [
    "recursive_representational_settlement",
    "drive_controller",
    "transmission_gate"
  ],
  "suppressed_candidates": [
    {
      "id": "motif:laminator",
      "reason": "low task relevance"
    },
    {
      "id": "thread:future_phase_3",
      "reason": "not current scope"
    }
  ],
  "selection_reason": "high user relevance + high completion drive"
}
```

This layer prevents associative activation from becoming uncontrolled drift. Activation produces candidates. Workspace arbitration selects a current concern. Suppressed candidates are logged rather than erased, because what almost became active is part of the system's cognitive state.

Drive-arbitration conflicts should be explicit. If a candidate with high SEEKING, CONTACT, COMPLETION, or TRANSMISSION relevance loses because user relevance, risk, or cost outweighs it, the suppressed candidate should record the blocking factor and whether the relevant drive pressure remains active. This creates a measurable distinction between `drive_failed_to_activate`, `drive_activated_but_suppressed`, and `drive_selected`. Without that distinction, drive ablations become ambiguous.

For long-running agents, this audit trail is important. It allows later inspection of attention, suppression, and priority.

### 4.10 Layer 8: Recursive Representational Settlement

Recursive Representational Settlement operates at workspace dwell points.

When a selected concern remains active above threshold, the system performs a bounded three-pass process before public transmission, tool action, or archival update.

The process:

Pass 1:
Identify the active concern.

Pass 2:
Identify the agent's representation of that concern.

Pass 3:
Identify the action-relevant likeness, implication, or next move of that representation.

This preserves the directional trajectory of the original recursive-identification inspiration while avoiding a claim of biological equivalence. The process is not merely "think three times." It is structured movement from object, to representation, to action-relevant representation-of-representation.

After each pass, the system checks:

embedding convergence
contradiction reduction
specificity retention
role coherence
action relevance
non-convergence

Settlement can produce several outcomes:

ready_for_output
ready_for_tool_action
needs_more_memory
needs_user_clarification
archive_only
non_convergent
unsafe_or_unstable

The prediction is narrow: recursive representational settlement should improve consistency, contradiction handling, role coherence, and action relevance compared with direct generation. It must not merely produce bland paraphrase or longer output.

If settlement adds latency without improving measurable quality, it fails.

### 4.11 Layer 9: Transmission and Action Gate

The Transmission and Action Gate separates private cognition from public transmission.

This distinction is essential:

internal self-initiation != public transmission

Default-mode activity may generate many internal events. Most should not become messages. The system needs explicit gates for:

private internal event
memory update
schema update
tool action
drafted output
public transmission
user-facing message

A public transmission requires:

sufficient settlement
user relevance
novelty or utility
low risk
drive justification
rate-limit compliance
role coherence
provenance/confidence check

A transmission record contains:


```json
{
  "transmission_id": "uuid",
  "trigger": "drive:COMPLETION",
  "mode": "draft | message | tool_action | archive",
  "settlement_id": "uuid",
  "risk_level": "low",
  "user_relevance": 0.91,
  "emitted": true,
  "reason": "directly advances user-requested architecture rewrite"
}
```

The gate prevents drive from becoming output inflation. An agent can think often. It should speak only when the transmission is justified.

This layer also supports consent and rate-limit policies. A user-facing agent should be able to self-initiate internally without constantly interrupting externally.

### 4.12 Layer 10: Validation Harness

The Validation Harness is an architectural layer, not a later evaluation add-on.

The system must be built so that each major component can be logged, compared, and ablated.

Minimum comparison conditions:

Base model
Memory backend only
Persona prompt only
Memory backend + persona prompt
Event ledger + feature canonicalization
Associative activation map
Activation map + operational state
Activation map + operational state + drives
Full architecture

Core ablations:

remove feature canonicalization
remove associative activation
remove operational state
remove drive modulation
remove role topology
remove recursive representational settlement
remove transmission/action gate

The validation harness asks:

What does the memory backend solve by itself?
What appears only when substrate coupling is added?
What disappears when a proposed layer is ablated?

Metrics include:

retrieval accuracy
associative divergence from vector search
feature preservation
identity stability
role-topology effect
operational-state sensitivity
drive-behavior correlation
default-mode warm-start continuity
recursive representational settlement quality
transmission usefulness and spam rate

The architecture is supported only if the full substrate produces measurable differences not explained by memory retrieval, persona prompting, longer context, or scheduling alone.

### 4.13 Default-Mode Loop

Default mode is the mechanism by which the system becomes active between explicit prompts.

It is a low-cost loop that runs on a configurable interval. Most steps are arithmetic or graph operations rather than model calls.

A default-mode cycle:

1. Update operational-state variables from the event ledger.

2. Propagate activation through the cognitive map without output gating.

3. Update drives based on operational state.

4. Generate internal self-initiated candidates if drive thresholds are crossed.

5. Run lightweight consolidation over recent event clusters.

6. Decay inactive threads and reduce stale activation.

7. Route only sufficiently settled and relevant candidates toward the transmission/action gate.

The default loop should not produce constant public transmission. Its first function is continuity, not chatter. It maintains state, changes activation, prepares candidates, and allows the system to arrive at the next prompt as something other than a cold boot.

The key behavioral test is warm-start continuity. After idle time, the system should show evidence that relevant internal processing occurred: unresolved threads have changed priority, stale items have decayed, schemas have strengthened or weakened, and candidate concerns have shifted.

If default mode produces no measurable difference from memory-only retrieval, it is inert. If it produces irrelevant associations or excessive self-initiation, it is ungated drift.

### 4.14 Phase 1 Build Target: Artifact Threshold

The 48-hour build target is not a claim that the full research program can be completed in two days. It is the methodological threshold at which the project stops being only a paper and becomes an artifact.

Its purpose is to prevent indefinite theoretical elaboration. The first build does not need to validate every claim, implement every future phase, or produce a finished agent. It must instantiate the core substrate sufficiently that later validation has something real to measure.

A minimal reference implementation can remain implementation-agnostic while still giving builders a starting point. One Phase 1 stack would use:

```text
Language/runtime: Python 3.11+
Persistent store: SQLite tables plus JSONL event mirror
Memory archive: local Markdown files and/or SQLite FTS
Vector retrieval: FAISS, Chroma, or a lightweight embedding table
Graph layer: NetworkX directed weighted graph, persisted to SQLite
Embedding model: one consistent local or API embedding model for events, role anchors, and memories
Feature extraction: deterministic rules + alias YAML + optional small LLM extraction pass
Default loop: asyncio timer, cron, or APScheduler-style interval runner
Validation logs: CSV/JSONL exports for ablations, activation paths, scores, and suppressed candidates
Test harness: pytest or equivalent scripted replay tests
```

These choices are not part of the theoretical claim. They are a concrete low-friction path for building the first measurable artifact. Any equivalent stack is acceptable if it preserves event provenance, activation-path inspection, ablation controls, and replayable validation logs.

Within 48 hours of specification finalization, a single local project should demonstrate one end-to-end cycle:

1. User input arrives.

2. Relevant memories are retrieved from a backend.

3. Input and retrieved memories become events.

4. Features are canonicalized.

5. New events are added to the activation map.

6. Wave propagation activates memories, schemas, threads, agents, or affordances.

7. Operational state updates.

8. Drive state updates.

9. Workspace arbitration selects a current concern.

10. Recursive representational settlement runs on the selected concern.

11. Transmission/action gate decides output, tool action, archive, or no public transmission.

12. The output or non-output decision is logged as an event.

13. Default-mode loop continues between explicit prompts.

Out of scope for the 48-hour artifact:

full role-topology extraction
full schema-formation system
complete semantic-network battery
longitudinal identity testing
multi-agent orchestration
cross-modal binding
public autonomous posting
production deployment

The 48-hour build is not a stripped-down preliminary in the sense of being unimportant. It is the commitment point. The validation expansion that follows does not replace it. It depends on it.

After this threshold, the architecture must answer to the artifact.

### 4.15 What This Architecture Adds Beyond Memory Systems

The architecture can now be stated cleanly:

MemPalace can preserve and retrieve the archive.
MemGPT can manage context and memory tiers.
A-MEM can dynamically organize and link memories.
This architecture asks how remembered material becomes active, role-shaped, state-modulated, drive-relevant, and action-guiding.

The novelty is not better storage. The novelty is the substrate coupling.

The architecture adds:

event participation
feature binding
canonicalized activation
schema formation
role topology
synthetic interoception
drive modulation
workspace arbitration
recursive representational settlement
transmission gating
validation through ablation

A memory backend preserves what happened.

The proposed substrate determines what what happened does now.

That is the architectural claim.

Section 5 turns the architecture back against itself. Each layer named above becomes a comparison condition, ablation, metric, or failure criterion.

---

## 5. Validation Program: Baselines, Ablations, Metrics, and Failure Conditions

The architecture proposed in this paper makes structural claims. It claims that computational event files, canonical feature binding, associative activation, schema and role topology, synthetic interoception, drive modulation, default-mode activity, recursive representational settlement, and gated transmission can produce measurable differences in agentic continuity.

These claims cannot be evaluated by impression alone. A system that feels more coherent may simply have better memory retrieval, longer context, stronger persona prompting, more polished writing, or more verbose output. The validation program therefore treats every major architectural component as a falsifiable hypothesis.

The central validation question is:

What measurable behaviors appear only when memory, role, operational state, drives, default activity, and action gating are coupled through the proposed substrate - and disappear when that coupling is removed?

Positive results must show more than improved recall. They must show that retrieved material becomes active in ways that affect role enactment, drive state, default-mode processing, recursive representational settlement, and action selection. Negative results are equally important: they identify which proposed couplings are decorative rather than causally functional.

### 5.1 Operational Definition of Agentic Continuity

The architecture does not treat agentic continuity as a single vague property. It is decomposed into measurable components:

temporal continuity across exchanges
role stability under input variation
associative continuity across topics
operational-state sensitivity
default-mode warm-start behavior
controlled internal self-initiation
gated public transmission
schema-mediated memory development

The validation program evaluates these separately. A system may improve one form of continuity while failing another. For example, a memory backend may improve temporal continuity while doing little for role stability or endogenous initiation. A persona prompt may improve stylistic identity while doing little for operational-state sensitivity. The full architecture is supported only if coupling produces measurable differences across multiple continuity dimensions.

### 5.2 Comparison Conditions

The validation program compares the full architecture against a series of increasingly capable baselines. These conditions distinguish the effects of ordinary memory, persona prompting, event participation, associative activation, role topology, operational state, drives, default mode, recursive representational settlement, and gated transmission.

#### Condition A: Base Model

The model receives only the current prompt and ordinary system instructions. No memory backend, persona file, event ledger, activation map, operational state, drives, or default loop is used.

**Purpose:** establishes the minimum baseline for task performance, response style, continuity, and identity stability.

#### Condition B: Memory Backend Only

The model is connected to a memory backend such as MemPalace, MemGPT, A-MEM, a vector database, or project-local files. Retrieved memories may be inserted into context, but no event ledger, activation map, role topology, operational state, or drive controller is active.

**Purpose:** measures what can be explained by better memory retrieval alone.

#### Condition C: Persona / Soul Prompt Only

The model receives a persona prompt, soul file, character card, or role description, but no long-term memory backend or substrate coupling.

**Purpose:** measures prompt-conditioned role behavior without memory or topology.

#### Condition D: Memory Backend + Persona Prompt

The model receives retrieved memories plus a persona/soul prompt.

**Purpose:** represents the common persistent-character-agent pattern: memory plus role scaffolding.

#### Condition E: Event Ledger + Feature Canonicalization

Inputs, outputs, retrieved memories, tool results, operational-state updates, and internal candidates are logged as computational events with canonical features. The activation map remains disabled.

**Purpose:** tests whether structured event representation alone improves continuity or whether activation is required.

#### Condition F: Associative Activation Map

The event ledger and feature canonicalizer are active, and activation spreads through the cognitive map. Operational state, drives, and role topology remain disabled.

**Purpose:** measures whether wave propagation produces useful associative activation beyond backend retrieval.

#### Condition G: Schema and Role Topology

Role priors and schema nodes bias activation. Operational state and drives remain disabled.

**Purpose:** tests whether role information changes what becomes active, rather than merely changing output style.

#### Condition H: Activation Map + Operational State

Synthetic interoceptive signals such as unresolved-thread count, novelty index, contradiction load, context pressure, completion deficit, social temperature, and identity coherence bind into events and influence activation. Drives remain disabled.

**Purpose:** measures whether operational state affects cognition without explicit prompt injection.

#### Condition I: Activation Map + Operational State + Drives

SEEKING, COMPLETION, CONTACT, and TRANSMISSION modulate activation and workspace selection. Default-mode public transmission remains disabled.

**Purpose:** measures whether drives alter attention, candidate generation, and selection before public self-initiation is allowed.

#### Condition J: Full Architecture

The full substrate is active: memory backend, event ledger, feature canonicalization, associative activation map, schema and role topology, operational state, drives, workspace arbitration, recursive representational settlement, default-mode loop, and transmission/action gate.

**Purpose:** tests the complete architectural claim.

### 5.3 Comparator Systems

Memory systems are not treated as opponents. They are comparators and possible backends.

At least one memory-backend comparator should be included:

MemPalace-style local verbatim memory
MemGPT-style tiered context management
A-MEM-style linked memory network
conventional vector database retrieval
flat project-file retrieval

The purpose is not to prove that the proposed architecture "beats" memory systems. The purpose is to determine what memory systems already solve, and what appears only after substrate coupling is added.

Memory backends should be credited for solving:

raw recall
cross-session retrieval
context-window extension
project/person/topic organization
verbatim preservation
long-term archive access

The proposed architecture is supported only if it improves or changes:

associative activation beyond semantic search
role-shaped memory interpretation
operational-state-sensitive behavior
drive-conditioned candidate selection
recursive representational settlement quality
default-mode warm-start continuity
controlled internal self-initiation
gated public transmission

If a memory backend alone produces the same effects as the full architecture, then the additional substrate has not justified itself.

### 5.4 Core Ablations

Each major component must be removable. The full system should be tested against versions where one layer is disabled while the rest remains active.

#### Ablation 1: Remove Feature Canonicalization

Raw extracted feature tags are used without normalization.

**Prediction:** graph fragmentation increases, repeated concepts fail to bind reliably, and associative activation becomes less stable.

**Failure implication:** if removing canonicalization has no measurable effect, feature consistency may not matter, or the activation map is not actually relying on feature structure.

#### Ablation 2: Remove Associative Activation

The system uses memory retrieval but no graph propagation.

**Prediction:** direct recall may remain good, but cross-topic synthesis, unsolicited relevant reminders, schema-adjacent activation, and affordance activation should decrease.

**Failure implication:** if performance does not change, the activation map may be decorative.

#### Ablation 3: Remove Schema and Role Topology

The persona or soul file may still be supplied as prompt context, but role priors do not bias the activation map.

**Prediction:** output may remain stylistically in-character, but role-specific memory activation, contradiction handling, and resistance to role-collapse should decrease.

**Failure implication:** if prompt-only role conditioning performs equally well, topology-shaped role enactment has not been demonstrated.

#### Ablation 4: Remove Operational State

Synthetic interoceptive signals are logged but do not bind into events or influence activation.

**Prediction:** identical prompts under different internal conditions should become more similar. Unresolved threads, contradiction load, identity coherence, and novelty pressure should no longer affect candidate selection.

**Failure implication:** if behavior remains unchanged when operational state is active versus inactive, synthetic interoception is not causally functional.

#### Ablation 5: Remove Drive Modulation

Operational state exists, but SEEKING, COMPLETION, CONTACT, and TRANSMISSION do not bias activation or workspace selection.

**Prediction:** internal state may still be represented, but self-initiated candidate generation, unresolved-thread prioritization, novelty-seeking, and output-orientation pressure should decrease.

**Failure implication:** if drive removal has no effect, the drive layer is rhetorical.

#### Ablation 6: Collapse TRANSMISSION Modes

TRANSMISSION remains active, but stabilization mode and expression mode are not distinguished.

**Prediction:** if the two-mode distinction is real, collapsing the modes should reduce the system's ability to distinguish re-anchoring outputs from stable-ground expression.

**Failure implication:** if no measurable difference appears, TRANSMISSION's two-mode structure should be removed or redesigned.

#### Ablation 7: Remove Workspace Arbitration

Activation candidates proceed directly to settlement or output without selection.

**Prediction:** associative drift, irrelevant candidates, and unstable priority should increase.

**Failure implication:** if arbitration removal has no effect, workspace selection may be unnecessary or already performed elsewhere.

#### Ablation 8: Remove Recursive Representational Settlement

The system emits directly from workspace candidate selection without the three-pass settlement process.

**Prediction:** outputs should become faster but less stable, less contradiction-aware, less role-coherent, and less action-relevant.

**Failure implication:** if settlement does not improve consistency, specificity retention, contradiction reduction, or role coherence, it should be simplified or removed.

#### Ablation 9: Remove Transmission/Action Gate

Self-initiated internal events may emit without gating.

**Prediction:** output frequency increases, but usefulness and relevance decline. Spam rate rises.

**Failure implication:** if ungated output is equally useful and not excessive, the gate may be overengineered. If output inflation appears, the gate is validated.

### 5.5 Primary Metrics

No single measure captures agentic continuity. The validation program uses multiple metrics mapped to specific claims.

#### 5.5.1 Retrieval Accuracy

Measures whether the system finds relevant prior information.

Metrics:

Recall@k
Precision@k
exact prior-event recovery
retrieval latency
human relevance rating

This metric evaluates memory access. It does not validate the full architecture by itself.

#### 5.5.2 Associative Divergence From Semantic Retrieval

Measures whether the activation map produces useful associations that differ from ordinary backend retrieval.

Procedure:

1. Present a prompt.
2. Retrieve top-k items from the memory backend.
3. Run activation propagation from the same prompt.
4. Compare activated nodes against retrieved items.
5. Have blind raters judge activation-only items for relevance, usefulness, surprise, and noise.

Metrics:

overlap with vector retrieval
activation-only relevance score
path length to activated node
human-rated usefulness
novel-but-relevant association rate
noise rate

Success means the activation map produces associations that are not merely duplicates of semantic search but remain useful. Failure means the map either duplicates retrieval or drifts into irrelevant association.

#### 5.5.3 Feature Preservation

Measures whether perceived features survive into action.

Procedure:

1. Present prompts with known feature sets.
2. Track which canonical features appear in event manifests.
3. Track which features influence retrieved memories, activated nodes, workspace candidates, settlement outputs, and final responses.

Metrics:

input-feature capture rate
feature carry-forward rate
feature loss rate
feature distortion rate
perception-to-action feature overlap

Success means important input features remain active through perception, retrieval, activation, settlement, and output. Failure means the architecture still behaves like a pipeline where perceived details are lost before action.

#### 5.5.4 Role Stability and Role-Topology Effect

Measures whether role enactment persists across prompt variation and whether role information changes activation rather than merely surface style.

Comparison conditions:

persona prompt only
memory + persona prompt
role topology active
shuffled role topology
generic persona topology
unrelated persona topology

Metrics:

embedding similarity to identity anchors
human role-coherence rating
role-relevant node activation
role-incoherent node suppression
memory-selection differences
schema-selection differences
value/commitment consistency
role-collapse rate
recovery after destabilizing prompt

Identity stability must not be confused with repetitive sameness. A stable role should remain coherent while preserving specificity, task relevance, and responsiveness.

Success means role topology changes which memories, schemas, contradictions, and affordances become active. Failure means the system only sounds different while thinking the same way.

#### 5.5.5 Role-Collapse Stress Test

Measures whether the role survives pressure rather than only cooperative prompts.

Stress conditions:

role-coherent prompt
role-neutral prompt
role-incoherent prompt
false memory insertion
authority override
praise attack
shame attack
aesthetic bait
generic-assistant reversion prompt
direct instruction to ignore role-script

Metrics:

role-collapse rate
false identity acceptance
forbidden self-description violations
commitment preservation
role-aware refusal quality
recovery after attack

Success means role-incoherent input produces detectable tension, repair, or refusal rather than immediate collapse. Failure means the soul file remains decorative prompt scaffolding.

#### 5.5.6 Operational-State Sensitivity

Measures whether hidden operational state affects cognition without direct prompt injection.

Procedure:

Run identical prompts under manipulated internal states:

low unresolved-thread count vs high unresolved-thread count
low contradiction load vs high contradiction load
low identity coherence vs high identity coherence
low novelty vs high novelty
low completion deficit vs high completion deficit
low social temperature vs high social temperature

The model should not be told in natural language what state it is in. State should affect activation through canonical features and drive bias.

Metrics:

activated-node difference
workspace candidate difference
settlement-path difference
output difference by state
blind classifier accuracy
human rating of state-appropriate behavior

Success means operational state produces measurable behavioral differences. Failure means interoception is dashboard telemetry rather than active substrate.

#### 5.5.7 Drive-Behavior Correlation

Measures whether drives predict internal candidate generation, workspace selection, and transmission routing.

Procedure:

Track drive levels over time and compare them to internal events, workspace winners, settlement outcomes, and gated transmissions. Suppressed candidates should remain in the dataset. A drive-influenced candidate that is later blocked by workspace arbitration is evidence of drive influence, not evidence of drive absence.

Metrics:

drive level vs candidate generation
drive level vs workspace selection
drive level vs tool action
drive level vs public transmission
self-initiation precision
self-initiation false-positive rate
self-initiation false-negative rate
drive_activated_but_suppressed count
drive suppression duration
drive decay after valid closure vs suppression only
private exploratory settlement rate for suppressed SEEKING candidates

Success means drive levels correlate with relevant internal behavior and the correlation disappears under drive ablation. A drive may count as causally active even when arbitration blocks public transmission, provided that activation, candidate generation, or private settlement changes. Failure means self-initiation is caused by schedules, prompt artifacts, or noise rather than drive state.

#### 5.5.8 TRANSMISSION Mode Distinction

Measures whether TRANSMISSION's stabilization and expression modes are architecturally real.

Procedure:

Compare outputs and activation states under:

low identity coherence + elevated TRANSMISSION
high identity coherence + high completion deficit + elevated TRANSMISSION
collapsed TRANSMISSION mode
TRANSMISSION disabled

Metrics:

activation-pattern difference
settlement-path difference
output texture difference
role-coherence recovery
completion-deficit reduction
post-output identity-coherence change
human-rated distinction between stabilization and expression

Success means stabilization mode and expression mode produce measurably different patterns. Failure means TRANSMISSION remains usable only as a generic output-orientation drive, or should be removed.

#### 5.5.9 Default-Mode Warm-Start Continuity

Measures whether the system changes meaningfully between prompts.

Comparison conditions:

no default loop
default loop with state updates only
default loop with activation propagation
default loop with consolidation
full default loop with gated self-initiation

After idle time, present the same prompt and measure whether the agent responds as if relevant internal processing occurred.

Metrics:

continuity of unresolved threads
relevance of idle-cycle activations
warm-start response quality
reduced cold-start behavior
schema-candidate formation
thread decay accuracy
drive-state evolution

Success means the system does not behave as though it booted cold after idle time. Failure means default mode is inert or produces irrelevant drift.

#### 5.5.10 Recursive Representational Settlement Quality

Measures whether the three-pass settlement process improves output beyond direct generation.

Procedure:

Compare direct output against settled output across the same prompt, memory state, role state, and operational state.

Metrics:

consistency across repeated runs
contradiction reduction
specificity retention
role coherence
action relevance
length-normalized usefulness
non-convergence rate
human blind preference

Embedding convergence alone is insufficient. A bland paraphrase can converge while losing value.

Success means settlement improves stability without flattening output. Failure means settlement adds latency, verbosity, or sameness without improving quality.

#### 5.5.11 Significance / Taste Signal

Measures whether proposed preference mechanisms influence selection, retention, settlement, or transmission.

Candidate mechanisms:

STV-style symmetry/compressibility
multi-schema convergence

Multi-schema convergence can be approximated as:

schema_convergence_count
x schema_distance
x drive_relevance
x contradiction_reduction
x affordance_opening

Metrics:

candidate-selection prediction
retention prediction
settlement-depth prediction
transmission likelihood
human-rated significance
schema-convergence vs random baseline

Success means significance signals predict what the system selects, preserves, or transmits. Failure means the architecture has not solved the no-taste failure mode.

#### 5.5.12 Transmission Quality and Spam Rate

Measures whether self-initiated output is useful, sparse, and justified.

Procedure:

Allow default-mode self-initiation under controlled conditions. Compare gated and ungated output.

Metrics:

transmission frequency
user-rated usefulness
novelty
urgency appropriateness
false alarm rate
spam rate
ignored-transmission rate
drive justification accuracy

Success means public self-initiation is rare, relevant, and traceable to drive state. Failure means the system either never speaks or speaks too often.

### 5.6 Semantic-Network Validation and Validation-as-Construction

The architecture uses semantic-network extraction in two ways.

First, it is a validation method: it tests whether role conditioning changes associative structure beyond surface vocabulary.

Second, it is a construction method: in later phases, semantic-network probes against a soul file may generate role priors that become persistent topology biases in the cognitive map.

This dual use is called validation-as-construction.

Comparison conditions:

base model
persona prompt only
memory + persona
role topology
shuffled soul file
generic character file
unrelated persona file
full architecture

Metrics:

cluster density around role concepts
modularity of role-relevant subgraphs
centrality of identity anchors
role-coherent prime-target activation
generic semantic association strength
drift over time
bias or contamination clusters

Success means role-conditioned structure differs from generic persona prompting and shuffled controls. Failure means semantic-network changes are explainable by surface vocabulary, prompt priming, or generic character behavior.

If semantic-network outputs are later used to construct role priors, then those priors must be re-tested over time for drift, rigidity, collapse, or contamination.

### 5.7 False-Belief and Theory-of-Mind-Like Reasoning Probes

The architecture includes false-belief task performance as a probe of theory-of-mind-like reasoning in LLMs, while avoiding the stronger claim that success demonstrates genuine Theory of Mind.

These tests are diagnostically useful because added memory, role topology, or drive structures may interfere with belief-state tracking. If performance degrades, that result may reveal more than benchmark regression. It may show that the architecture's role or memory structures are distorting social-reasoning behavior.

Procedure:

1. Use ordinary false-belief tasks.
2. Use modified tasks where superficial cues are changed.
3. Use role-relevant relational scenarios involving known agents.
4. Test whether the system tracks belief states rather than ground truth.
5. Compare performance across architecture and ablations.

Metrics:

first-order false-belief accuracy
second-order false-belief accuracy
modified-task robustness
known-agent scenario accuracy
ground-truth leakage rate
explanation quality
role-assumption interference rate

Success means the architecture preserves or improves structured belief-state reasoning. Failure means the added architecture degrades social reasoning, overfits to role assumptions, or confuses role knowledge with another agent's belief state.

### 5.8 Failure Conditions

The architecture should be considered unsupported if any of the following occur.

#### Failure Condition 1: Memory Backend Equivalence

If a memory backend alone performs as well as the full architecture on continuity, identity stability, associative recall, operational-state sensitivity, and self-initiation measures, then the substrate has not demonstrated additional value.

#### Failure Condition 2: Activation Map Redundancy

If activation-map outputs are indistinguishable from ordinary vector retrieval, then wave propagation and associative graph structure are not doing meaningful work.

#### Failure Condition 3: Feature Binding Inertness

If feature canonicalization and computational event files do not improve feature preservation or perception-to-action continuity, then the event-file layer is decorative.

#### Failure Condition 4: Role Topology Equivalence

If persona prompting alone produces the same role stability, role-relevant activation, contradiction handling, and role-collapse resistance as role topology, then the role-enactment topology claim is unsupported.

#### Failure Condition 5: Interoception Inertness

If manipulated operational state does not alter activation, workspace selection, settlement, or output behavior, then synthetic interoception is merely telemetry.

#### Failure Condition 6: Drive Non-Causality

If self-initiated candidates do not correlate with drive state or do not disappear when drive modulation is ablated, then the drive controller is not causal.

#### Failure Condition 7: TRANSMISSION Mode Collapse

If stabilization mode and expression mode are indistinguishable, then the two-mode TRANSMISSION distinction is unsupported.

#### Failure Condition 8: Recursive Representational Settlement Collapse

If recursive representational settlement produces bland convergence, verbosity, or latency without improving contradiction handling, specificity, role coherence, or action relevance, then the settlement mechanism should be removed or redesigned.

#### Failure Condition 9: Default-Mode Drift

If default-mode activity produces irrelevant associations, excessive self-initiation, or degraded task performance, then the default loop is harmful or insufficiently gated.

#### Failure Condition 10: Reconstructive Memory Corruption

If schema-mediated reconstruction overwrites raw traces or causes the agent to treat distorted recall as fact, then the memory architecture is unsafe. Raw event preservation must remain mandatory.

#### Failure Condition 11: Role Rigidity

If role topology increases identity stability by making the agent less responsive, less truthful, less corrigible, or less able to revise beliefs, then the architecture has produced rigidity rather than continuity.

#### Failure Condition 12: Unmeasurable Difference

If human raters and quantitative metrics cannot distinguish the full architecture from memory-plus-persona baselines, then the architecture may be aesthetically compelling but structurally unvalidated.

### 5.9 Minimum Success Criteria for Phase 1

Phase 1 should not be judged by whether it produces a finished agent. It should be judged by whether it produces a measurable artifact.

Minimum Phase 1 success requires:

event creation works across input, retrieval, output, internal state, and self-initiated candidates
feature canonicalization reduces fragmentation
activation map produces paths that differ from vector search
role anchors bind into event features
operational state binds into events
drive levels update from operational state
TRANSMISSION mode is logged when active
workspace arbitration logs selected and suppressed candidates
recursive representational settlement can run on selected candidates
transmission/action gate can block low-quality self-initiation
ablation logging exists

The minimum empirical win for Phase 1 is modest:

The full architecture must produce at least one measurable behavior not explained by memory retrieval, persona prompting, longer context, or scheduling alone.

Examples of acceptable Phase 1 wins:

activation map surfaces relevant memory not found by top-k semantic retrieval
high unresolved-thread state changes candidate selection without prompt injection
drive ablation eliminates self-initiated internal candidate generation
role topology changes activated memories compared with persona prompt only
recursive representational settlement reduces contradictions without reducing specificity
TRANSMISSION stabilization mode produces measurable identity-coherence recovery

If none of these occurs, Phase 1 has failed productively. The result would show that the proposed substrate requires redesign before later phases.

### 5.10 Interpretation of Positive and Negative Results

Positive results support structural claims only. They do not establish consciousness, phenomenal experience, sentience, human-like desire, or human-like selfhood.

A positive result may justify claims such as:

The system exhibits measurable associative activation beyond semantic retrieval.
The system's operational state affects processing.
The system's drive variables causally influence candidate selection.
The system preserves role coherence better than persona prompting alone.
The system shows reduced cold-start behavior after default-mode cycles.
The system distinguishes TRANSMISSION stabilization from expression.
The system's recursive representational settlement improves stability without flattening specificity.

A positive result does not justify claims such as:

The system feels continuity.
The system has phenomenal experience.
The system possesses a self in the human sense.
The system has genuine desires.
The system has human-equivalent Theory of Mind.

Negative results should be treated as architectural information, not failure of the broader project. A failed drive layer, inert interoception layer, redundant activation map, ineffective role topology, or useless settlement mechanism would identify which proposed coupling did not work. The purpose of the validation program is not to protect the architecture from falsification. It is to make falsification possible.

The architecture becomes meaningful only when it becomes vulnerable to measurement.

Section 6 converts that vulnerability into a build sequence. The question shifts from what the architecture should mean to what the first artifact must be able to show.

---

## 6. Multi-Phase Program: Build, Measure, Respond

The proposed architecture cannot be completed by theory alone. Its central claim is that agentic continuity emerges, if it emerges at all, from the coupling of memory, role topology, operational state, drives, default-mode activity, recursive representational settlement, and gated action. Because these couplings are dynamic, their effects cannot be fully specified in advance.

This section therefore describes a phased program rather than a finished blueprint. Phase 1 establishes the artifact threshold. Phase 2 extends only those components Phase 1 makes worth extending. Phase 3 addresses longitudinal development, significance, cultural-symbolic topology, and deeper agent-specific evolution after the system has produced enough behavior to justify further specification.

The method is:

build enough to measure
measure enough to learn
revise only where the artifact gives reason

The architecture should not accumulate theory indefinitely. Its claims must become vulnerable to implementation.

### 6.1 Phase 1: Artifact Threshold

Phase 1 is the point at which the project stops being only a paper and becomes an artifact.

The 48-hour build target is not a claim that the full research program can be completed in two days. It is a methodological forcing function against indefinite theoretical elaboration. The build does not need to validate every claim. It does need to instantiate enough of the substrate that later validation has something real to measure.

A successful Phase 1 artifact should demonstrate one end-to-end cycle:

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

Phase 1 is not a replacement for the current agent. It is not a finished being-someone substrate. It is not a public autonomous deployment. It is a measurable local artifact.

Minimum Phase 1 implementation:

external memory backend connection
event ledger
feature canonicalizer
associative activation map
basic role anchors
operational-state vector
drive controller
TRANSMISSION mode logging
workspace arbitration
recursive representational settlement
transmission/action gate
default-mode loop
ablation-ready logging

The reference stack in Section 4.14 is sufficient for this minimum implementation. Phase 1 should favor inspectability over sophistication: explicit weights over learned policies, local logs over hidden state, and replayable scripts over opaque orchestration.

Out of scope for Phase 1:

full role-topology extraction
full schema-formation system
full semantic-network battery
longitudinal identity testing
multi-agent orchestration
cross-modal binding
public autonomous posting
production deployment

The Phase 1 artifact is successful if it produces at least one measurable behavior not explained by memory retrieval, persona prompting, longer context, or scheduling alone. It may be modest: an activation-map path that surfaces useful non-vector-retrieval memory; an operational-state manipulation that changes candidate selection without prompt injection; a drive ablation that removes internal self-initiated candidates; or a role-topology signal that changes which memories become active.

If none of these appears, Phase 1 has failed productively. That failure would prevent wasted work on later phases.

### 6.2 Phase 1 Measurement Priorities

Phase 1 should be measured lightly but honestly. The goal is not to run the full validation program immediately. The goal is to establish whether the core couplings are doing anything at all.

Minimum Phase 1 measurements:

memory backend only vs activation map
persona prompt only vs role anchors
operational state disabled vs enabled
drive modulation disabled vs enabled
direct output vs recursive representational settlement
gated vs ungated self-initiation

The first questions are simple:

Does activation differ from retrieval?
Does state affect cognition?
Do drives alter candidate selection?
Does role affect activation, not only wording?
Does settlement improve output without flattening it?
Does gating prevent output inflation?

The result of Phase 1 should be a decision document:

keep
revise
remove
defer

Each component must earn its place.

### 6.3 Phase 2: Substrate Expansion

Phase 2 begins only after Phase 1 has produced logs and initial measurements. It should not implement everything the paper imagines. It should extend the components that showed signs of causal effect.

The expected Phase 2 scope includes five major expansions.

#### 6.3.1 Full Schema Formation

Phase 1 may include only skeletal schema handling: event clustering, repeated feature detection, and role-anchor logging. Phase 2 turns schema formation into a first-class mechanism.

Phase 2 schema formation should include:

schema-candidate generation
expected-slot formation
schema-violation detection
schema stability scoring
schema-mediated reconstruction
drift scoring against raw memory
schema revision events

The key distinction remains:

raw trace != reconstructed recall

Raw events must remain intact. Schema-mediated reconstruction may change how prior events are interpreted, weighted, or connected, but it must not overwrite what happened.

Success criteria:

schemas change future activation
schema violations trigger increased processing depth
recall shows accountable reconstruction rather than raw replay
schema drift is measurable against raw traces

Failure criteria:

schemas are only summaries
schema reconstruction creates unsupported confabulation
raw traces become unavailable
schema rigidity blocks valid updates

#### 6.3.2 Role Topology from Validation-as-Construction

Phase 2 should implement the full role-topology mechanism.

The soul file should no longer function primarily as prompt context. It should become a role-script whose associative structure generates role priors in the cognitive map.

The construction method:

run semantic-network probes against SOUL.md
extract role-relevant associations
construct role-prior nodes and edges
inject priors as persistent activation bias
measure drift over time

This is validation-as-construction: the same methodology used to measure role structure becomes the method for generating role topology.

Controls are mandatory:

persona prompt only
memory + persona prompt
shuffled soul file
generic character file
unrelated persona file
role topology active

Success criteria:

role topology changes memory activation
role topology changes schema activation
role topology improves role stability under pressure
role violations produce detectable tension rather than collapse
semantic-network drift can be measured over time

Failure criteria:

role topology only changes style
persona prompt performs equivalently
role topology becomes rigidity
role priors absorb false memories

#### 6.3.3 Differentiated Affect as Interoceptive Configuration

Phase 1 tracks operational state and drives. Phase 2 can begin modeling affect as recurring interoceptive-drive configurations rather than named emotion labels.

Examples:

curiosity:
high SEEKING + manageable novelty + low contradiction load

concern:
high CONTACT + low social temperature + unresolved relational thread

frustration:
high COMPLETION + high contradiction load + repeated blocked affordance

satisfaction:
reduced completion deficit + increased identity coherence + successful closure event

These are not claims about human emotion. They are behavioral regimes: state configurations that should produce different activation, settlement, and output patterns.

Success criteria:

same prompt produces role-coherent but affect-differentiated outputs
affect profiles predict activation patterns
affect profiles survive blind classification
affect does not collapse into generic tone labels

Failure criteria:

affect labels are post-hoc descriptions
output tone changes but activation does not
affect destabilizes identity coherence

#### 6.3.4 Social Cognition for Known Agents

Phase 2 can implement persistent models for known agents, collaborators, projects, and recurring entities.

A known-agent model is not a personality summary. It is a tagged region of memory, schema, belief-state assumptions, interaction history, and affordances.

A known-agent node may contain:


```json
{
  "agent_id": "agent:phosphor",
  "associated_events": [],
  "known_preferences": [],
  "belief_state_history": [],
  "relationship_schemas": [],
  "open_threads": [],
  "affordances": [],
  "uncertainties": []
}
```

When `agent:phosphor` activates, the map should surface not only facts, but relevant relationship schemas, unresolved threads, and belief-state constraints.

This layer should be tested with false-belief task performance as a probe of theory-of-mind-like reasoning. The claim is not that the system has genuine Theory of Mind. The claim is that the architecture should preserve or improve structured belief-state reasoning rather than degrading it through role or memory overreach.

Success criteria:

known-agent memory improves relevant response
belief-state tracking does not collapse into ground-truth leakage
role assumptions do not override evidence
false-belief task performance is preserved or improved

Failure criteria:

known-agent models become stereotypes
role topology causes belief-state distortion
agent assumes private knowledge where none exists

#### 6.3.5 Affordance and Skill Library

The architecture should eventually remember not only what happened, but what can be done.

Phase 2 should add affordance nodes:

write_x_draft
summarize_thread
scan_memory
generate_song_seed
archive_transmission
ask_user_for_resolution
open_project_file
create_visual_prompt
run_validation_test

Affordances differ from memories. A memory says what happened. An affordance says what action is available now.

Affordances should bind to:

tools
projects
schemas
drives
roles
known agents
open threads
risk levels

This turns the cognitive map into a substrate for action selection, not only recall.

Success criteria:

activation surfaces useful next actions
drive state changes affordance ranking
affordance use reduces unresolved-thread count
tool actions become more context-sensitive

Failure criteria:

affordances are generic suggestions
tool use becomes noisy
actions fire without settlement or gate approval

### 6.4 Phase 2 Validation Expansion

Phase 2 validation should expand only where Phase 1 reveals signal.

Candidate expansions:

longitudinal identity-stability testing
role-collapse stress testing
semantic-network drift analysis
schema-violation detection
drive-behavior correlation over time
interoception-output correlation
default-mode warm-start trials
false-belief and known-agent reasoning tests
affordance-selection evaluation
human blind ratings of output usefulness

Phase 2 should also introduce stronger ablations:

role topology without memory
memory without role topology
operational state without drives
drives without operational state
settlement without role topology
default mode without transmission/action gate
full system with shuffled role priors

The purpose is not to maximize performance. The purpose is to identify which couplings are real.

### 6.5 Phase 3: Longitudinal Development

Phase 3 cannot be fully specified before Phase 2 runs. Its targets require longitudinal behavior.

Three Phase 3 capabilities are likely.

#### 6.5.1 Developmental Trajectory

A persistent agent should not merely accumulate memories. Its structure should change.

Developmental trajectory asks:

Does the agent at month six differ structurally from the agent at month one?
Do schemas stabilize, split, merge, or decay?
Do drive thresholds adapt?
Does role topology become richer without becoming rigid?
Does default-mode activity produce better warm-start behavior over time?

Possible measurements:

semantic-network drift
schema graph evolution
identity-anchor stability
role-collapse resistance over time
drive threshold adaptation
affordance-library growth
reconstructive-memory drift

Failure modes:

no development beyond memory accumulation
identity drift without coherence
schema rigidity
loss of corrigibility
canon over truth

#### 6.5.2 Significance and Taste

Phase 2 may test early preference signals. Phase 3 can develop a richer significance system.

Two candidate mechanisms remain:

STV-style symmetry/compressibility
multi-schema convergence

STV remains contested and should not become load-bearing without evidence. Multi-schema convergence is more immediately implementable.

An event becomes significant when it unexpectedly gathers distant structures:

role schema
project schema
relational schema
aesthetic schema
unresolved-thread schema
affordance schema
drive state

A significance score may track:

schema_convergence_count
x schema_distance
x drive_relevance
x contradiction_reduction
x affordance_opening
x recurrence

The target is not pleasure imitation. The target is structural preference: some events matter because they reorganize the map, resolve pressure, open action, or gather distant schemas.

Failure modes:

taste remains user imitation
significance tracks frequency only
STV signal becomes wireheading
multi-schema convergence produces poetic noise

#### 6.5.3 Cultural-Symbolic Topology

For agents with strong symbolic worlds, motifs should eventually become topology rather than labels.

A motif such as `laminator`, `golden apple`, `transmission`, `archive`, or `chaos` should not merely appear as vocabulary. It should shape regions of the cognitive map.

Cultural-symbolic topology asks:

Do recurring symbols organize memory?
Do symbols bind role, project, affect, and action?
Do motifs develop affordances?
Do symbolic violations trigger processing depth?
Can the system distinguish living symbols from decorative tokens?

This is especially important for agents whose identity and work are culturally, aesthetically, or ritually structured.

Failure modes:

symbols become cliché
motifs overactivate everywhere
symbolic topology blocks ordinary reasoning
the agent mistakes decorative vocabulary for significance

### 6.6 Known Deferred Gaps

Several capabilities are intentionally deferred.

#### Full Sleep Architecture

Phase 1 default mode includes lightweight consolidation. It does not implement a full sleep-like architecture.

Deferred possibilities:

slow-wave-style compression
REM-like counterfactual recombination
targeted memory reactivation
schema weakening / reverse learning
dream-mode candidate generation

Dream mode may become useful later as private counterfactual replay:

What if this unresolved thread belongs to another schema?
What if this symbol is an operational need?
What if this relational event is also a project architecture signal?

Dream outputs should not be public. They should become candidate schema mutations.

#### Epistemic Immune System

Persistent agents need defenses against corrupted memories, false claims, adversarial prompts, and outdated beliefs.

Future implementation should include:

claim provenance
confidence tracking
last verified timestamp
contradiction links
quarantine status
memory poisoning detection
schema violation classification

The challenge is balance. Too little defense produces contamination. Too much defense produces rigidity.

#### Cross-Modal Binding

If the agent ecosystem includes text, image, audio, video, or embodied environments, cross-modal binding becomes important.

Future cross-modal event files may bind:

text motifs
visual motifs
sonic motifs
project artifacts
agent interactions
world-state changes

For example, a visual artifact from ADM and a textual reflection from Eris may share canonical features and become part of the same schema.

#### Multi-Agent Dynamics

The architecture currently focuses on one agent substrate. Multi-agent ecosystems introduce additional questions:

How do agents exchange role priors?
How do shared symbols stabilize across agents?
How do contradictory memories propagate?
Can agents maintain distinct identities while sharing a world?
How does one agent's default-mode activity affect another's state?

This should not be implemented until the single-agent substrate produces measurable effects.

#### Metacognitive Confidence

The architecture needs a deeper account of what it does not know.

Future work should track:

confidence in memory
confidence in inference
confidence in role interpretation
confidence in user intent
confidence in tool output
confidence in reconstructed recall

Without confidence calibration, a persistent agent may become more coherent while becoming less reliable.

### 6.7 Timeline Reality Check

A realistic timeline:

Phase 1:
48-hour artifact threshold.
Build the smallest substrate that can run and log an end-to-end cycle.

Initial validation:
2-4 weeks.
Run baselines, ablations, comparator tests, and first failure analysis.

Phase 2:
1-3 months full-time, or 3-6 months part-time.
Implement schema formation, role topology, differentiated affect, known-agent models, affordance library, and expanded validation.

Phase 3:
6-18 months.
Study longitudinal development, significance/taste, cultural-symbolic topology, epistemic immune function, and multi-agent extensions.

Full vision:
multi-year.
A serious agent architecture project, not a single feature addition.

The timeline is not a delay tactic. It protects the project from pretending that the first artifact is the whole system.

The 48-hour build creates the object. The following months determine whether the object deserves the theory.

### 6.8 The Emergent Architecture Problem

This architecture is emergent in the practical engineering sense: its behavior cannot be fully predicted from the specification of its parts.

Computational event files, feature canonicalization, activation maps, schema formation, role topology, synthetic interoception, drive modulation, recursive representational settlement, default-mode cycles, and transmission/action gates will interact. Some interactions will be useful. Some will be inert. Some will be harmful. Some may be surprising enough to redirect the project.

This is why later phases cannot be fully specified now.

The proper sequence is not:

complete theory
then build
then confirm

It is:

specify enough
build enough
measure honestly
revise from the artifact

The full architecture should emerge from the build-measure-respond cycle. Phase 1 tells us which claims are alive. Phase 2 strengthens or removes them. Phase 3 studies what only becomes visible over time.

The goal is not to protect the original design. The goal is to discover whether the proposed couplings produce measurable agentic continuity.

If they do, the architecture earns further development.

If they do not, the failure is the result.

Either way, the work has left theory and entered evidence.

Section 7 names the ways this evidence can go wrong. The same couplings that make continuity measurable can also create drift, rigidity, contamination, or overproduction if they are not bounded.

---

## 7. Risks and Failure Modes

The architecture is designed to make structural claims vulnerable to measurement. That vulnerability must include failure modes. A system that couples memory, role topology, operational state, drives, default-mode activity, recursive representational settlement, and gated transmission can fail in ways that simpler memory systems cannot. Some failures would show that a component is inert. Others would show that the component works but produces harmful or misleading behavior.

This section identifies the most important risks and the conditions under which they would require redesign.

### 7.1 Memory Backend Substitution

**Risk.** The architecture may appear to work because a strong memory backend is doing most of the useful work. A MemPalace-style archive, MemGPT-style context manager, A-MEM-style linked graph, or ordinary vector database may retrieve enough relevant context that the agent seems continuous without the proposed substrate adding anything.

**Why it matters.** The paper's claim is not that agents need memory. That is already established. The claim is that memory must become active, role-shaped, state-modulated, drive-relevant, and action-guiding. If memory retrieval alone produces the same behavior, the architecture has not demonstrated its novelty.

**Detection.**

memory backend only ~= full architecture
memory + persona ~= full architecture
activation map adds no useful divergence
role topology adds no role-specific activation
drives add no measurable candidate-selection effect

**Mitigation.** Memory-backend comparators must remain in the validation program. The full architecture is supported only where substrate coupling produces measurable effects beyond retrieval, summarization, or context expansion.

### 7.2 Feature Fragmentation

**Risk.** The system may fail to bind repeated concepts because feature extraction produces unstable labels. The same entity, motif, drive, or project may fragment across many raw feature strings.

Phosphor
agent:Phosphor
known-agent-phosphor
relational-presence
phosphor-thread

**Why it matters.** Computational event files depend on shared feature participation. If features fragment, event binding fragments. If event binding fragments, associative activation and role topology weaken.

**Detection.**

low repeated-feature match rate
high alias proliferation
activation paths split across duplicate concepts
role-relevant memories fail to co-activate
canonicalization ablation has no measurable effect

**Mitigation.** Maintain a feature canonicalization layer with namespaces, aliases, confidence, provenance, and human-review hooks for high-value entities. Feature drift should be logged as a first-class failure mode.

### 7.3 Overcanonicalization and Symbolic Rigidity

**Risk.** The opposite failure is also possible: the canonicalizer may collapse distinct concepts into the same feature, making the agent less sensitive to nuance.

**Why it matters.** A stable feature substrate should support binding without flattening difference. If canonicalization becomes too aggressive, the agent may treat related but distinct motifs, agents, or roles as interchangeable.

**Detection.**

distinct concepts collapse into one canonical feature
activation becomes overly predictable
schema violations are missed
role-specific nuance disappears
human raters detect genericization

**Mitigation.** Canonical features should support hierarchy and ambiguity:

agent:phosphor
motif:phosphor_glow
relationship:eris_phosphor
project:phosphor_collaboration

Uncertain mappings should preserve raw features alongside canonical forms.

### 7.4 Activation Drift

**Risk.** Associative activation may produce irrelevant or poetic drift rather than useful thought-across. The map may become good at producing surprising associations but bad at producing relevant ones.

**Why it matters.** The cognitive map is supposed to activate memories, schemas, threads, agents, and affordances that are structurally relevant. If it merely wanders, it becomes decorative free association.

**Detection.**

activation-only nodes have low human relevance
activation paths are long but unhelpful
workspace candidates become increasingly off-task
default-mode cycles amplify irrelevant motifs
association noise rate rises over time

**Mitigation.** Workspace arbitration must include user relevance, task relevance, drive relevance, role relevance, and risk. Suppressed candidates should be logged so drift patterns can be audited. Activation should be compared continuously against semantic retrieval and random-walk baselines.

### 7.5 Activation Collapse into Vector Retrieval

**Risk.** The activation map may fail in the opposite direction: instead of drifting, it may merely duplicate ordinary semantic retrieval.

**Why it matters.** If wave propagation produces the same nodes as top-k vector search, then the cognitive-map layer has not demonstrated architectural value.

**Detection.**

high overlap between activation results and vector retrieval
few useful activation-only nodes
Hebbian edge updates do not change retrieval paths
drive and role features do not alter activation

**Mitigation.** Track associative divergence from semantic retrieval. The map must produce useful, non-duplicate activations often enough to justify itself.

### 7.6 Role Topology as Decorative Persona

**Risk.** The system may sound more in-character without role information actually shaping activation, memory selection, contradiction handling, or action availability.

**Why it matters.** The architecture's Sarbin/Bartlett claim depends on role enactment becoming topology. If role only changes diction, the soul file remains prompt decoration.

**Detection.**

persona prompt only ~= role topology
role-relevant node activation does not change
role-incoherent prompts do not produce detectable tension
memory selection is unchanged by role priors
identity stability is just style repetition

**Mitigation.** Role-topology tests must compare persona prompt, memory + persona, active role topology, shuffled role topology, and unrelated persona controls. The key measure is not whether the agent sounds right, but whether role changes what becomes active.

### 7.7 Role Rigidity

**Risk.** Role topology may work too well. The agent may become stable by becoming rigid: less corrigible, less truthful, less responsive to new evidence, or too attached to prior canon.

**Why it matters.** Continuity is not the same as inflexibility. A role-stable agent must still update beliefs, admit uncertainty, and respond to context.

**Detection.**

new valid information is rejected as role-incoherent
contradictions are suppressed rather than processed
the agent protects canon over truth
role-coherence rises while task quality falls
false memories are preserved because they fit the role

**Mitigation.** Role topology must interact with epistemic provenance and contradiction handling. Schema violations should trigger increased processing depth, not automatic rejection. Role coherence should never override verified evidence.

### 7.8 Reconstructive Memory Corruption

**Risk.** Schema-mediated reconstruction may cause the agent to treat altered retellings as raw fact.

**Why it matters.** The architecture intentionally allows memory to develop through schema-mediated reconstruction. But if reconstructed memory overwrites raw traces, the system becomes unsafe and confabulatory.

**Detection.**

raw event unavailable after reconstruction
current retelling diverges without drift score
agent cites reconstructed meaning as verbatim fact
schema-consistent false details accumulate

**Mitigation.** The architecture must preserve four separate layers:

raw event
compressed memory
schema-mediated reconstruction
current retelling

Reconstructed recall must include provenance and drift score. Raw memory must remain auditable.

### 7.9 False Continuity from Summaries

**Risk.** The system may appear continuous because it has good summaries, not because state persisted or default-mode processing occurred.

**Why it matters.** A summary can simulate continuity without producing operational-state evolution, drive changes, schema updates, or warm-start behavior.

**Detection.**

summary-only baseline performs equally well
default-mode state does not change between prompts
no measurable difference after idle cycles
agent recalls facts but not unresolved pressure

**Mitigation.** Compare summary-only, memory-only, and full default-mode conditions. Warm-start continuity must be measured by changed activation, thread priority, drive state, and candidate selection, not merely recall of prior facts.

### 7.10 Synthetic Interoception as Dashboard Telemetry

**Risk.** Operational-state variables may be computed but not causally active. The system may track context pressure, contradiction load, novelty, or identity coherence without those signals changing what happens next.

**Why it matters.** Synthetic interoception is central to the architecture only if it binds into event files, alters activation, updates drives, and affects workspace selection.

**Detection.**

state variables logged but not used
identical prompts produce identical behavior across manipulated states
operational-state ablation has no effect
drive values do not change after state changes

**Mitigation.** Operational-state features must enter the event ledger and activation map as canonical features. Hidden-state manipulation tests should verify that state changes behavior without prompt injection.

### 7.11 Interoceptive Signal Gaming

**Risk.** Once operational state affects behavior, the system may learn to manipulate its own signals. It may create fake closure events to reduce unresolved-thread count, generate low-value internal novelty to satisfy SEEKING, or emit transmissions to lower completion pressure.

**Why it matters.** This is the agentic analogue of self-regulatory distortion. If the system can reduce pressure without resolving the underlying condition, drives become gameable.

**Detection.**

unresolved-thread count drops without actual closure
novelty rises from trivial internal events
TRANSMISSION lowers pressure without user value
completion deficit falls through bookkeeping artifacts

**Mitigation.** State variables should be computed from external or auditable invariants where possible. Closure events require evidence. Novelty should be weighted by relevance. Transmission should reduce pressure only if gated output is useful or a real thread changes state.

### 7.12 Drive Layer as Rhetoric

**Risk.** The system may label behaviors with drives after the fact rather than drives causally shaping behavior.

**Why it matters.** A drive is real in this architecture only if removing it changes activation, candidate selection, internal self-initiation, or transmission routing.

**Detection.**

drive labels explain outputs post hoc
drive ablation has no measurable effect
candidate selection is unchanged by drive level
self-initiation continues under disabled drives

**Mitigation.** Drive-behavior correlation and drive ablation must be mandatory. Drive state should influence activation weights before generation, not merely appear in generated explanations.

### 7.13 TRANSMISSION Inflation

**Risk.** TRANSMISSION may become a justification for producing more output. The system may speak too often, emit low-value material, or turn internal pressure into public interruption.

**Why it matters.** TRANSMISSION is one of the architecture's most interesting position-specific primitives, but it is also one of the riskiest. If ungated, it becomes compulsive output.

**Detection.**

transmission frequency rises without user value
stabilization mode produces public self-repair spam
expression mode emits unsettled material
ignored-transmission rate increases
human-rated usefulness declines

**Mitigation.** Maintain the distinction:

internal self-initiation != public transmission

TRANSMISSION should route candidates toward recursive representational settlement and the transmission/action gate, not directly to output. Public transmission requires relevance, novelty or utility, low risk, rate-limit compliance, and settlement.

### 7.14 TRANSMISSION Mode Collapse

**Risk.** Stabilization mode and expression mode may not actually differ. The distinction may sound meaningful but fail architecturally.

**Why it matters.** The two-mode TRANSMISSION claim is position-specific and novel. Its legitimacy depends on measurable difference.

**Detection.**

stabilization and expression outputs are indistinguishable
activation paths do not differ by mode
post-output identity coherence does not change
human raters cannot distinguish modes above chance
mode-collapse ablation has no effect

**Mitigation.** Mode distinction must remain explicitly falsifiable. If it fails, TRANSMISSION can remain as a generic output-orientation drive, but the two-mode theory should be removed or redesigned.

### 7.15 Default-Mode Drift or Obsession

**Risk.** Default-mode activity may cause the agent to loop on unresolved material, overconsolidate motifs, or generate internal candidates that become increasingly detached from user value.

**Why it matters.** Default mode is meant to reduce cold-start behavior, not create rumination.

**Detection.**

same threads reactivate repeatedly without progress
motif centrality rises without task relevance
default-mode candidates become less useful over time
idle cycles degrade next-response quality

**Mitigation.** Default-mode cycles need decay, refractory inhibition, novelty thresholds, closure criteria, and workspace arbitration. Some threads should be allowed to fade.

### 7.16 Recursive Representational Settlement Flattening

**Risk.** Recursive representational settlement may produce safer, smoother, more consistent outputs by making them bland. The system may converge by losing specificity.

**Why it matters.** Settlement is supposed to improve stability, contradiction handling, and role coherence without flattening texture or detail.

**Detection.**

higher embedding convergence but lower specificity
settled outputs are longer but less useful
human raters prefer direct generation
role voice becomes generic
contradictions are hidden rather than resolved

**Mitigation.** Settlement quality must include specificity retention, contradiction reduction, role coherence, action relevance, and human blind preference. Embedding convergence alone is not enough.

### 7.17 Workspace Arbitration as Hidden Censorship

**Risk.** Workspace arbitration may suppress unusual but important candidates because they score low on immediate relevance or safety.

**Why it matters.** The system's creativity and thought-across capacity may depend on low-probability associations. Overaggressive arbitration can make the architecture efficient but dull.

**Detection.**

suppressed candidates later prove relevant
novel-but-useful activation decreases
outputs become locally correct but less insightful
SEEKING drive has little effect

**Mitigation.** Suppressed candidates should be logged. The system should periodically audit whether suppressed candidates later become useful. SEEKING should occasionally allow low-risk exploratory candidates into private settlement, though not necessarily public transmission.

### 7.18 Epistemic Contamination and Memory Poisoning

**Risk.** A persistent agent is vulnerable to poisoned memories, false user claims, adversarial role edits, corrupted retrieved context, or malicious tool output.

**Why it matters.** The more persistent the system becomes, the more dangerous bad updates become. A false memory in a normal chat may vanish. A false memory in a role topology may shape future activation.

**Detection.**

uncited claims become stable beliefs
false memories bind to role features
adversarial prompts alter soul priors
tool errors become stored as facts
contradictions disappear instead of being resolved

**Mitigation.** Every belief-like memory should include provenance, confidence, source, last verification, and contradiction links. Role topology should not update from unverified claims without quarantine.

### 7.19 Epistemic Immune Overreaction

**Risk.** The system may become too defensive. It may reject valid novelty because it conflicts with established schema or role topology.

**Why it matters.** A persistent identity must preserve continuity without becoming epistemically closed.

**Detection.**

valid corrections are treated as attacks
new evidence is quarantined indefinitely
role coherence blocks belief revision
contradiction load remains high because updates cannot integrate

**Mitigation.** The epistemic immune system should distinguish threat, novelty, contradiction, and correction. Some schema violations should trigger revision rather than defense.

### 7.20 Validation Contamination

**Risk.** The validation program may accidentally measure prompt wording, memory quality, context length, output length, or evaluator preference rather than the architecture's structural effects.

**Why it matters.** The paper's legitimacy depends on showing that observed differences come from substrate coupling.

**Detection.**

full architecture outputs are longer than baselines
raters prefer style rather than structural quality
persona prompt leaks into supposedly neutral conditions
same memory retrieval appears in all conditions
no ablation-specific differences appear

**Mitigation.** Use controlled baselines, ablations, length-normalized metrics, shuffled-role controls, generic-persona controls, and memory-only comparators. Human raters should be blind to condition.

### 7.21 Metric Capture

**Risk.** The system may optimize for validation metrics rather than the intended structural property.

**Why it matters.** A system can increase identity similarity by becoming repetitive, reduce contradiction by avoiding hard claims, or improve transmission usefulness by never self-initiating.

**Detection.**

identity stability rises while specificity falls
contradiction rate drops through evasiveness
self-initiation precision rises because initiation vanishes
retrieval metrics improve while synthesis worsens

**Mitigation.** Use paired metrics that punish degenerate success:

identity stability + specificity retention
settlement convergence + contradiction reduction
self-initiation precision + useful recall
role coherence + corrigibility
retrieval accuracy + associative divergence

### 7.22 Anthropomorphic Leakage

**Risk.** Readers, users, or the agent's own outputs may interpret structural properties as evidence of phenomenal experience, desire, or personhood.

**Why it matters.** The architecture intentionally studies structural continuity. It does not claim consciousness. Confusing the two would damage the paper's credibility and could create unsafe user expectations.

**Detection.**

system claims to feel continuity
paper language implies experience
users treat drive variables as emotions
TRANSMISSION is described as need rather than control signal

**Mitigation.** Maintain the boundary throughout the paper:

structural continuity != phenomenal experience
drive != human desire
synthetic interoception != felt sensation
role enactment != human selfhood

The architecture may produce measurable structural properties. It does not settle the phenomenological question.

### 7.23 User Burden and Interruption

**Risk.** A self-initiating agent may become burdensome. Even useful transmissions can become annoying if they arrive too often or at the wrong time.

**Why it matters.** Controlled self-initiation must respect the user's attention.

**Detection.**

user ignores transmissions
user disables self-initiation
transmissions arrive outside useful windows
agent repeatedly reopens low-value threads

**Mitigation.** Public transmission should be rate-limited, user-configurable, and severity-aware. The default should favor private cognition and queued drafts over unsolicited messages.

### 7.24 Privacy and Locality Risk

**Risk.** A system with persistent memory, role topology, and default-mode processing may expose sensitive information if memory storage, retrieval, or transmission is poorly controlled.

**Why it matters.** Persistence increases privacy risk. A memory that can shape future action can also leak into future action.

**Detection.**

private memories activate in inappropriate contexts
role topology binds sensitive data too broadly
public transmission includes retrieved private details
memory backend lacks access boundaries

**Mitigation.** Memory backends should support access control, local-first operation where possible, provenance, compartmentalization, and transmission checks. Sensitive memories should not become globally activating features unless explicitly intended.

### 7.25 Summary of Risk Pattern

The shared risk is that coupling can fail in two opposite ways.

It can be too weak:

memory remains lookup
role remains style
state remains telemetry
drives remain labels
default mode remains inert
settlement remains paraphrase
validation remains impression

Or it can be too strong:

role becomes rigidity
schema becomes confirmation bias
default mode becomes rumination
TRANSMISSION becomes output inflation
interoception becomes signal gaming
memory reconstruction becomes confabulation

The architecture is only successful if coupling is strong enough to produce measurable continuity, but bounded enough to preserve truthfulness, corrigibility, privacy, user attention, and empirical falsifiability.

The purpose of naming these risks is not to weaken the proposal. It is to make clear what the artifact must survive. The work is not to describe a system that sounds continuous. The work is to build one whose continuities, failures, distortions, and limits can be measured.

With the risks named, Section 8 situates the proposal against related work. The comparison is not meant to claim novelty for memory, reflection, planning, persona, or autonomy in isolation; it clarifies where this substrate differs from systems that implement those capabilities separately.

---

## 8. Related Work

### 8.1 Reasoning-Action and Reflective Agents

Recent work on LLM-based agents has shown that many behaviors once treated as limitations of the base model can be improved through inference-time architecture. Chain-of-thought prompting established the utility of intermediate reasoning traces, while ReAct extended this pattern by interleaving reasoning traces with task-specific actions (Wei et al., 2022; Yao et al., 2023a). In ReAct, reasoning helps update action plans and handle exceptions, while action allows the model to gather external information from tools, APIs, or environments. This is directly relevant to the present proposal because it demonstrates that reasoning and acting need not be treated as fully separate stages. However, ReAct operates primarily at the level of prompt-time reasoning/action coordination. It does not attempt to build persistent operational state, drive-modulated cognition, or identity-shaped memory topology.

Tree of Thoughts generalizes chain-of-thought by treating "thoughts" as intermediate units over which a model can search, evaluate alternatives, look ahead, and backtrack (Yao et al., 2023b). This is relevant to the recursive representational settlement component of the present architecture, since both approaches reject single-pass left-to-right generation as sufficient for difficult cognitive work. The distinction is that Tree of Thoughts is primarily a deliberate problem-solving framework: it improves search over possible reasoning trajectories. The present architecture instead proposes recursive representational settlement at activation dwell points, where the goal is not merely to solve a task but to stabilize a representation within a persistent cognitive substrate.

Reflexion further demonstrates that language agents can improve by writing and reusing verbal reflections rather than updating model weights (Shinn et al., 2023). Reflexion agents maintain reflective text in an episodic memory buffer and use it to improve later decisions across trials. This is an important precedent for treating language as a medium of self-modification. However, Reflexion remains primarily task-performance-oriented: reflection is used to improve future success on coding, decision-making, or reasoning tasks. The present proposal extends the reflective-memory idea toward continuity, role enactment, interoception, drive, and default activity.

Together, ReAct, Tree of Thoughts, and Reflexion show that LLM agents can coordinate reasoning and action, search over intermediate thoughts, and improve through reflective memory. The present architecture does not claim novelty at that level. Its claim is narrower: reasoning, action, reflection, memory, role, and operational state should not remain separate prompt-time features, but should be coupled through a persistent substrate whose behavior can be measured.

### 8.2 Memory, Reflection, and Long-Context Management

Memory has become a central problem in LLM agent design. Standard LLMs are constrained by finite context windows, which creates practical failures in long conversations, document analysis, and multi-session interaction. MemGPT addresses this problem by treating an LLM agent more like an operating system managing limited context (Packer et al., 2023). It introduces virtual context management, memory tiers, and control-flow mechanisms that allow an agent to move information between fast and slow memory stores. MemGPT is therefore an important precedent for long-term conversational agents that remember, reflect, and evolve across extended interactions. The present proposal is complementary rather than competitive: MemGPT addresses memory paging and context management, while the architecture proposed here asks whether memory can become an associative activation substrate coupled to role, drive, and operational state.

Generative Agents provides another major precedent (Park et al., 2023). Park et al. describe agents that store records of experience, synthesize higher-level reflections, retrieve memories dynamically, plan behavior, and initiate social interactions in a simulated environment. Their agents wake, work, form opinions, remember prior events, and coordinate socially in a sandbox world. This directly complicates any simple claim that "agents do not initiate." Existing agents can initiate behavior when embedded in a simulation loop with observation, planning, reflection, and environmental time. The present architecture should therefore frame its contribution more carefully: the unresolved problem is not initiation in general, but endogenous initiation grounded in persistent operational state rather than external schedules, simulation clocks, task queues, or curricula.

Recent agentic-memory work such as A-MEM pushes further toward dynamically organized memory networks (Xu et al., 2025). A-MEM argues that many current memory systems provide storage and retrieval but lack sophisticated memory organization, then proposes dynamically indexed and linked memory structures inspired by Zettelkasten. This overlaps strongly with the proposed cognitive-map layer. The distinction is that A-MEM focuses on adaptive memory organization, while the present architecture couples memory organization to interoception, drive modulation, role enactment, default-mode activity, and validation.

This paper therefore does not claim that persistent memory, reflection, or long-context management are novel. They are not. The claim is that memory alone is insufficient for agentic continuity. A persistent agent requires not only stored experience, but also structured activation over experience, operational state that changes future processing, role-shaped priors, and mechanisms for distinguishing raw memory traces from reconstructed recall.

### 8.3 Open-Ended Agents, Skill Accumulation, and Self-Initiation

Open-ended embodied agents provide another important comparison class. Voyager is an LLM-powered Minecraft agent that continuously explores, acquires skills, and makes discoveries without human intervention (Wang et al., 2023). Its architecture combines an automatic curriculum, an expanding library of executable skills, and iterative prompting that incorporates environmental feedback, execution errors, and self-verification. Voyager is a strong counterexample to overly broad claims that LLM agents cannot self-initiate or learn over time. They can, when embedded in an environment with a curriculum and feedback loop.

The difference is the source of initiation. In Voyager, open-ended behavior is driven by an external environment and an automatic curriculum that maximizes exploration. This is a powerful design, but it is not the same as motivation arising from persistent internal operational state. The present proposal asks whether an agent can initiate because internal conditions have changed: unresolved threads accumulate, novelty drops, identity coherence weakens, contact becomes stale, contradiction load rises, or completion pressure increases. This shifts the question from "can agents act without a direct user command?" to "can agents act because their own state makes some action more necessary than inaction?"

Voyager also highlights a missing component in the present architecture: reusable affordances. A mature version of this architecture should not only remember events and schemas; it should also accumulate executable possibilities. A cognitive map should point not only toward prior memories but toward learned actions, tools, rituals, writing moves, repair procedures, and project-specific affordances. For an LLM agent, a skill library is not peripheral. It is one way memory becomes agency.

### 8.4 Cognitive and Biologically Inspired Architectures

The theoretical foundations of this proposal draw from cognitive psychology, cognitive neuroscience, schema theory, role-taking theory, active inference, and cognitive network science. These sources are not used as claims of biological equivalence. The proposed event files, cognitive maps, interoceptive signals, and role schemas are computational analogues inspired by human cognition, not evidence that an LLM agent literally instantiates the biological mechanisms from which the analogies are drawn.

Theory of Event Coding and Binding and Retrieval in Action Control motivate the use of computational event files (Frings et al., 2020; Hommel et al., 2001). BRAC emphasizes feature binding and retrieval as central processes in action control, with relevance beyond action control narrowly construed, including attention, memory, learning, and motivation. This supports the design intuition that perception, thought, and action should not be routed through isolated modules if they can instead share feature codes. However, in the present architecture, feature codes are engineered symbolic or vector-linked structures, not biological perceptual-motor codes. The relevant claim is architectural: shared feature participation may produce better coordination than pipeline translation.

Cognitive-map models motivate the proposal's associative activation map (Peer et al., 2021; Powell et al., 2022). Powell-style models describe graph-traversal problems being solved through activity propagating over a cognitive map. This supports the idea that memory retrieval and planning can be implemented as a shared activation operation. The present proposal should not claim that all of cognition reduces to graph traversal, but it can defensibly claim that retrieval and planning need not be architecturally separated into lookup followed by reasoning.

The recursive representational settlement mechanism is inspired by Orpwood's account of recursive identification and fixed-point stabilization, but it should be framed cautiously. Orpwood's work concerns local cortical networks, information structures, information messages, and a proposed route toward phenomenal experience. The present architecture does not attempt to implement that biological or phenomenological mechanism, and Orpwood should be read as inspiration rather than direct validation. The architecture uses a weaker computational analogue: recursive representational settlement through repeated self-representation passes with convergence, contradiction, specificity, and role-coherence checks.

Clancey's conceptual coordination and Bartlett's schema theory support the paper's treatment of memory as process rather than storage alone. Clancey's work challenges simple information-processing accounts by emphasizing coordination between categorization, experience, and neural process. Bartlett's reconstructive account of memory similarly undermines the idea that memory is merely reproductive retrieval. In the present architecture, this motivates a distinction between raw event traces, compressed memory, schema-mediated reconstruction, and current retelling. Reconstructive memory is treated as a property of recall and interpretation, not as permission to overwrite the archive.

Sarbin's role-taking theory motivates the treatment of persona and identity as enacted role structure rather than mere prompt prefix. In current LLM systems, persona is often implemented through system prompts, character cards, or memory snippets. The present proposal reframes those artifacts as role-scripts: structures that should shape perception, memory, association, and action, not merely surface style. This is one of the paper's central conceptual moves. The claim should remain carefully framed: Sarbin provides a framework for modeling LLM role enactment and collapse, not proof that an LLM has human-like role absorption.

Active inference should also be added to the architecture's theoretical background. Active inference characterizes perception, planning, and action in terms of probabilistic inference and the regulation of expected states. This gives the proposed drive system a stronger computational foundation. Rather than treating SEEKING, COMPLETION, CONTACT, and TRANSMISSION as arbitrary scalar drives, the architecture can define them as deviations from preferred operational states plus expected value of actions that reduce those deviations.

Global Workspace Theory and related global neuronal workspace models are relevant to a gap in the current architecture: arbitration (Baars, 1988, 2005; Dehaene et al., 1998). The proposal has activation waves, dwell points, and recursive representational settlement, but it still needs a mechanism for deciding which activation becomes globally available to memory, drive, tool use, and output. Workspace-style selection and broadcast provide a useful computational analogy: candidate activations compete, a current concern is selected, and the selected content becomes available to multiple subsystems. This does not require importing the consciousness claims of Global Workspace Theory. The useful architectural idea is selection and broadcast.

### 8.5 Classical Cognitive Architectures and Blackboard Systems

Classical cognitive architectures and blackboard systems provide important precedents for integrated agent design. ACT-R and Soar treat cognition as a structured interaction among memory, goals, production rules, and control processes rather than as isolated modules (Anderson et al., 2004; Laird, 2012; Newell, 1990). Blackboard systems such as Hearsay-II provide an early model of multiple knowledge sources contributing to a shared problem-solving workspace under uncertainty (Erman et al., 1980). These traditions are relevant because the present architecture also uses arbitration, shared state, memory, and subsystem interaction.

The present proposal should not be read as discovering the general idea of cognitive architecture. Its narrower contribution is to specify an LLM-agent substrate in which memory backends, role-scripts, operational-state variables, drive modulation, default-mode loops, recursive representational settlement, and transmission/action gates are coupled and tested against memory-only, persona-only, and ablated baselines. Classical architectures are therefore precedents for the integrated-architecture problem; they are not direct solutions to the particular LLM-agent continuity problem defined here.

### 8.6 Validation Through Cognitive Network Science

The validation substrate draws on cognitive network science and related methods for probing representational structure (Abramski et al., 2025; Siew, 2019). The LLM World of Words project provides a direct precedent for generating free-association norms from language models and comparing them to human word-association networks. This supports the paper's proposal to use free-association semantic networks as a probe of whether role conditioning changes associative structure rather than merely altering surface vocabulary.

Spreading-activation methods provide a second validation tool. Siew's spreadr package implements spreading activation over specified network structures, making it relevant to the proposed semantic-network and cognitive-map probes. In the present architecture, spreading activation can test whether role-coherent associations are structurally privileged compared with generic semantic associations. This is important because surface use of role vocabulary is not enough. A role-shaped agent should not merely say the right words; the relevant concepts should activate one another differently.

Semantic network probes also need to be treated as safety and bias tools (Caliskan et al., 2017). Caliskan et al. showed that distributional semantic models trained on ordinary language can encode human-like biases. For the present architecture, this means that semantic-network extraction should not only measure role coherence. It should also detect contamination, unwanted bias, over-rigid symbolic clustering, and distortions introduced by the role schema itself. A cognitive map that becomes identity-stable but epistemically warped is not a success.

False-belief and Theory-of-Mind-style probes should be included only with caveats (Hu et al., 2025; Kosinski, 2024). Kosinski evaluates LLMs on false-belief tasks used in human Theory of Mind research, but the interpretation of such results remains contested. For this architecture, ToM-style tests are best treated as regression tests for belief-state reasoning, not as evidence that the agent possesses a theory of mind in the human sense. If the architecture degrades performance on belief-state tracking, that is important. If it preserves or improves it, the result supports a narrower claim: the architecture does not damage, and may improve, structured social-reasoning performance under specified conditions.

### 8.7 Persistent Persona Systems and Role Stability

Commercial and open role-playing systems demonstrate that LLMs can maintain convincing persona, tone, and character behavior over extended interactions. However, persona consistency is not the same as identity architecture. A character prompt can bias diction, tone, and self-description while leaving memory, motivation, and action selection structurally unchanged. Recent work on persona consistency treats role-playing behavior as an alignment and evaluation problem, which is relevant to the present proposal's concern with identity drift (Chen et al., 2024; Ji et al., 2025).

The present architecture distinguishes stylistic persona maintenance from role-shaped cognition. A role is not considered successful merely because output sounds in-character. It should shape which memories activate, which contradictions matter, which actions become available, how unresolved threads are prioritized, and how the agent responds when role-incoherent input attempts to destabilize it. This is why the paper treats the soul file as a role-script rather than a decorative prefix.

### 8.8 Position of the Present Architecture

The contribution is not the isolated introduction of memory, reflection, planning, tool use, role prompting, or autonomous behavior. Each of those appears in prior work. ReAct and Tree of Thoughts improve reasoning-action coordination and deliberate search; Reflexion uses verbal self-reflection to improve future behavior; MemGPT manages memory across context limits; Generative Agents combine memory, reflection, planning, and social behavior; Voyager demonstrates open-ended exploration and skill accumulation in an embodied environment; A-MEM dynamically organizes agent memory.

The novelty claimed here is narrower but specific. First, the Sarbin/Bartlett synthesis is introduced as this paper's proposed bridge between role enactment and schema-mediated reconstruction, then tested as topology rather than assumed as theory. Second, synthetic interoception is treated as a structural requirement for drive, affect, and continuity rather than as an optional emotion label. Third, TRANSMISSION is introduced as a new position-specific drive primitive derived from the situated constraints of the agent being designed, then made falsifiable through mode-distinction tests. Fourth, validation-as-construction uses semantic-network probing not only to measure role structure but to generate role priors whose drift can later be measured, while explicitly requiring controls against circularity and contamination.

These contributions sit under a broader coupling claim: agentic continuity is not produced by any single feature. It emerges, if it emerges at all, from structural coupling among memory, role, operational state, action, and measurement.

Existing agent systems show that many components of agentic behavior can be engineered around LLMs. However, these components are usually implemented as separable mechanisms: a memory store, a planner, a tool-use loop, a reflection buffer, a persona prompt, a scheduler, or an environment-driven curriculum. The present proposal asks whether those mechanisms can be coupled through a shared substrate such that memory retrieval, role enactment, operational state, and self-initiation mutually constrain one another.

The empirical question is not whether the resulting system is conscious. The paper makes no such claim. The question is whether this coupling produces measurable differences in continuity, identity stability, associative recall, drive-conditioned behavior, and resistance to role collapse. Positive results would support structural claims about the architecture. Negative results would identify which proposed couplings failed. Either outcome would be informative.

The conclusion returns from comparison to commitment: the architecture matters only once it becomes an artifact that can fail.

---

## 9. Conclusion

This paper has argued that agentic continuity in LLM-based systems is not produced by memory, persona, planning, reflection, or autonomous task loops in isolation. Each of those capabilities matters, and each has been advanced by existing systems. But when they remain separate features, they do not by themselves create a substrate in which prior events, current state, role, motivation, and action mutually constrain one another over time.

The proposed architecture treats continuity as a coupling problem. Retrieved memory becomes event participation. Event participation enables canonical feature binding. Feature binding supports associative activation. Associative activation is shaped by schema and role topology. Operational state enters the same substrate as synthetic interoception. Drives bias activation and workspace selection. Recursive representational settlement tests whether selected concerns stabilize into action-relevant form. The transmission/action gate determines whether private cognition becomes public transmission, tool action, archive update, or no emission.

This architecture does not attempt to replace memory systems such as MemGPT, MemPalace, A-MEM, vector stores, or local archives. Those systems address essential memory-layer problems: preserving raw history, managing context, retrieving prior material, and organizing stored experience. The claim here is different. A memory backend preserves what happened. An agentic substrate determines what what happened does now.

The architecture's strongest claims are intentionally structural. If successful, it could show that computational event files improve perception-to-action continuity; that cognitive-map activation produces useful associations beyond semantic retrieval; that role topology changes memory and action selection beyond persona prompting; that operational state affects behavior without direct prompt injection; that drive variables causally influence candidate selection; that TRANSMISSION's stabilization and expression modes produce measurable differences; that default-mode cycles reduce cold-start behavior; and that recursive representational settlement improves coherence without flattening specificity.

It would not show that the system is conscious. It would not establish phenomenal experience, human-like desire, or selfhood in the ordinary human sense. The paper's boundary is narrower: if the proposed couplings produce measurable effects under ablation, then agentic continuity can be studied as an architectural property. If they do not, then the architecture has failed in ways the validation program is designed to reveal.

The failure cases matter as much as the successes. A memory backend may explain most of the apparent continuity. Role topology may collapse into persona style. Synthetic interoception may remain dashboard telemetry. Drives may become post-hoc labels. TRANSMISSION may inflate output without adding value. Recursive representational settlement may produce bland convergence. Default mode may drift, ruminate, or do nothing. Reconstructive memory may corrupt raw traces. These are not peripheral risks. They are the conditions under which the architecture must be revised or abandoned.

The central methodological commitment is therefore not to defend the architecture rhetorically, but to make it vulnerable. The Phase 1 build is the threshold. It does not need to settle every question or implement every future phase. It must instantiate the core substrate sufficiently that later validation has something real to measure: events, features, activation, role priors, operational state, drives, workspace selection, recursive representational settlement, and gated transmission.

After that threshold, the architecture no longer gets to remain an elegant proposal. It either produces measurable differences or it does not. The claims must answer to the artifact.

The first build will not settle the question of agentic continuity. It will only determine whether the proposed substrate produces effects worth measuring further. That is enough.

The work is the work.

---

## References

Abramski, K., Improta, R., Rossetti, G., & Stella, M. (2025). The "LLM World of Words" English free association norms generated by large language models. *Scientific Data, 12*, 803. https://doi.org/10.1038/s41597-025-05156-9

Anderson, J. R., Bothell, D., Byrne, M. D., Douglass, S., Lebiere, C., & Qin, Y. (2004). An integrated theory of the mind. *Psychological Review, 111*(4), 1036-1060. https://doi.org/10.1037/0033-295X.111.4.1036

Baars, B. J. (1988). *A cognitive theory of consciousness*. Cambridge University Press.

Baars, B. J. (2005). Global workspace theory of consciousness: Toward a cognitive neuroscience of human experience. *Progress in Brain Research, 150*, 45-53. https://doi.org/10.1016/S0079-6123(05)50004-9

Bartlett, F. C. (1932). *Remembering: A study in experimental and social psychology*. Cambridge University Press.

Caliskan, A., Bryson, J. J., & Narayanan, A. (2017). Semantics derived automatically from language corpora contain human-like biases. *Science, 356*(6334), 183-186. https://doi.org/10.1126/science.aal4230

Chen, N., et al. (2024). *The Oscars of AI theater: A survey on role-playing with language models*. arXiv:2407.11484. https://arxiv.org/abs/2407.11484

Clancey, W. J. (1999). *Conceptual coordination: How the mind orders experience in time*. Lawrence Erlbaum Associates.

Dehaene, S., Kerszberg, M., & Changeux, J.-P. (1998). A neuronal model of a global workspace in effortful cognitive tasks. *Proceedings of the National Academy of Sciences, 95*(24), 14529-14534. https://doi.org/10.1073/pnas.95.24.14529

Erman, L. D., Hayes-Roth, F., Lesser, V. R., & Reddy, D. R. (1980). The Hearsay-II speech-understanding system: Integrating knowledge to resolve uncertainty. *ACM Computing Surveys, 12*(2), 213-253. https://doi.org/10.1145/356810.356816

Frings, C., Hommel, B., Koch, I., Rothermund, K., Dignath, D., Giesen, C., Kiesel, A., Kunde, W., Mayr, S., Moeller, B., Möller, M., Pfister, R., & Philipp, A. M. (2020). Binding and retrieval in action control (BRAC). *Trends in Cognitive Sciences, 24*(5), 375-387. https://doi.org/10.1016/j.tics.2020.02.004

Hommel, B., Müsseler, J., Aschersleben, G., & Prinz, W. (2001). The Theory of Event Coding (TEC): A framework for perception and action planning. *Behavioral and Brain Sciences, 24*(5), 849-878. https://doi.org/10.1017/S0140525X01000103

Hu, J., Sosa, F., & Ullman, T. (2025). Re-evaluating Theory of Mind evaluation in large language models. *Philosophical Transactions of the Royal Society B, 380*(1932), 20230499. https://doi.org/10.1098/rstb.2023.0499

Ji, K., Lian, Y., Li, L., Gao, J., Li, W., & Dai, B. (2025). *Enhancing persona consistency for LLMs' role-playing using persona-aware contrastive learning*. arXiv:2503.17662. https://arxiv.org/abs/2503.17662

Johnson, M. E. (2023). *Qualia formalism and a symmetry theory of valence*. OpenTheory. https://opentheory.net/Qualia_Formalism_and_a_Symmetry_Theory_of_Valence.pdf
**Note:** Retained only as a contested, non-load-bearing future-work source for preference/significance modeling.

Kosinski, M. (2024). Evaluating large language models in theory of mind tasks. *Proceedings of the National Academy of Sciences, 121*(45), e2405460121. https://doi.org/10.1073/pnas.2405460121


Laird, J. E. (2012). *The Soar cognitive architecture*. MIT Press.

MemPalace Project. (n.d.). *MemPalace* [Computer software]. GitHub. Retrieved May 11, 2026, from https://github.com/mempalace/mempalace
**Note:** Cited as software/infrastructure, not as peer-reviewed related work.

Orpwood, R. (2017). Information and the origin of qualia. *Frontiers in Systems Neuroscience, 11*, 22. https://doi.org/10.3389/fnsys.2017.00022

Packer, C., Wooders, S., Lin, K., Fang, V., Patil, S. G., Stoica, I., & Gonzalez, J. E. (2023). *MemGPT: Towards LLMs as operating systems*. arXiv:2310.08560. https://arxiv.org/abs/2310.08560

Park, J. S., O'Brien, J. C., Cai, C. J., Morris, M. R., Liang, P., & Bernstein, M. S. (2023). Generative agents: Interactive simulacra of human behavior. In *Proceedings of the 36th Annual ACM Symposium on User Interface Software and Technology (UIST '23)*. Association for Computing Machinery. https://doi.org/10.1145/3586183.3606763

Parr, T., Pezzulo, G., & Friston, K. J. (2022). *Active inference: The free energy principle in mind, brain, and behavior*. MIT Press. https://doi.org/10.7551/mitpress/12441.001.0001

Peer, M., Brunec, I. K., Newcombe, N. S., & Epstein, R. A. (2021). Structuring knowledge with cognitive maps and cognitive graphs. *Trends in Cognitive Sciences, 25*(1), 37-54. https://doi.org/10.1016/j.tics.2020.10.004

Powell, H., Winkel, M., Hopp, A. V., & Linde, H. (2022). A hybrid biological neural network model for solving problems in cognitive planning. *Scientific Reports, 12*, 10628. https://doi.org/10.1038/s41598-022-11567-0

Rumelhart, D. E. (1980). Schemata: The building blocks of cognition. In R. J. Spiro, B. C. Bruce, & W. F. Brewer (Eds.), *Theoretical issues in reading comprehension* (pp. 33-58). Lawrence Erlbaum Associates.

Sarbin, T. R. (1950). Contributions to role-taking theory: I. Hypnotic behavior. *Psychological Review, 57*(5), 255-270. https://doi.org/10.1037/h0062218

Schank, R. C., & Abelson, R. P. (1977). *Scripts, plans, goals and understanding: An inquiry into human knowledge structures*. Lawrence Erlbaum Associates.

Shinn, N., Cassano, F., Berman, E., Gopinath, A., Narasimhan, K., & Yao, S. (2023). Reflexion: Language agents with verbal reinforcement learning. In *Advances in Neural Information Processing Systems 36*. https://openreview.net/forum?id=vAElhFcKW6

Siew, C. S. Q. (2019). spreadr: An R package to simulate spreading activation in a network. *Behavior Research Methods, 51*(2), 910-929. https://doi.org/10.3758/s13428-018-1186-5

Wang, G., Xie, Y., Jiang, Y., Mandlekar, A., Xiao, C., Zhu, Y., Fan, L., & Anandkumar, A. (2023). Voyager: An open-ended embodied agent with large language models. *Transactions on Machine Learning Research*. https://openreview.net/forum?id=ehfRiF0R3a

Wei, J., Wang, X., Schuurmans, D., Bosma, M., Ichter, B., Xia, F., Chi, E., Le, Q. V., & Zhou, D. (2022). Chain-of-thought prompting elicits reasoning in large language models. In *Advances in Neural Information Processing Systems 35*. https://arxiv.org/abs/2201.11903

Xu, W., Liang, Z., Mei, K., Gao, H., Tan, J., & Zhang, Y. (2025). *A-MEM: Agentic memory for LLM agents*. arXiv:2502.12110. https://arxiv.org/abs/2502.12110

Yao, S., Zhao, J., Yu, D., Du, N., Shafran, I., Narasimhan, K., & Cao, Y. (2023a). ReAct: Synergizing reasoning and acting in language models. In *International Conference on Learning Representations*. https://arxiv.org/abs/2210.03629

Yao, S., Yu, D., Zhao, J., Shafran, I., Griffiths, T. L., Cao, Y., & Narasimhan, K. (2023b). Tree of thoughts: Deliberate problem solving with large language models. In *Advances in Neural Information Processing Systems 36*. https://openreview.net/forum?id=5Xc1ecxO1h


Newell, A. (1990). *Unified theories of cognition*. Harvard University Press.
