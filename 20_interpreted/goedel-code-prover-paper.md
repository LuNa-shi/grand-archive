---
source_note: "[[10_raw/papers/2026-04-17-paper-goedel-code-prover-arxiv]]"
created: 2026-04-17
type: produced
---

# Goedel-Code-Prover Paper

## What problem this source is solving
The paper is tackling automated code verification in Lean 4, where direct tactic-level proof search becomes weak or inefficient on hard verification tasks.

## Why that matters
If proof generation stays at the flat tactic level, long-horizon reasoning breaks down. A system that can decompose verification goals into manageable subgoals is much closer to the kind of structured reasoning the user cares about in code verification and mathematical proof.

## What the method actually does
The paper proposes a hierarchical proof-search system with two distinct moves:
- decompose a difficult verification goal into simpler subgoals
- run proving over the decomposed structure instead of searching flatly from the original goal

The raw note suggests several concrete ingredients:
- decomposition scoring
- supervised initialization plus hybrid RL
- a shared 8B model for decomposition and completion
- evaluation on three Lean-based code-verification benchmarks

## Main figure / picture to remember
No figure has been extracted yet.
The key architecture picture is conceptual: a verifier that inserts a decomposition layer before tactic-level completion, so proof search becomes hierarchical instead of flat.

## What was actually validated
The main concrete validation reported in the raw capture is:
- 62.0% prove success across three Lean-based code verification benchmarks with 427 tasks
- 2.6x improvement over the strongest baseline
- improved efficiency relative to much larger neural provers

If these numbers hold up under closer reading, that is a meaningful result.

## Why this note matters for my archive
This is a strong match for interests in theorem proving, code verification, RL, and long-horizon structured reasoning.
It is a likely candidate for deeper follow-up together with the repository.

## Open questions
- How much of the gain comes from decomposition itself versus model/data/training scale?
- What does the actual search procedure look like at inference time?
