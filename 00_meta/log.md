# Grand Archive Log

## 2026-04-17 | archive initialized
- Created initial 3-layer PKB structure in the Obsidian vault.
- Added schema, index, log, personal taste note, and Hermes best-practices note.
- Created raw / produced / synthesis directory stubs.
- Next step: collect the user's core interests, favorite source types, and seed sources.

## 2026-04-17 | profile updated with core interests
- Added high-confidence interest areas to 01_profile/personal-taste.md.
- Interests now include AI agents, LLMs, VLA models, robotics, long-horizon agents, code generation, mathematical proof, RL, AI infra, business insights, and startups in China and America.
- Next step: gather preferred source types and seed sources for daily collection.

## 2026-04-17 | source preferences and seeds added
- Added preferred source types, filtering rules, and initial seed sources to 01_profile/personal-taste.md.
- Captured preference for impactful personal blogs, broad primary-source formats, latest American trends, and no default reliance on Chinese media platforms.
- Next step: create raw-source subfolders and seed-source registry notes.

## 2026-04-17 | first source-ingestion test completed
- Captured raw notes for the user's example sources and GitHub sources using dynamic folder creation.
- Added raw captures for blog, GitHub Pages guide, course site, business portal, company research site, X post, arXiv paper, GitHub repo, and the user's GitHub profile.
- Updated the personal taste note with GitHub-derived interests including embodied AI, VLN, agent memory, navigation/planning, and LLM/VLM for robotics.

## 2026-04-17 | ingestion workflow updated from failure lessons
- Recorded a new personal operating rule for Hermes: use source-aware capture paths instead of blindly starting with generic web extraction.
- X/Twitter should be captured through browser text extraction first in this environment.
- GitHub and some docs pages may also require browser-first capture when web extraction is blocked.
- arXiv should usually start from the abstract page instead of direct PDF navigation.

## 2026-04-17 | produced-note trial created
- Added concise produced notes for Karpathy's PKB post, Physical Intelligence π0.7, and the user's GitHub profile.
- Added a short produced-note template and explicit ingestion/writing rules reflecting the user's preference for brevity, key figures, and emphasis on validated contribution over abstract concept inflation.

## 2026-04-17 | image handling rule added
- Updated the source-ingestion rules to download key images into a local asset folder when possible and embed local files instead of hotlinking.
- This makes produced notes more durable and readable inside Obsidian.

## 2026-04-17 | block-generation guide refined
- Strengthened the procedure so produced notes must try to identify the true main figure, architecture overview, pipeline figure, or strongest explanatory image.
- Replaced the hotlinked image in the π0.7 produced note with a local embedded asset.
- Recorded that the produced-note / blog-generation protocol is an evolving guide to be negotiated and improved with the user over time.

## 2026-04-17 | technical writing standard tightened
- Updated the produced-note rules to reduce non-technical discussion and prefer concrete technical details.
- Revised the π0.7 note to tell the story through the system design, conditioning structure, figure meaning, and concrete demonstrated behaviors rather than broad framing.

## 2026-04-17 | project-local skills scaffold added
- Created project_skills/ as a local operating-manual layer for this archive.
- Added reusable local skill docs for search, ingest, synthesize, source preprocessing, and blog-block quality.
- The new design treats archive workflows like composable project functions: normalize source first, then produce, then synthesize.

## 2026-04-17 | seed-source multi-platform demo distilled
- Wrote a larger-scale synthesis note showing that the current seed sources already demonstrate working ingestion across blogs, GitHub Pages, course pages, X posts, arXiv papers, GitHub repos/profiles, company sites, and business portals.
- Reduced the demonstrated successes and failures into reusable pipelines inside project_skills/source-preprocessing.md.
- This is the first real proof that the archive's source-handling layer can be treated like composable software logic rather than ad hoc note taking.

## 2026-04-17 | produced-note coverage expanded across seed sources
- Added produced notes for Karpathy blog, Claude Code guide preface, CSE 234 course page, IBM Institute for Business Value, Goedel-Code-Prover paper, Goedel-Code-Prover repository, and Physical Intelligence source overview.
- Strengthened the rule that important sources should first become concise interpreted notes before multi-source synthesis.
- Simplified project_skills/source-preprocessing.md back into a single pass-oriented control file with routing logic, for-loop logic, and source-type conditions in one place.
