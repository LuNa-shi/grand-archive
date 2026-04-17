# Search skill

Purpose:
Actively search for new high-signal sources aligned with the user's interests and prepare them for possible ingestion.

## Inputs
- the user's interest profile
- seed sources
- time horizon: daily / weekly / ad hoc
- optional topic focus

## Outputs
- a shortlist of high-signal new sources
- short why-it-matters bullets
- links ready for ingestion

## Workflow
1. Start from the user's interest profile and seed sources.
2. Search for the latest material from primary or high-signal sources.
3. Prefer frontier American signals and original builders/researchers.
4. Reject low-signal aggregation and default Chinese media platforms.
5. Group findings by theme:
   - agents
   - embodied AI / robotics
   - reasoning / code / proof
   - AI infra
   - business / startup intelligence
6. For each candidate source, decide:
   - ignore
   - save for raw capture
   - ingest immediately
7. When used in a scheduled run, produce a compact daily digest.

## Important rule
Search does not directly write polished produced notes.
Search finds candidates.
Ingest does the normalization and note generation.

## Good behavior
- prefer direct sources over reporting about sources
- prefer latest technically meaningful updates
- keep candidate lists small and high-signal
- avoid flooding the archive
