# OpenBrainLM — Subproject Governance
> Auto-loaded by Claude Code when working in this directory.
> Parent governance: `C:\apps_ai\CLAUDE.md` (inherits all global rules).

---

## What Is This

An open-source LM plug-in brain. Built from biomimicry and emergent Nicomachean
ethical conflict resolution.

- **Mind** (Trinity dialectic: Logos fights Pathos, Ethos arbitrates) + **Brain** (Neural_ARC, SPAUN 2.0) = **OpenBrain**
- 8 operational layers derived from real biological mechanisms
- 8 cognitive agents named for the biological functions they ARE (SPAUN-derived, self-evolving)
- 8 curated brain regions (local knowledge store)
- LM-agnostic — pluggable backends, zero vendor lock-in

## Owner

See parent `C:\apps_ai\CLAUDE.md` for owner profile.

## Architecture (8 Layers)

| Layer | Name | Biology | Status |
|---|---|---|---|
| L1 | Active Sensing | Octopus + Rat Whiskers | BUILT |
| L2 | Ganglion | Octopus Arms | BUILT |
| L3 | Stigmergy + Swarm | Insect Hive | BUILT |
| L4 | Action Selection | Basal Ganglia + Thalamus | BUILT |
| L5 | Memory (Hippocampus) | Hippocampus | BUILT |
| L6 | Relevance Detection | Amygdala + Quorum | BUILT |
| L7 | Chromatophore | Octopus Skin Display | BUILT |
| L8 | Pathos | Human Default Mode Network | BUILT |

Cross-cutting: Prediction Error, Hebbian Plasticity (STDP), Interoception, Cerebellum Timing.

## 8 Cognitive Agents

| Agent | Biological Analogue | Function |
|---|---|---|
| hippocampus | Hippocampus | Memory routing, Hebbian learning (L5) |
| explorer | Exploratory circuits | Learning, knowledge acquisition |
| verifier | Prediction error (Friston) | Error detection, claim validation |
| immune | Immune system | Adversarial challenge, threat detection |
| prefrontal | Prefrontal cortex | Metacognition — who watches the watchers |
| morphogen | Octopus RNA editing | Self-modification, neuroplasticity |
| consolidator | Glial cells | Memory consolidation, sleep cycle |
| homeostasis | Autonomic nervous system | Self-maintenance, integrity regulation |

10 more agents will be derived from the symbiosis of neurology and
Nicomachean Ethics heuristic taxonomy as the brain matures.

## Key Files

| File | Purpose |
|---|---|
| `ARCHITECTURE.md` | Full tech spec + system diagrams |
| `OPERATIONAL_LAYERS.md` | Full 8-layer biology spec |
| `WHAT_IS_OPENBRAIN.md` | Philosophy and "why" |
| `openbrainlm/registry.py` | 8 agents + 8 brain regions |
| `openbrainlm/core/trinity.py` | Trinity dialectic engine |
| `openbrainlm/agents/hippocampus.py` | L5 Hippocampal memory routing agent |
| `openbrainlm/bridge.py` | Spinal cord — pluggable backends |
| `openbrainlm/orchestrator.py` | Ignition protocol + layer orchestration |
| `tests/` | Test suite (135 tests) |
| `docs/specs/SELF_EVOLUTION_LOOP.md` | Sleep cycle + morphogen fitness + knowledge promotion |
| `docs/specs/EPIMORPHIC_REGENERATION.md` | Blastema sandbox + autotomy |
| `docs/specs/ALLOSTATIC_DECISION_GATE.md` | 4-tier allostatic escalation |

## Rules (supplement parent CLAUDE.md)

1. **Biomimicry first.** Every layer derives from a real biological mechanism. Nothing invented. Everything assembled.
2. **Inhibition-by-default.** Default state = all actions suppressed (basal ganglia model). Actions are RELEASED, not activated.
3. **Brain regions, not file cabinets.** Route queries by semantic salience, not brute search. Hippocampus agent handles routing.
4. **Trinity is a DIALECTIC, not a pipeline.** Logos and Pathos fight. Ethos arbitrates. The fight IS the productive mechanism.
5. **Append-only knowledge.** Never delete from brain memory. Overflow to long-term storage.
6. **Quarantine before promotion.** New research → quarantine → immune agent verifies → then promote to domain region.
7. **Biological names only.** Agents are named for the cognitive function they ARE. No tech labels, no domain names.
8. **OPEN_BRAIN.md in every region.** Queen pheromone — every brain region must contain the master brain document.

## Source of Truth Hierarchy

1. Real biology (papers, books in Neural_ARC)
2. `OPERATIONAL_LAYERS.md` (architecture spec)
3. `OPEN_BRAIN.md` (master brain document)
4. Code (implements the above)

## Dependencies

- Python 3.10+ (stdlib only — zero external dependencies for core alpha)
- Pluggable backends for knowledge, agents, notifications (bridge.py)
- Phase 1: semantic-router (MIT), HippoRAG (open), Qdrant/LanceDB (Apache-2.0)
- Phase 2: DebateLLM (Apache-2.0), CraniMem (paper), snnTorch (MIT), Kotaemon (Apache-2.0)
- Phase 3: pymdp (MIT), neat-python (BSD-3), LangGraph (MIT), Letta (Apache-2.0)
- See `IMPLEMENTATION_PLAN.md` for full 86-repo component map and integration sequence
- Execution sequence: `docs/specs/SELF_EVOLUTION_LOOP.md`. Escalation logic: `docs/specs/ALLOSTATIC_DECISION_GATE.md`.
- **License rule**: Core brain = MIT/Apache/BSD only. GPL isolated via wrapper, never imported directly.
