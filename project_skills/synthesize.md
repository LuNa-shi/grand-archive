# Synthesize skill

Purpose:
Answer higher-level questions using the archive's normalized local sources instead of live pages.

## Inputs
- one question, theme, comparison request, or idea-generation prompt

## Outputs
- direct answer
- optional synthesis note in 30_synthesis/

## Workflow
1. Start from produced notes and related raw captures.
2. Pull together the relevant local sources.
3. Compare overlap, tension, and missing pieces.
4. Separate:
   - what the sources actually support
   - what is plausible but not yet validated
   - what remains open
5. Produce either:
   - a conversational answer
   - a compact comparison
   - a new synthesis note

## Important rule
Synthesis should be downstream of good ingestion.
If source normalization is weak, synthesis quality collapses.

## Good use cases
- compare several robotics systems
- extract recurring themes from a week of sources
- answer strategic questions from the archive
- write topic maps and research directions
