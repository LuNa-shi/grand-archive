# Deepen skill

Purpose:
Upgrade an already-ingested source note into a deeper, more complete interpretation suitable for a strong technical archive note or deep blog draft.

This is not first-pass ingest.
This is a second-pass quality upgrade.

## When to use
Use this after a source already has:
- a raw source note
- a first interpreted note or rough interpretation
- at least one stable local source artifact

Typical triggers:
- the note is too summary-like
- the source has important figures not yet captured
- the architecture is underspecified
- the empirical story is incomplete
- the note should become strong enough to reuse in future synthesis or blog writing

## Inputs
- one existing interpreted note
- its linked raw note
- the best available native source artifacts

## Outputs
- upgraded interpreted note
- additional local raw artifacts if needed
- clearer figure coverage
- stronger explanation of method, validation, and why it matters

## Main structural rule
Do not place all main figures in one separate gallery-like section unless the source truly requires a visual appendix.
For most deep interpretations, use topic-first organization:
- each major topic gets its own explanation block
- figures are embedded inside the section they explain
- evidence lives beside the claim it supports

## Deepening workflow
1. Read the current interpreted note first.
2. Identify what is missing:
   - problem framing
   - architecture or pipeline
   - training details
   - inference details
   - main empirical result
   - ablations
   - failure analysis
   - best figures
   - core technical design choice
3. Re-open the best native source artifact.
4. If the source is a paper or PDF-first source, apply `project_skills/paper-reading.md` and `project_skills/pdf-extraction.md` as needed.
5. Build or verify an evidence set:
   - local source artifact
   - clean text source if available
   - figure list
   - key result tables
   - ablation tables if present
6. Do a dedicated figure pass.
7. Prefer a more complete figure set, not only one benchmark chart.
8. For paper-like sources, usually capture:
   - setup/example figure
   - architecture or overview figure
   - main result figure
   - one or more figures for scaling, ablation, score quality, or failure analysis when they carry the technical story
9. Figure-source priority for papers:
   - embedded figure extracted from PDF
   - clean crop from PDF page region
   - source package/native paper asset
   - browser-rendered crop only as a fallback
10. Never use a webpage screenshot as the final paper figure if a PDF-native or PDF-cropped figure can be produced.
11. Map each chosen figure to:
   - figure number
   - caption meaning
   - section/topic where it belongs
   - why it matters in the note
12. Rewrite the interpreted note around readable topic blocks, not around a detached figure dump.
13. Rewrite figure-adjacent prose so each figure has a clear explanatory role.
14. Keep static artifacts in raw, not interpreted.
15. If the note is intended to support future blog writing, shape it into reusable blocks:
   - sharp framing
   - architecture explanation
   - training/inference or system pipeline
   - evidence-linked technical claims
   - limitations and open questions

## Recommended deep-note organization
Choose the sections that fit the source, but prefer a structure like:
- why this source matters
- problem setup or motivation
- task/setup example with figure when useful
- core method/architecture with figure when useful
- training/setup details when important
- inference/runtime behavior when important
- main results with result figure/table inline
- ablations/dynamics/failure analysis with supporting figure/table inline
- interpretation
- limits/open questions
- bottom line for the archive

## Quality bar
A good deepened note should explain:
- what exact problem the source solves
- what the main method really is
- what the core design choice is
- how training and inference work
- what the main figures actually show
- what was truly validated
- what the important limitations are
- why the source matters for the archive

## Important rule
Deepening is a note-quality upgrade stage between ingest and synthesis.
Do not jump straight from rough ingest to multi-source synthesis if the source is important enough to deserve a real second pass.

## Deep blog orientation
A strong deepened note should already contain the reusable building blocks for a technical blog:
- sharp framing
- architecture explanation
- evidence-based interpretation
- figure-linked argument
- concrete technical takeaways
- explicit uncertainty where the source does not support a stronger claim
