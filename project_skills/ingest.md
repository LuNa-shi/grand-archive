# Ingest skill

Purpose:
Take one source and convert it into:
1. a normalized local raw artifact
2. a concise produced note that helps the user understand it quickly

## Inputs
- one source URL, file, transcript, PDF, repo, post, or pasted text

## Outputs
- raw capture in 10_raw/
- optional raw static artifacts adjacent to the raw note
- produced note in 20_interpreted/

## Workflow
1. Identify source type.
2. Apply source-preprocessing rules.
3. Save the best local raw artifact first.
4. Create or update the raw markdown capture note with provenance.
5. Identify the best explanatory figure if one matters.
6. Keep static source artifacts in raw, not produced.
7. Create a concise produced note that explains:
   - what problem the source tackles
   - why it matters
   - what the method/system does
   - what the main figure shows
   - what evidence is actually demonstrated
8. Embed raw-hosted local figures into the produced note when useful.

## Important rule
Never summarize directly from a fragile live page if a cleaner PDF, HTML, transcript, or local artifact can be captured first.

## Quality bar
A good ingest result leaves the archive with a stable source record and a note the user can understand in under a minute.
