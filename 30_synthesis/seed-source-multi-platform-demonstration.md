# Seed-source multi-platform demonstration

Created: 2026-04-17

## Goal
Show that the archive can already handle the current seed sources across multiple source types, and reduce the result into reusable project-local pipelines.

This is not a theoretical plan.
It is a demonstration built from the seed sources that were actually captured.

## Seed sources covered
From `01_profile/seed-sources.md`, the archive already has working raw captures for:
- personal blog: Andrej Karpathy blog
- GitHub Pages guide: Claude Code Complete Guide V2 preface
- course page: CSE 234 Data Systems for Machine Learning
- company research site: Physical Intelligence
- business portal: IBM Institute for Business Value
- X post/thread: Karpathy on LLM knowledge bases
- arXiv paper: Goedel-Code-Prover
- GitHub repository: Goedel-Code-Prover repo
- GitHub profile: LuNa-shi

So this is already a real multi-platform ingestion demonstration.

## What was proven
We already reproduced successful raw capture across these source classes:

1. Personal blog / GitHub Pages / course pages
   - worked via browser snapshot capture
   - good for page structure, headings, visible topic inventory, and why-it-matters summary
   - current weakness: not yet normalized into saved HTML or PDF artifacts by default

2. X / Twitter
   - worked via browser-visible text capture
   - this was the right move because generic extraction is unreliable here
   - successful pattern: capture visible text first, then summarize conceptually in raw

3. arXiv paper
   - worked from abstract page capture
   - successful pattern: do not start from direct PDF navigation when the environment treats it as a raw download event
   - abstract-first gave stable metadata, claims, and evaluation summary
   - later, the PDF can still be saved as a local raw artifact for figure extraction or deeper reading

4. GitHub repository / profile
   - worked via browser snapshot
   - successful pattern: capture repo metadata, top-level structure, stars/forks, and obvious technical modules
   - this is enough for a first-pass taste signal or technical source note

5. Company research site
   - worked for homepage-level capture via browser snapshot
   - deeper article interpretation worked once we identified a better figure source and moved static artifacts into raw
   - biggest lesson: web visuals can be messy; native artifacts are better than reconstructing from webpage slices

6. Business portal
   - worked via browser snapshot
   - useful as a lower-priority comparative source rather than a primary feed

## Reusable pipelines extracted from the demo

### Pipeline A — browser-structured page capture
Used successfully for:
- Karpathy blog
- Claude Code GitHub Pages guide
- CSE 234 course page
- IBM business portal
- Physical Intelligence homepage
- GitHub repo/profile pages

Steps:
1. Open page in browser.
2. Capture visible structure and topic inventory.
3. Save a raw markdown note with provenance.
4. Record whether this should later be upgraded to local HTML/PDF.

Why it worked:
- good enough for high-level source mapping
- robust when generic extraction is flaky
- fast across many heterogeneous pages

Current limitation:
- browser snapshot alone is not the final form for figure-heavy or long-form technical reading

### Pipeline B — browser-visible social text capture
Used successfully for:
- Karpathy X post on LLM knowledge bases

Steps:
1. Open the post in browser.
2. Extract visible text from the page.
3. Save the key content into raw markdown.
4. Treat screenshots as optional, not primary, unless the image/layout matters.

Why it worked:
- avoids failing generic extraction paths
- preserves the real post content instead of a broken scrape

### Pipeline C — arXiv abstract-first capture
Used successfully for:
- Goedel-Code-Prover arXiv paper

Steps:
1. Start at the arXiv abstract page.
2. Capture title, authors, version, date, and abstract-level claims.
3. Save raw markdown note.
4. Use PDF later only when needed for figures or deeper interpretation.

Why it worked:
- avoids unstable direct PDF-first handling
- gets the most important paper metadata quickly
- enough for first-pass triage

### Pipeline D — paired paper + repo capture
Used successfully for:
- Goedel-Code-Prover paper
- Goedel-Code-Prover repository

Steps:
1. Capture the paper as a conceptual/method source.
2. Capture the repo as the implementation source.
3. Cross-link them mentally or explicitly in the raw notes.
4. Use both together for future produced notes.

Why it worked:
- separates claims from implementation
- supports better technical judgment than reading either alone

### Pipeline E — article + figure refinement loop
Used successfully, though with failures first, for:
- Physical Intelligence π0.7

Steps:
1. Capture the source article/page at raw level.
2. Draft a produced note from the article.
3. If the main figure is unclear on the web page, stop trying to overfit browser screenshot workflows.
4. Look for a better native artifact.
5. Keep the chosen figure in raw, not produced.
6. Embed from raw into the produced note.

Why it mattered:
- this was the first proof that figure handling needs its own explicit rule set
- it also showed that the archive should distinguish static source artifact storage from produced-note interpretation

## Failures that taught something useful
These were not wasted failures. They became reusable logic.

### Failure 1
Trying to rely on generic extraction as the first move for every public page.

Lesson:
Use source-aware routing first.

### Failure 2
Trying to reconstruct the π0.7 main figure from messy webpage image slices.

Lesson:
When a cleaner native artifact exists, use that instead of forcing screenshot reconstruction.

### Failure 3
Putting a static source image into produced assets.

Lesson:
Produced should stay clean. Static source artifacts belong in raw.

### Failure 4
Treating all source types as if they should be captured the same way.

Lesson:
The system needs if/else routing by source class before ingestion becomes stable.

## What this means for project skills
The project-local markdown skills are already starting to behave like software modules:
- search = candidate generation
- source preprocessing = source-type routing and normalization
- ingest = raw + produced transformation
- synthesize = answer/questions layer
- blog-block-quality = output quality contract

This demo suggests the next real refinement should be:
- split source preprocessing into more atomic platform modules
- write down successful branches as reusable if/else logic
- treat each markdown skill as a compact control program for an agent capability

## Suggested next decomposition
The next version should likely split source preprocessing into:
- website-pages.md
- x-posts.md
- arxiv-papers.md
- github-sources.md
- company-research-sites.md
- video-and-transcript-sources.md

Each file should describe:
- trigger conditions
- preferred local artifact
- fallback order
- common failure modes
- what counts as success

## Bottom line
The seed sources already prove that this archive can handle multiple source types in a real way, not just as a concept.

The most important architectural lesson is this:
Do not let live webpages be the working memory of the system.
Normalize each source into a local raw artifact first, then let higher-level skills operate on that stable layer.
