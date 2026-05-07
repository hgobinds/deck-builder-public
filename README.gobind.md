# Deck Builder, In A More Human Voice

Dear reader, have you ever opened a folder and felt your shoulders tighten because the thing inside it was not work, exactly, but sediment?

Old decks. Half-used templates. A PDF someone swore was important. Screenshots with names like `final_final_v3_REAL`. A PowerPoint that contains one perfect slide and thirty-seven tiny crimes against the nervous system. You know the feeling. The jaw goes a little hard. The breath gets shallow. Somewhere in the body, a small administrative death occurs.

This workspace is an attempt to make that not happen.

Deck Builder is a way of making slide decks with an AI agent without asking the agent to hold the whole mess in its head. The folder structure carries the memory. The files carry the state. The human stays in the chair where judgment belongs.

That is the point.

## The Method Underneath

This workspace was made using the Interpretable Context Methodology from [Interpretable Context Methodology: Folder Structure as Agent Architecture](https://arxiv.org/html/2603.16021v2).

The idea is simple enough to miss. The folder is not storage. The folder is architecture.

A numbered folder tells the agent where it is in the work. A `CONTEXT.md` file tells it what to load, what to ignore, what output to produce, and when to stop and ask the user. Stable references stay away from messy project material. Intermediate work stays visible, editable, plain. No black box. No magic memory. No pretending the model remembers what matters because it once saw a sentence in a chat window three hours ago.

Just files. Just stages. Just enough friction to keep everyone honest.

## What This Thing Is For

Deck Builder turns rough material into professional slide decks.

Not in one heroic leap. That way lies nausea.

It moves like this:

```text
brief -> source discovery -> narrative -> storyboard -> design -> build -> QA -> handoff -> archive
```

First, you work out what the deck is for. Who is in the room? What do they need to decide? What should they feel brave enough, calm enough, or informed enough to do after the last slide?

Then you work out what the deck is allowed to claim. User documents, internal PDFs, approved prior decks, saved webpages, source notes. No invented numbers. No fake quotes. No "industry research suggests" with nothing behind it. If the deck says a thing, the thing needs a home.

Then comes the argument. Then the storyboard. Then design. Then the actual PowerPoint. Then QA, because decks rot in small ways: a cut-off label, a stale client name, a claim that sounded true because it was smooth, a chart with no source, a speaker note that says the quiet part too confidently.

Finally, when the deck has done its job, it gets archived. Not embalmed. Curated. The useful parts survive. The rest can die peacefully.

## The Rooms In The House

`active/` is where living projects go. If a deck is currently being made, it belongs here, warm and slightly chaotic.

`archive/` is where completed, paused, superseded, or delivered projects go. The archive is not a junk drawer. It is memory with discipline.

`_config/` holds stable rules: deck types, audience profiles, visual constraints, QA checklists, brand guidance. These are the things that should apply across many decks.

`_templates/` holds reusable deck outlines and PowerPoint template notes. This is where starting structures live.

`_references/` holds approved reusable material: prior decks, example slides, messaging, source decks. If something is only relevant to one project, keep it out of here. The sacred shelf is not for laundry.

`_registry/` is the long memory: deck index, client index, reusable patterns, archive log.

`_skills/` holds helper scripts, including the boilerplate for building decks programmatically.

## The Shape Of A Project

Every active deck should look like this:

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

`project-state.md` is the pulse. Read it first. It tells you where the project is, what has been approved, what output exists, and what needs to happen next. Do not rely on chat history. Chat history is smoke. Files are bone.

Each stage folder has its own `CONTEXT.md`. That local context file matters because the agent should not load the whole universe every time it moves. A deck gets worse when the wrong context leaks in. Old drafts whisper. Rejected sources seduce. Archive material starts pretending it belongs in the current project. So the system says: load this, skip that, produce this, stop here.

Small boundaries. Big relief.

## The Rules That Matter

Do not build slides before the storyboard exists.

Every slide gets one job. One. A slide that tries to explain the market, introduce the product, handle an objection, and ask for money is not a slide. It is a panic attack with typography.

Every deck needs an audience, a decision, and a desired action. Without those three, you are decorating uncertainty.

Ask the user what they already have before searching the web. Documents, reports, prior decks, constraints, preferences, private context. Often the good stuff is already sitting in the user's folder, sweating quietly.

Do not run web searches until the source plan is discussed and approved.

Do not use rejected or undecided sources to support deck claims.

Do not invent data, quotes, logos, client facts, market claims, or convenient little truths that make the slide feel complete. The audience may not catch it. You will know. The deck will know.

Run visual QA before handoff. Actually look at the slides. Text extraction is not enough. A deck is a visual object. It has weight, spacing, rhythm, breath.

Keep project-specific mess inside the active project folder. Keep `_references/` stable. Archive useful memory, not every crumb.

## Adding Example PowerPoint Files

Example decks are how this workspace learns taste.

Not taste as in "make it pretty." Taste as in: this is how a good executive update breathes. This is how a proposal earns trust. This is how a chart-heavy deck avoids turning into spreadsheet soup. This is how a speaker deck leaves room for the human voice.

Add a small number of useful `.pptx` files. A clean branded template. A strong executive update. A good sales or proposal deck. A pitch deck if you make pitch decks. A visual-heavy deck with charts, diagrams, or product screenshots. A speaker-heavy deck with good pacing. Any approved prior client deck that future work is allowed to learn from.

Do not add every deck you find. More examples can make the system dumber. Too many voices in the room and suddenly nobody can hear themselves think.

Put reusable blank or branded templates in:

```text
_templates/
```

Put approved prior decks in:

```text
_references/approved-prior-decks/
```

Put individual useful slide examples in:

```text
_references/example-slides/
```

Put reusable messaging decks in:

```text
_references/messaging/
```

Put stable fact, chart, or benchmark decks in:

```text
_references/data-sources/
```

Run-specific material belongs inside the active project, usually here:

```text
active/project-name/01_intake/input/
```

If a file is confidential, one-off, rough, legally awkward, emotionally cursed, or simply not approved for reuse, do not place it in `_references/`.

## How To Add A Template

Add the PowerPoint file to `_templates/` with a clean lowercase name:

```text
_templates/company-open-template.pptx
```

Then add a matching note beside it:

```text
_templates/company-open-template.md
```

That note should say when to use the template, what to preserve, what to avoid, and whether it should be copied before editing. The agent needs these instructions because a template is more than a file. It has manners. Logos go somewhere. Footers behave a certain way. Type has a temperature.

A simple note is enough:

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

If this should become the default template, update `_templates/open-template.md` or the relevant stage instructions.

## How To Add A Prior Deck

Add the PowerPoint file to `_references/approved-prior-decks/`:

```text
_references/approved-prior-decks/client-topic-presentation-example.pptx
```

Then add its companion note:

```text
_references/approved-prior-decks/client-topic-presentation-example.md
```

The note should explain why the deck is worth keeping. Not "good deck." That says nothing. Say the actual thing. Strong opening. Clean objection handling. Useful two-column architecture. Great chart pacing. A closing slide that did not beg.

Use this shape:

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

Then add it to `_registry/decks-index.md` with status `Reference`. If it teaches something that should survive across projects, add the lesson to `_registry/reusable-patterns.md`.

## Large Files, Git LFS, And Other Small Sorrows

This repo is configured to treat `.pptx` files as Git LFS files. After adding a PowerPoint file, make sure the actual file is present locally, not just a tiny pointer file.

If the deck is too large, too confidential, or not meant to be committed, keep it outside the repo and add only a metadata note explaining where the user can find it locally. A missing file is annoying. A leaked client deck is worse. One gives you a headache. The other gives you heat in the stomach.

## Starting A New Deck

Create a project folder in `active/`:

```text
active/client-topic-deck-YYYY-MM/
```

Copy the standard stage folders from the sample project. Create `project-state.md`. Start in `01_intake/`. Load the root `CONTEXT.md`, the project state, and the relevant deck-type template.

Then stop.

Ask the user what the deck is for. Ask who is in the room. Ask what decision or action they want. Ask what material they already have. Ask what constraints matter. Give them the chance to empty their pockets before you start arranging the objects on the table.

## Resuming A Deck

Open the project folder. Read `project-state.md`. Load the current stage `CONTEXT.md`. Load only what the stage asks for. Continue from the recorded next action.

This sounds bureaucratic until you have watched an agent confidently rewrite a deck from the wrong stage with the wrong source and the wrong assumption. Then the bureaucracy starts to look like kindness.

## Naming

Use the presentation date, not the build date:

```text
YYMMDD_Presentation_Name.pptx
YYMMDD_Presentation_Name_Speaker_Notes.md
YYMMDD_Presentation_Name_QA.md
YYMMDD_Presentation_Name_Final.pptx
YYMMDD_Presentation_Name_Final.pdf
```

Use underscores. No spaces. Match the name across deck, notes, QA, and exports.

Tiny naming discipline saves future suffering. This is not glamorous. Neither is flossing. Death still comes, but at least the file can be found.

## Archive

When the deck is delivered or closed, archive it.

Keep final deliverables, source selections, saved source snapshots, narrative, storyboard, design plan, speaker notes, QA notes, handoff notes, retrospective, and any build script worth reusing. Update the archive README. Update `_registry/decks-index.md`. Update `_registry/archive-log.md`. Promote durable lessons to `_registry/reusable-patterns.md`.

Do not preserve every messy draft. The archive is not a mausoleum for indecision.

The point is that a future agent, or a future you, can open the project cold and understand what happened. What was made. What worked. What should be reused. What should be left in the ground.

May all beings make slides that know why they exist.

May all beings keep their sources clean and their claims honest.

May all beings find the final deck without scrolling through seventeen versions of shame.

A Thursday in May, 2026.
