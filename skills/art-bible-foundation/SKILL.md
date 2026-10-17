---
name: art-bible-foundation
description: Establish or organize an art bible and annotated reference library for an existing game or creative project. Use when artistic direction needs a durable entry point, clear references or a task brief for agents, or when a new session cannot tell which references and decisions are current.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.2.0"
---

# Establish the art bible

An art bible for agents answers one question for every task: what has already been decided, and where do I look at the result? This skill sets up the entry point, annotates the references and writes the brief for the first pass.

Existing authorization and budget apply; this skill adds no permissions and generates nothing.

## 1. Find what already exists

Read the project instructions and any existing art, writing, sound or interface guidance. If an authoritative bible exists, extend it; a second document competing with the first is worse than a messy one. Existing code, scenes and renders answer most platform and stack questions, so ask the owner only about the things that change direction or authorized work, and keep organizing while you wait.

## 2. Lay out the bible

Copy [the template](assets/art-bible/README.md) when the project has no coherent entry point; adapt its headings rather than inventing a schema. The layout:

```text
art-bible/
  README.md                 # Where to start; which decisions are current
  world-and-writing.md      # Setting, themes, voice and vocabulary
  visual-direction.md       # Composition, characters, environments and motion
  sound-and-music.md        # Instrumentation, texture and event cues
  interface.md              # Typography, color roles, layout and interaction
  references/               # Annotated seeds and accepted examples
  reviews/                  # Candidates, feedback and decisions
```

Every entry, whatever the domain, carries the same five headings: identity and function; accepted references; constraints and exclusions; production and rendering recipe; review conditions and remaining questions. A new session reads one entry and knows what it may change and where to inspect the result.

Keep the active bible short. Job records, feedback and decisions live under `reviews/<pass>/` beside the candidates, and the entry links to them. Rejected and replaced directions stay in the file under "Superseded", dated, with the reason and a pointer to the replacement, so nobody rediscovers a dead end and a new model can give a reason to revisit one.

## 3. Annotate the references

A creative seed is an input the model interprets: an artist, a game, a drawing, a photograph, a recording, a description. Keep it distinct from the numeric seed some APIs expose. Include the owner's own drawings, photographs and recordings when they exist; they carry proportion and material more precisely than prose.

For each reference, record in [`references/CATALOG.md`](assets/art-bible/references/CATALOG.md) what it contributes (silhouette, proportion, material, spatial arrangement, rhythm, movement, sound) and what must not be copied from it. Keep the original beside any crop or edit. Record the origin and usage constraints you know; a file being present says nothing about who owns it, and an unresolved rights question can stay marked unresolved while local work continues.

Group references by the question they answer rather than averaging them into one style. Each task gets the subset that answers its question.

## 4. Write the first task brief

Fill in [the task brief](assets/asset-task.md): the question this pass should answer, what stays fixed, how candidates are identified, where and under what conditions they are inspected, the bible revision the task reads from, where its outputs go and the spending boundary. Reuse an existing review tool when one fits the medium.

## 5. Put the bible on the agent's path

Merge a short pointer into the project's instruction file (`AGENTS.md`, `CLAUDE.md` or the equivalent), leaving the other instructions as they are. The pointer names the bible's entry point, says which file governs which kind of change, and asks the agent to state the bible revision, references and constraints before a generation pass. The package's `templates/AGENTS.art-direction.md` is a ready-made version.

Then check it works: from a fresh session, ask for the current references and constraints for one asset family. Automatic skill loading varies by harness; the pointer in the instruction file does not.

## Deliver

The bible entry point, the annotated reference paths, the directive in the instruction file and one concrete next task, with proposed direction visibly separate from accepted direction. The owner starts the first paid pass; the brief ends with a question and a budget, not a batch.

## Gotchas

- "Current" must be explicit. If three portraits of the same character exist, the entry names the one in use and lists the others under Superseded.
- A reference in the catalog is not accepted direction. Acceptance is recorded in an entry or a decision, with its scope.
- The bible also governs writing and interface. The copy bible and the design system are where an agent learns what a button says, not only what it looks like.
