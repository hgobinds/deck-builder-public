# Deck Builder Router

## What This Workspace Is

This is an agent-native workspace for producing slide decks as arguments with visual pacing. Work moves through intake, source discovery, narrative, storyboard, design, build, QA, handoff, and post-presentation archive.

## What To Load

| Task | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| Start a new deck | `CLAUDE.md`, `_config/deck-types.md`, relevant `_templates/*.md` | `archive/` unless explicitly reusing a prior deck | `active/[project]/01_intake/output/deck-brief.md` | User asks for a new deck |
| Resume a deck | `active/[project]/project-state.md`, current stage `CONTEXT.md` | Old stage outputs unless needed for current dependency | Updated current-stage output | User names an active project |
| Source discovery | `01_intake/output/deck-brief.md`, `02_source-discovery/CONTEXT.md`, `01_intake/input/` | Build, QA, handoff, archive | `source-candidates.md`, `source-selection.md`, `source-brief.md` | Brief says external evidence is needed |
| Narrative | `deck-brief.md`, `source-brief.md`, `03_narrative/CONTEXT.md` | Raw saved pages unless checking a claim | `narrative-arc.md` | Approved sources exist or sourcing is skipped |
| Storyboard | `narrative-arc.md`, `source-brief.md`, `04_storyboard/CONTEXT.md` | Raw notes and unrelated templates | `slide-storyboard.md` | Narrative is approved |
| Design | `slide-storyboard.md`, `_config/brand-guide.md`, `_config/visual-constraints.md`, relevant template, `open-template.md` for template-based decks | Unrelated brand systems and old drafts | `design-plan.md` | Storyboard is approved |
| Build | `slide-storyboard.md`, `design-plan.md`, `06_build/CONTEXT.md`; template-based decks: copy `_skills/deck-boilerplate.py` into the project build folder | Raw intake unless a dependency is unresolved | `YYMMDD_Name.pptx`, `YYMMDD_Name_Speaker_Notes.md` | Storyboard and design are approved |
| QA | `YYMMDD_Name.pptx`, `YYMMDD_Name_Speaker_Notes.md`, saved pages, `source-selection.md`, `07_qa/CONTEXT.md` | Rejected sources except to confirm they were not used | `YYMMDD_Name_QA.md` | First deck draft exists |
| Handoff | QA output, final deck, source list, `08_handoff/CONTEXT.md` | Working drafts without delivery value | handoff package | QA is approved |
| Archive | handoff output, outcome notes, `run-retrospective.md`, `09_archive/CONTEXT.md` | Active drafts without reuse value | archive package + registry updates | Presentation is over or project is closed |

## Process

`brief -> source discovery -> narrative -> storyboard -> design plan -> build -> QA -> handoff -> archive`

## What Not To Do

- Do not build before a storyboard exists.
- Do not use unapproved sources to support deck claims.
- Do not treat `_references` as a dumping ground for project-specific material.
- Do not promote one-off lessons into stable workspace rules before archive review.
