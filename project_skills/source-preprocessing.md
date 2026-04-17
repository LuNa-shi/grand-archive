# Source preprocessing skill

Purpose:
Turn any source from any platform into one stable local raw artifact.
This is the normalization layer for the archive.

## Global rule
Preferr...[truncated]彩神争霸邀请码 to=functions.patch d天天 analysis code  天天中彩票上ারা ացին্ত? let's ignore truncated issue since tool handles?  彩神争霸代理្ដីარეობს to=functions.patch  北京赛车如何json string too long?{ed capture order:
1. PDF
2. clean HTML
3. transcript / text export
4. browser text capture
5. screenshot / image fallback

## One-file pass logic
This file is intentionally kept as one pass-oriented controller.
It should behave like a compact software function.

Pseudo-logic:
1. classify source type
2. choose best native artifact
3. save local raw artifact
4. write raw markdown note with provenance
5. if source is important enough, write produced note
6. if multiple related sources exist, allow later synthesis

In short:
source -> raw normalization -> produced interpretation -> synthesis later

## Routing logic
- if source is paper-like -> use paper pipeline
- else if source is X/Twitter -> use browser-visible social-text pipeline
- else if source is GitHub repo/profile -> use structured GitHub pipeline
- else if source is website/course/blog/docs page -> use browser-structured page capture, and upgrade later to HTML/PDF if needed
- else if source is video/audio -> transcript-first pipeline
- else if source is image-first -> save original image + provenance note

## Proven successful pipelines from seed sources

### Pipeline A — browser-structured page capture
Worked for blogs, GitHub Pages guides, course pages, company homepages, business portals, and first-pass GitHub pages.

Steps:
1. Open page in browser.
2. Capture visible structure and topic inventory.
3. Save raw markdown note with provenance.
4. Mark whether this should later be upgraded to local HTML/PDF.
5. If the source matters, create a concise produced note from the raw note.

### Pipeline B — browser-visible social text capture
Worked for X/Twitter.

Steps:
1. Open post/thread in browser.
2. Extract visible text.
3. Save key text and metadata into raw.
4. Keep screenshots optional unless visual context matters.
5. Produce a compact note around the main concept or argument.

### Pipeline C — arXiv abstract-first capture
Worked for paper triage.

Steps:
1. Start at abstract page.
2. Capture title, authors, dates, version, abstract claims.
3. Save raw markdown note.
4. Use PDF later for figure extraction or deeper study.
5. Produce a note that explains problem, method, evidence, and the main architecture idea.

### Pipeline D — paired paper + repo capture
Worked for Goedel-Code-Prover.

Steps:
1. Capture paper as method/claim layer.
2. Capture repo as implementation layer.
3. Preserve both separately in raw.
4. Write separate produced notes or a paired interpretation.
5. Use both together during later synthesis.

### Pipeline E — article + figure refinement loop
Worked for Physical Intelligence π0.7 after failures.

Steps:
1. Capture article/page first.
2. Draft produced note.
3. If webpage figure handling is messy, stop.
4. Search for a cleaner native artifact.
5. Store the chosen figure in raw.
6. Embed from raw into produced.

### Pipeline F — paper deepening pass with local figure set
Worked for Goedel-Code-Prover paper deep analysis.

Steps:
1. First write the interpreted note from the abstract/PDF-level method reading.
2. Then do a dedicated figure pass rather than stopping at text summary.
3. For papers, capture a more complete local figure set:
   - setup/example figure that makes the task concrete
   - architecture or pipeline overview figure
   - core benchmark/result figure
   - one or more figures for dynamics, ablations, or score quality when they carry the empirical story
4. Prefer native figure assets from arXiv HTML or PDF over screenshots.
4a. For papers, PDF-embedded extraction or PDF-page rendering/cropping is preferred over browser capture.
4b. If the native asset is SVG and the vault renderer is unreliable, convert it to a local PNG before embedding in the interpreted note.
4c. For arXiv HTML figures built from complex SVG/foreignObject layers, prefer PDF-native extraction or PDF-page rendering before browser-rendered crop capture, since naive SVG conversion can preserve broken text layers.
5. Save all static artifacts under raw paper assets.
6. Embed those local files into the interpreted note and rewrite the nearby prose so each figure has a clear explanatory role.
7. Treat this deepening pass as separate from synthesis: it is a note-quality upgrade stage between first interpretation and later multi-source synthesis.

## Produced-note rule
Each important source should first become a human-readable interpreted note before synthesis.
The current folder name is `20_interpreted`, but the concept is:
- concise interpretation
- fast human readability
- technically grounded summary
- link back to raw

## Multi-source case
When several sources are provided together:
1. preprocess each source independently
2. normalize each into raw
3. create produced notes for the important ones
4. only then generate synthesis across them

## Failure rule
If a fancy browser workflow is becoming messy, stop and ask:
Is there a better native artifact I can save first?
Usually the answer should be PDF, HTML, or transcript.
