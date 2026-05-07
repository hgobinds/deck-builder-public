# Deck Builder

Deck Builder is a workspace for producing professional slide decks from rough briefs, source material, reusable templates, and stable reference assets.

It is designed for agent-assisted work. The folder structure tells an agent what to load, what to skip, what to produce next, and when to ask for user approval. The goal is to make deck creation repeatable without turning every deck into the same generic output.

## Methodology Reference

This workspace was built using the Interpretable Context Methodology described in [Interpretable Context Methodology: Folder Structure as Agent Architecture](https://arxiv.org/html/2603.16021v2).

The method treats folder structure as the orchestration layer for sequential, human-reviewed AI work. Numbered stage folders define the workflow, `CONTEXT.md` files define the local contract for each stage, stable reference material stays separate from run-specific working artifacts, and every intermediate output remains visible and editable as a plain file.

## What This Workspace Does

Deck work moves through a fixed lifecycle:

```text
brief -> source discovery -> narrative -> storyboard -> design -> build -> QA -> handoff -> archive
```

Each stage has a specific job:

- Intake clarifies the audience, decision, desired action, constraints, and source needs.
- Source discovery gathers and approves the evidence the deck is allowed to use.
- Narrative shapes the argument before any slide list is written.
- Storyboard turns the argument into slide-by-slide jobs.
- Design system defines the visual direction before the deck file is built.
- Build creates the `.pptx` and matching speaker notes.
- QA checks text, visuals, structure, sources, and unsupported claims.
- Handoff packages final files for delivery.
- Archive preserves useful memory after the project is complete.

## Folder Map

| Folder | Purpose |
|---|---|
| `active/` | Current deck projects. Each project follows the staged workflow. |
| `archive/` | Completed, paused, superseded, or delivered deck projects. |
| `_config/` | Stable standards: deck types, audience profiles, visual constraints, QA rules, and brand guidance. |
| `_templates/` | Reusable deck outlines and template notes. |
| `_references/` | Stable approved reference assets, prior decks, messaging, examples, and data sources. |
| `_registry/` | Workspace memory: deck index, client index, reusable patterns, and archive log. |
| `_skills/` | Local helper scripts and build boilerplate for deck generation. |

## Adding Example PowerPoint Files

Users should add example `.pptx` files when they want future decks to reuse a visual style, slide pattern, pacing model, layout convention, or approved prior presentation.

Use two different locations depending on the file's purpose:

| Example Type | Put It Here | Use When |
|---|---|---|
| Reusable blank or branded template | `_templates/` | The file should be used as a starting template for future decks. |
| Approved prior deck | `_references/approved-prior-decks/` | The file is a finished deck worth studying or borrowing patterns from. |
| Individual example slides | `_references/example-slides/` | Only a few slides are useful as visual examples. |
| Reusable messaging deck | `_references/messaging/` | The deck contains durable positioning, wording, or explanation patterns. |
| Data/source deck | `_references/data-sources/` | The deck is mainly used as a stable source of approved facts, charts, or benchmarks. |

Do not put one-off client files, rough drafts, confidential run-specific source material, or unapproved working decks in `_references/`. Put those inside the relevant active project, usually in:

```text
active/project-name/01_intake/input/
```

### Recommended Example Files

For a useful personal setup, add a small set of example decks:

- One clean branded template deck.
- One strong executive update deck.
- One strong sales or proposal deck.
- One strong pitch deck, if you make pitch decks.
- One visual-heavy deck with charts, diagrams, or product screenshots.
- One speaker-heavy deck with good talk-track pacing.
- Any client-approved prior deck that future work is allowed to reuse.

More is not always better. Add examples because they teach the system something reusable, not because they exist.

### How To Add A Reusable Template Deck

1. Add the `.pptx` file to `_templates/`.
2. Use a clear lowercase filename with hyphens:

   ```text
   _templates/company-open-template.pptx
   ```

3. Add a matching `.md` note beside it:

   ```text
   _templates/company-open-template.md
   ```

4. In the `.md` note, document:

   ```markdown
   # Company Open Template

   Template file: `company-open-template.pptx`

   ## Use When

   - Building a template-based deck for [team/client/use case].

   ## Build Notes

   - Preserve logo placement, footer, typography, and master layouts.
   - Inspect the PowerPoint layout inventory before building.
   - Copy the template into the active project's `06_build/output/` or working area before editing.
   - Do not overwrite the template file.

   ## Avoid

   - Do not use for [cases where this template is wrong].
   ```

5. If this should become the default template, update `_templates/open-template.md` or the relevant stage/design instructions to point to it.

### How To Add An Approved Prior Deck

1. Add the `.pptx` file to `_references/approved-prior-decks/`.
2. Use a descriptive filename:

   ```text
   _references/approved-prior-decks/client-topic-presentation-example.pptx
   ```

3. Add a matching `.md` note beside it:

   ```text
   _references/approved-prior-decks/client-topic-presentation-example.md
   ```

4. In the `.md` note, document:

   ```markdown
   # Client Topic Presentation Example

   Example file: `client-topic-presentation-example.pptx`

   ## Use When

   - Reusing slide patterns, pacing, section structure, or messaging from this deck.

   ## Reference Notes

   - This is a stable reference example, not run-specific input.
   - Do not edit the reference copy in `_references/approved-prior-decks/`.
   - If a future project transforms this deck directly, copy it into that project's `01_intake/input/` first.

   ## Reuse Value

   - [What patterns are worth reusing.]

   ## Restrictions

   - [Any client, confidentiality, brand, or usage limits.]
   ```

5. Add the deck to `_registry/decks-index.md` with status `Reference`.
6. If it teaches a durable pattern, add that pattern to `_registry/reusable-patterns.md`.

### Working With Large PowerPoint Files

This repo is configured to treat `.pptx` files as Git LFS files. After adding a `.pptx`, check that the actual file is present locally and not only a pointer file.

If a deck is too large, confidential, or not meant to be committed, leave the `.pptx` outside the repo and add only a metadata note that explains where the user can find it locally. Do not commit sensitive client decks unless they are approved for reuse.

## Active Project Structure

Every active deck project should follow this structure:

```text
active/project-name/
  project-state.md
  run-retrospective.md
  01_intake/
  02_source-discovery/
  03_narrative/
  04_storyboard/
  05_design-system/
  06_build/
  07_qa/
  08_handoff/
  09_archive/
```

Each stage has its own `CONTEXT.md` with:

- what the stage does
- what to load
- what to skip
- expected output
- acceptance criteria
- approval gate
- things not to do

`project-state.md` is the first file to load when resuming a project. It records the current stage, next action, approvals, outputs, and acceptance criteria. Do not rely on chat history to know where a deck stands.

## Core Rules

- Do not build slides before the storyboard exists.
- Every slide must have one job.
- Every deck must have a stated audience, decision, and desired action.
- Ask the user for documents, reports, prior decks, constraints, and preferences before assuming what to use.
- Do not run web searches until the source plan is discussed and approved.
- Do not use rejected or undecided sources to support deck claims.
- Do not invent data, quotes, logos, client facts, or market claims.
- Every deck must pass visual QA before handoff.
- Keep project-specific material inside the active project folder.
- Keep `_references/` stable and reusable.
- Archive useful memory, not every messy working artifact.

## How To Start A New Deck

1. Create a new project folder in `active/` using the naming pattern:

   ```text
   client-topic-deck-YYYY-MM/
   ```

2. Copy or create the standard stage folders from the sample project.
3. Create `project-state.md`.
4. Start in `01_intake/`.
5. Load the root `CONTEXT.md`, the project `project-state.md`, and any relevant deck-type template.
6. Discuss the brief with the user before writing anything.

## How To Resume A Deck

1. Open the project folder in `active/`.
2. Read `project-state.md`.
3. Load the current stage `CONTEXT.md`.
4. Load only the inputs required by that stage.
5. Continue from the recorded next action.

The workspace is intentionally designed to load less. Completed stages, archive folders, old drafts, and unrelated references should stay out of context unless they are needed for a specific dependency or claim check.

## Naming

Use the presentation date, not the build date, for deck filenames:

```text
YYMMDD_Presentation_Name.pptx
YYMMDD_Presentation_Name_Speaker_Notes.md
YYMMDD_Presentation_Name_QA.md
YYMMDD_Presentation_Name_Final.pptx
YYMMDD_Presentation_Name_Final.pdf
```

Use underscores and no spaces. Match the name across deck, speaker notes, QA, and export files.

## Reuse And Archive

The archive is where deck runs become future intelligence.

After a deck is delivered or closed:

- preserve final deliverables and important stage outputs
- write or update the archive `README.md`
- update `_registry/decks-index.md`
- update `_registry/archive-log.md`
- promote only durable lessons to `_registry/reusable-patterns.md`

The archive should help a future agent open the project cold and understand what happened, what mattered, and what is worth reusing.
