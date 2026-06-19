# studykit

A Claude Code plugin that turns Claude into a study partner. It onboards your subjects, learns your writing voice from your own past work, scaffolds essays and analytical assignments (thesis, structure, evidence, technique, A-grade angles), and gives feedback in your own voice. You write the prose; it does the analytical heavy lifting.

## Install

In Claude Code:

```
/plugin marketplace add acehoapt/studykit
/plugin install studykit@studykit
```

## Use

1. Make a folder for your schoolwork (e.g. `~/Schoolwork`) and launch Claude Code from inside it. Always launch from this folder — that is what loads your setup.
2. Run `/setup` — answer a few questions about your subjects and upload some of your past writing so Claude learns your voice.
3. Drop in an assignment: paste the task sheet, rubric, and any texts. Claude analyses it, asks questions, and builds the scaffold with you.
4. Write the essay yourself from the scaffold. Use `/voice` anytime to refine your style profile, and `/model` for an annotated worked example.

## Commands

- `/setup` — one-time onboarding: subjects, goals, folders, and a project `CLAUDE.md`.
- `/voice` — build a writing-voice profile from your own samples.
- `/model` — an annotated worked example to learn the technique from.

The `assignment-scaffold` skill triggers automatically when you start an essay or analytical assignment.

## Updates

```
/plugin marketplace update
```
