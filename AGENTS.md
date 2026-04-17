# AGENTS.md

This file is the top-level controller for the Grand Archive workflow.

Treat the archive as a small software system made of local markdown skills.
Do not treat every request as ad hoc note taking.

## Core pipeline
Default pipeline:
source -> preprocessing -> raw -> interpreted -> deepen if important -> synthesis later

## Local skills
Use the project-local markdown skills in `project_skills/` as routing rules:
- `project_skills/search.md`
- `project_skills/source-preprocessing.md`
- `project_skills/ingest.md`
- `project_skills/paper-reading.md`
- `project_skills/pdf-extraction.md`
- `project_skills/deepen.md`
- `project_skills/synthesize.md`
- `project_skills/blog-block-quality.md`

## Routing rules

### If user command starts with `ingest`
Interpret it as a source-ingestion request.

Workflow:
1. Identify the source type.
2. Apply `project_skills/source-preprocessing.md`.
3. If the source is paper-like or PDF-first, apply `project_skills/paper-reading.md`.
4. If PDF figure/text extraction is needed, apply `project_skills/pdf-extraction.md`.
5. Apply `project_skills/ingest.md`.
6. Save the best local raw artifact first.
7. Create or update the interpreted note.
8. If the source is a paper and is important, preserve enough figure and evidence structure for a later deepen pass.
9. If the source is important and the first interpreted note is still shallow, continue with `project_skills/deepen.md`.

Example intent:
- `ingest https://...`
- `ingest arxiv:2603.19329`
- `ingest <paper url>`
- `ingest <local pdf>`

### If user asks to improve, deepen, expand, enrich, or make a note/blog more complete
Apply `project_skills/deepen.md`.

For papers and PDF-first sources, treat deepen as a dedicated paper-reading pass:
- verify the local PDF
- improve figure coverage
- improve architecture and evidence coverage
- prefer PDF-native or PDF-cropped figures over webpage screenshots
- place figures inline with the topic they explain instead of isolating them in one figure block

### If user asks specifically for paper reading, PDF extraction, figure cleanup, or paper-quality deep interpretation
Route to:
- `project_skills/paper-reading.md`
- `project_skills/pdf-extraction.md`
- then `project_skills/deepen.md` if interpretation must be upgraded

### If user asks for cross-source conclusions, comparisons, or big-picture connections
Only do this after good raw + interpreted notes exist.
Then apply `project_skills/synthesize.md`.

## Archive rules
- Normalize every important source into a stable local raw artifact first.
- Keep static artifacts in raw.
- Prefer native artifacts over fragile live pages.
- For papers, architecture figures and result figures are both important.
- For papers, webpage screenshots are fallback only, not preferred final figure assets.
- Deepening is a real stage, not an optional afterthought.
- For deep interpreted notes, prefer topic-first figure placement over gallery-style figure dumping.

## Preferred behavior
- Be source-aware.
- Reuse local skills instead of improvising the workflow each time.
- Upgrade important notes with a dedicated deepening pass before synthesis.
- Treat good deepened notes as reusable building blocks for future deep blogs.
