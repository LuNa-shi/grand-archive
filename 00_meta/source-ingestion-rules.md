# Source Ingestion and Produced-Note Rules

## Folder policy
- The current numeric prefixes exist only for ordering and system structure.
- For raw-source subfolders, create them dynamically when a real source category appears.
- Do not create unnecessary empty folders.
- If the user later wants, the top-level numbered folders can be renamed to simpler names.

## Writing policy for produced notes
- Be brief and concise.
- Focus on what the source is trying to say and what it actually does.
- Reduce non-technical discussion.
- Prefer technically grounded details over big-picture wording.
- Tell the story of the source through the concrete technical choices it reveals.
- Do not over-explain every concept.
- Do not spend much space on setup details, model sizes, or exhaustive architecture details unless they are central.
- For papers and technical blog posts, prioritize this order:
  1. what problem the source is trying to solve
  2. why that problem matters / motivation
  3. what the method or system actually does
  4. what the main figure or architecture image shows
  5. what the experiments, demos, or evaluations really validate
- Prefer validated contribution over claimed concept.
- If a source has useful images, diagrams, or figures, include the key one in the produced note whenever possible.
- When a key image matters, download it into a local asset folder and embed the local file instead of hotlinking.
- Do not settle for a random image: try to identify the true main figure, architecture overview, pipeline figure, or most explanatory image of the source.
- If the source has many figures, prefer the one that best explains the central method or strongest validated result.
- The goal is readability, not completeness.

## Blog / block generation protocol
- Treat this protocol as an evolving guide, not a fixed one-shot format.
- Keep negotiating and refining the produced-note style with the user.
- The protocol itself is important knowledge and should be updated when the user sharpens the standard.
- A good produced block should help the user grasp the source quickly, not recreate the whole source.

## Capture policy learned so far
- Use source-aware ingestion instead of blindly relying on generic web extraction.
- Prefer local-first archival: save a durable local source artifact into raw whenever possible before summarizing.
- Keep produced clean: static source files, downloaded artifacts, screenshots, PDFs, HTML exports, and reference images should live in raw, not produced.
- Choose the best native source format first, in this order when available: PDF, clean HTML, clean page text, browser/screenshot fallback.
- For papers and paper-like web pages, prefer downloading the PDF first.
- For websites, prefer exporting or downloading a PDF version first; if a good PDF is unavailable, prefer saving a clean HTML version.
- Browser/screenshot capture is a fallback for sources that do not expose a good PDF/HTML artifact.
- X/Twitter: browser-first capture.
- GitHub: browser-first capture when extraction is blocked.
- arXiv: abstract/HTML first, PDF only when necessary.
- YouTube / video sources: prefer transcript first; use frames only when the visuals themselves are technically important.
- Podcasts / audio: prefer transcript first; keep audio only as a raw attachment when useful.
- For hard webpages with animated, sliced, or visually complex figures, use browser/screenshot/vision inspection only after checking whether the PDF or HTML source has a cleaner figure.
- For figures from PDFs, prefer direct page rendering and clean cropping over screenshotting tiled web images.
- For multi-source ingestion, normalize every source into one local raw artifact first, then write produced notes from those normalized local captures.
