# Deck Builder

This workspace produces, tracks, archives, and reuses professional slide decks from rough briefs, run-specific source material, and stable brand/reference assets.

## Workspaces

- `/active`: current deck projects.
- `/archive`: completed, paused, superseded, or delivered deck projects.
- `/_registry`: indexes, client memory, reusable patterns, and archive log.
- `/_config`: stable standards and constraints.
- `/_templates`: reusable deck structures.
- `/_references`: stable reusable references only.

Inside each active project:

- `/01_intake`: collect brief, audience, goals, source material.
- `/02_source-discovery`: gather external sources, examples, data, and references.
- `/03_narrative`: shape the argument and message arc.
- `/04_storyboard`: map slide-by-slide flow.
- `/05_design-system`: choose visual direction and reusable slide patterns.
- `/06_build`: create the deck and speaker notes.
- `/07_qa`: inspect text, visuals, sources, and file integrity.
- `/08_handoff`: package final deck and supporting notes.
- `/09_archive`: close the project after the presentation is over and move useful memory into the archive.

## Routing

All root and stage `CONTEXT.md` files must include a `What To Load` table with a `Skip These` column. Loading less is part of the design.

| Task | Go to | Load | Skip These | Skills/Tools |
|---|---|---|---|---|
| Start a new deck | `/active/new-project/01_intake` | root `CONTEXT.md` + relevant template | `archive/` unless reusing a prior deck | web search if current facts are needed |
| Resume deck work | active project folder | `project-state.md` + current stage `CONTEXT.md` | completed stages unless needed | depends on stage |
| Find an old deck | `/_registry` then `/archive` | `decks-index.md` + archive `README.md` | active projects unless searching unfinished work | none |
| Gather sources | active project `/02_source-discovery` | stage `CONTEXT.md` + deck brief + intake input | build output and archive folders | discuss source plan with user first (user docs, web search, or both); never run searches without agreement |
| Shape deck argument | active project `/03_narrative` | stage `CONTEXT.md` + deck brief + approved source brief | raw saved pages unless checking a claim | reasoning |
| Create slide outline | active project `/04_storyboard` | stage `CONTEXT.md` + narrative output + source brief | raw research sprawl and unrelated templates | none |
| Choose visual direction | active project `/05_design-system` | stage `CONTEXT.md` + brand guide + config templates | unrelated brand systems and old drafts | image generation if custom visuals are needed |
| Build presentation | active project `/06_build` | stage `CONTEXT.md` + storyboard + design plan | raw intake files unless dependency is unresolved | template-based decks: copy `_skills/deck-boilerplate.py` into the project build folder; run speaker notes through `/humanizer` before saving |
| QA deck | active project `/07_qa` | stage `CONTEXT.md` + built deck + saved sources + `source-selection.md` | unrelated references and rejected drafts | `pptx`, visual QA, text extraction |
| Package final | active project `/08_handoff` | stage `CONTEXT.md` + QA output + final deck | raw working files not needed for delivery | `pdf` if export needed |
| Archive after presentation | active project `/09_archive`, then `/archive` + `/_registry` | handoff output + presentation notes + `run-retrospective.md` | active drafts without reuse value | `pdf` if export needed |

## Naming

- Deck project folders: `client-topic-deck-YYYY-MM/`
- Intake brief: `deck-brief.md`
- Narrative: `narrative-arc.md`
- Storyboard: `slide-storyboard.md`
- Design plan: `design-plan.md`
- Draft deck: `YYMMDD_Presentation_Name.pptx`
- Speaker notes: `YYMMDD_Presentation_Name_Speaker_Notes.md`
- QA notes: `YYMMDD_Presentation_Name_QA.md`
- Final deck: `YYMMDD_Presentation_Name_Final.pptx`
- PDF export: `YYMMDD_Presentation_Name_Final.pdf`
- Project state: `project-state.md`
- Archive notes: `README.md`
- Reuse notes: `reuse-notes.md`
- Archive closeout: `archive-closeout.md`

Use the presentation date (not build date) for the YYMMDD prefix. Use underscores, no spaces. Match the name across deck, speaker notes, QA, and PDF.

## Source Discovery Rules

- Always discuss the source plan with the user before running any searches.
- Ask explicitly: do you have documents, reports, or internal material to contribute?
- Only run web searches after agreeing on what to look for.
- Never assume external search is the right starting point.

## Collaboration Rules

- At the start of every stage, discuss your intended approach with the user before producing any output.
- Ask what the user wants to contribute — their own documents, preferences, constraints — before assuming.
- At intake specifically: even if the user gives a one-line brief, explicitly invite more context before drafting. Do not treat a short answer as complete.
- Only proceed after the user agrees on the direction.
- Never run searches, write drafts, or build files as the first action in a stage.

## Hard Rules

- Do not build slides before the storyboard exists.
- Every slide must have one job.
- Every deck must have a stated audience, decision, and desired action.
- Every deck must pass visual QA before handoff.
- Do not use text-only slides unless the format explicitly calls for them.
- Do not invent data, quotes, logos, claims, or client facts.
- Every active deck must have a `project-state.md`.
- Archive should preserve useful memory, not every messy working artifact.
- Keep `_references` stable; put run-specific material inside active project folders.
