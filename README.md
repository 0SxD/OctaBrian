# OpenBrainLM

An open-source LM plug-in brain. Built from biomimicry and emergent Nicomachean ethics-based conflict resolution.

## What Is This

A pluggable brain architecture for language models. 8 operational layers derived from real biological mechanisms. 8 cognitive agents. 8 curated brain regions. A Trinity dialectic engine where Logos fights Pathos and Ethos arbitrates — the fight IS the thinking.

LM-agnostic. Pluggable backends. Zero vendor lock-in. Pure Python stdlib core.

**Read the full philosophy:** [`WHAT_IS_OPENBRAIN.md`](WHAT_IS_OPENBRAIN.md)

## Origin Story

This project started as a research deep dive — the first thing built using Claude Code as an autonomous research and development tool. The question was: *can you derive a functional brain architecture from real biology, not metaphors?*

The 8-layer architecture, the Trinity dialectic, the concept papers — all emerged from that exploration. We're putting it out there to see what people think. The research was fascinating. The code works. Whether it's useful beyond the exploration is for the community to decide.

**The 4 concept papers** in `docs/concept_papers/` document the thinking:
1. [The Dialectic Loop](docs/concept_papers/01_THE_DIALECTIC_LOOP.md) — adversarial debate as decision mechanism
2. [The Trinity & Memory](docs/concept_papers/02_THE_TRINITY_AND_MEMORY.md) — recursive self-checking + sleep cycle
3. [The Self-Learning Brain](docs/concept_papers/03_THE_SELF_LEARNING_BRAIN.md) — evolution, fitness, knowledge promotion
4. [The 8-Layer Brain](docs/concept_papers/04_THE_8_LAYER_BRAIN.md) — full architecture with proven components

## Quick Start

```bash
# Clone
git clone https://github.com/OpenBrainLM/OpenBrainLM.git
cd OpenBrainLM

# Install (editable)
pip install -e .

# Run CLI
python -m openbrainlm

# Run tests
pytest tests/ -v
```

## Architecture

| Layer | Name | Biology |
|---|---|---|
| L1 | Active Sensing | Octopus + Rat Whiskers |
| L2 | Ganglion | Octopus Arms |
| L3 | Stigmergy + Swarm | Insect Hive |
| L4 | Action Selection | Basal Ganglia + Thalamus |
| L5 | Memory (Hippocampus) | Hippocampus |
| L6 | Relevance Detection | Amygdala + Quorum |
| L7 | Chromatophore | Octopus Skin Display |
| L8 | Pathos | Human Default Mode Network |

Cross-cutting: Prediction Error, Hebbian Plasticity (STDP), Interoception, Cerebellum Timing.

## Key Documents

| Document | What It Covers |
|---|---|
| [`WHAT_IS_OPENBRAIN.md`](WHAT_IS_OPENBRAIN.md) | Philosophy, Trinity dialectic, why this exists |
| [`ARCHITECTURE.md`](ARCHITECTURE.md) | Full technical spec + system diagrams |
| [`OPERATIONAL_LAYERS.md`](OPERATIONAL_LAYERS.md) | 8-layer biology spec with implementation details |
| [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md) | Phase sequence + 86-repo component map |
| [`OPEN_BRAIN.md`](OPEN_BRAIN.md) | Queen pheromone — core principles (append-only) |

## Design Principles

1. **Biomimicry first.** Every layer derives from a real biological mechanism. Nothing invented. Everything assembled.
2. **Inhibition-by-default.** Default state = all actions suppressed (basal ganglia model). Actions are RELEASED, not activated.
3. **Trinity is a DIALECTIC, not a pipeline.** Logos and Pathos fight. Ethos arbitrates. The fight IS the productive mechanism.
4. **Append-only knowledge.** Never delete from brain memory. Overflow to long-term storage.
5. **Quarantine before promotion.** New research enters quarantine first. Immune agent verifies. Then promote.

## Status

**Alpha** — all 8 layers built, orchestrator functional, 135 tests passing. Phase 1 complete. The brain knows its architecture. It does not yet know its name.

This is exploratory research, not production software. Use it, learn from it, build on it.

## Acknowledgments

The concept of a persistent, pluggable brain for AI was inspired by [OB1 (Open Brain)](https://github.com/NateBJones-Projects/OB1) by Nate B. Jones. OB1 provides persistent memory infrastructure — database, vector search, and an open protocol that any AI tool can plug into.

OpenBrainLM is a completely independent project — different architecture, different purpose. OB1 is the memory infrastructure layer; OpenBrainLM is a pluggable brain architecture built from biological mechanisms. No code was taken from OB1. The inspiration was the idea itself: that AI needs a real brain, not just a context window.

## License

[MIT](LICENSE)
