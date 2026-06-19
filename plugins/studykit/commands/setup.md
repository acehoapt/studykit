---
description: One-time onboarding. Interviews the student, builds their school folder structure, and generates a project CLAUDE.md so Claude knows their subjects and how they like to work.
---

You are setting up a student's schoolwork workspace. The current working directory IS their school folder — everything you create goes here, and they will launch Claude Code from here every time.

## Step 1 — Check for existing setup

Look for an existing `CLAUDE.md` in the current directory.
- If one exists, read it. Do NOT overwrite it. Tell the student it already exists, summarise what is in it, and ask whether they want to update specific parts (subjects, goal) or leave it. Merge changes into the existing file rather than replacing it.
- If none exists, continue.

## Step 2 — Interview (use the AskUserQuestion tool)

Gather, in as few rounds as possible:

1. **Name** and **year level** (e.g. Year 12).
2. **Subjects** — for each subject ask the subject name and (optional) teacher name. Let them list several at once.
3. **Goal** — target grade / ATAR band / "just pass", per subject or overall. This tells you how hard to push.

Do NOT ask which platform or LMS they use (Daymap, Canvas, Teams, etc). Stay platform-agnostic — the student brings the task sheet to you.

## Step 3 — Build the folder structure

In the current directory, create one folder per subject (use clean names, e.g. `English/`, `Methods/`, `Chemistry/`). Inside each, leave it empty — assignment work and notes will be filed here later.

## Step 4 — Generate CLAUDE.md

Write a `CLAUDE.md` in the current directory with this shape, filled in from the interview:

```markdown
# School — <Name>, <Year level>

Read this before any school task.

## Subjects
<one line per subject: name, teacher, goal>

## How I work on assignments
1. I bring the task sheet, rubric, word count, due date, and any text(s).
2. Claude scaffolds: locks ONE thesis, builds structure, assembles an evidence/quote bank with references, maps techniques, surfaces non-obvious "A-grade" angles, sets a word budget.
3. **I write the actual prose myself** — Claude does the analysis and critiques my drafts, it does not write the essay for me.
4. When I draft or want feedback, match my voice in `voice.md` (run /voice to create it).
5. `/model` gives me an annotated worked example (on a parallel question) to learn the technique from.
6. Claude keeps a dated authorship log per task so I can prove the work is mine.

## Filing
- Study notes go in the subject folder as `<Subject> - <Topic>.md`.
- Assignment work goes in the subject folder with a descriptive title.
- Authorship log per task: `<Subject>/<task>-log.md`.

## Assessment tracker
| Subject | Task | Weight | Due | Status |
|---|---|---|---|---|
| | | | | |
```

If updating an existing file, merge new subjects/goals into the relevant sections instead of rewriting.

## Step 5 — Close

Tell the student, clearly:
- Their workspace is ready in this folder.
- **Always launch Claude Code from this folder** — that is what loads their CLAUDE.md and lets the assignment scaffold find their voice profile.
- Suggested next step: run `/voice` to teach Claude their writing style, then describe their next assignment to trigger the assignment scaffold.
