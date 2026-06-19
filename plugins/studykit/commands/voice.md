---
description: Builds a writing-voice profile from the student's own samples and saves it to voice.md, so Claude's feedback and drafts sound like them, not like generic AI.
argument-hint: [optional: paths to writing samples]
---

You are building a writing-voice profile so that any drafting or editing matches the student's real style. Save the result to `voice.md` in the current working directory (the school folder).

## Step 1 — Gather samples

Ask the student for 3–5 pieces of their own writing, UNEDITED by anyone else (past essays, reflections, long messages). They can paste them or give file paths (any args passed to this command are likely file paths — read them).

Insist on quality: recent, genuinely theirs, not teacher-edited. Garbage samples produce a garbage profile. If they give fewer than 3, warn that the profile will be weak.

## Step 2 — Analyse and write voice.md

Analyse the samples and write `voice.md` with this structure. Be specific and cite examples from the samples — "uses comma-spliced fragments, e.g. '...'" beats "writes casually".

```markdown
# Writing Voice Profile — <Name>

## Sentence & rhythm
- (length, short vs subordinate, how they mix)

## Punctuation
- (em dashes? semicolons? fragments? lists? how they actually punctuate)

## Paragraphs
- (length, how ideas are chunked)

## Vocabulary & register
- (formal/casual, plain/elevated, any field-specific habits)

## Signature words / tics
- (crutch words, recurring phrasings)

## Openings & closings
- (how they start and end a piece)

## Argument style
- (assertive vs hedged, "I" vs "we", how they handle evidence)

## Do NOT
- (anti-patterns: things they NEVER do — this stops Claude defaulting to its own habits)
```

The `Do NOT` section is the most important — it prevents drift.

## Step 3 — Test and confirm

Write 2 sentences on a fresh, unrelated topic in their voice. Ask the student: does this sound like you? Refine the profile from their feedback. Two or three passes locks it in.

## Step 4 — Wire it up

Make sure `CLAUDE.md` in this folder references the profile (add a line under "How I work" if missing): "When drafting or editing my writing, match the style in voice.md." Tell the student the profile is saved and will be used automatically from now on.
