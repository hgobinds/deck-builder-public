# Stage 04: Storyboard

## What This Stage Does

Translate the approved narrative into a slide-by-slide flow.

## What To Load

| Situation | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| Default | `../03_narrative/output/narrative-arc.md`, `../02_source-discovery/output/source-brief.md`, project `project-state.md` | Raw notes and unrelated templates | `output/slide-storyboard.md` | Narrative is approved |

## Process

1. **Discuss first.** Before laying out slides, share your proposed structure with the user:
   - How many slides do you plan and in what order?
   - Are there specific slides or sections the user wants to see or avoid?
   - Are there visual ideas or examples they have in mind?
2. Get agreement on slide count and flow before writing individual slides.
3. Draft each slide using the format below.
4. Review the full storyboard with the user before marking approved.

## Slide Format

```markdown
## Slide [number]: [Working title]

Message:
Audience job:
Content:
Visual:
Speaker note:
Dependencies:
```

## Acceptance Criteria

- Every slide has a message, audience job, content, visual direction, and dependency list.
- Slide titles carry the argument rather than merely labeling topics.
- Source, data, image, quote, and approval dependencies are visible.
- Build can create the deck without returning to raw notes.

## Approval Gate

Review required by: deck owner.
Approved to proceed?: yes/no.

## What Not To Do

- Do not write out all slides before the user has agreed on the flow.
- Do not let one slide do multiple jobs.
- Do not choose decorative visuals before knowing the slide job.
- Do not hide dependencies.
