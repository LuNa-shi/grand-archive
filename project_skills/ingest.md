# Ingest skill

Purpose:
Take one source and convert it into:
1. a normalized local raw artifact
2. a concise interpreted note that helps the user understand it quickly

## Inputs
- one source URL, file, transcript, PDF, repo, post, or pasted text

## Outputs
- raw capture in 10_raw/
- optional raw static artifacts adjacent to the raw note
- interpreted note in 20_interpreted/

## Workflow
1. Identify source type.
2. Apply source-preprocessing rules.
3. Save the best local raw artifact first.
4. Create or update the raw markdown capture note with provenance.
5. Keep static source artifacts in raw, not interpreted.
6. Create a concise interpreted note that explains:
   - what problem the source tackles
   - why it matters
   - what the method/system does
   - what evidence is actually demonstrated
7. If the source has an important visual explanation, capture at least one strong local figure and embed it from raw.
8. For papers, prefer a paper-aware first pass:
   - capture the PDF locally
   - capture or derive a clean text source
   - identify the task/setup figure if it matters
   - identify the architecture/overview figure if it matters
   - identify the main result figure or table if it carries the empirical story
9. For papers, do not use webpage screenshots as final figures when a PDF-native or PDF-cropped figure is available.
10. If the source is important and the first interpreted note is still shallow, route immediately into deepen.

## Important rules
- Never summarize directly from a fragile live page if a cleaner PDF, HTML, transcript, or local artifact can be captured first.
- Prefer native source artifacts over screenshots.
- For papers, the first-pass note can stay concise, but it should already preserve enough structure for a later deepening pass.

## Quality bar
A good ingest result leaves the archive with:
- a stable source record
- at least one trustworthy local artifact
- a clear first interpreted note the user can understand quickly
- enough preserved structure to support a stronger deepen pass later
