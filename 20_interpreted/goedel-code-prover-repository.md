---
source_note: "[[10_raw/github/2026-04-17-github-repo-goedel-code-prover]]"
created: 2026-04-17
type: produced
---

# Goedel-Code-Prover Repository

## What problem this source is solving
The repository is the implementation side of the Goedel-Code-Prover system. It exists to turn the paper's hierarchical proof-search idea into an actual Lean-centered verification stack.

## Why that matters
For this archive, papers without code are weaker signals than paper+repo pairs. The repository tells us whether the claimed method has a visible executable structure and what the engineering decomposition actually looks like.

## What the system actually does
From the visible top-level structure, the repo is organized around:
- decomposition
- proving
- benchmarking
- Lean integration
- scripts and configuration

The presence of directories like `decomposer/`, `prover/`, `benchmark/`, and `lean-ray-server/` is the important story. It suggests that the implementation mirrors the paper's hierarchical split between subgoal generation and downstream proving.

## Main figure / picture to remember
There is no figure here.
The important picture is structural: paper claims on one side, repo modules on the other, with decomposition and proving separated into explicit implementation components.

## What was actually validated
What is validated from the repo page alone is limited but useful:
- the project is public
- the structure is nontrivial and method-shaped rather than toy-like
- there is visible implementation evidence for decomposition, proving, and benchmarking

This is not proof of performance, but it is proof that the work is concretely instantiated.

## Why this note matters for my archive
This repo should be read together with the paper.
It is a good example of how the archive should treat paper+implementation pairs as stronger signals than papers alone.

## Open questions
- Which folder best reveals the core decomposition logic: `decomposer/` or `prover/`?
- Is the benchmark setup close enough to the paper to make reproduction credible?
