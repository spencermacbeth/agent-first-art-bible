---
name: art-bible-foundation
description: Start or organize a game's art bible from the user's ideas, drawings, photos, recordings and existing assets. Use when establishing creative direction, assembling seeds for a first taste pass or making the bible discoverable to future agents.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.4.0"
---

# Start from the user's taste

Build a useful starting point for making and reviewing art. The bible should grow as the user chooses directions; they do not need to specify the whole game before seeing alternatives.

## Understand the project

Read the existing project and any artistic guidance. Find out what the game is about, what it should feel like and which part the user wants to explore next. Include setting, themes and writing style as well as images, models, interfaces, motion, music and sound where relevant.

Use what the user has already supplied. Ask only for missing choices that materially affect the work, and keep organizing the available inputs while waiting. Keep an existing bible and its layout when they work.

## Assemble the seeds

Gather the user's drawings, location photos, videos, music references, games, artists and written ideas. A seed here is a creative input, not an API's random-number setting.

For each useful reference, note what to take from it: proportions from a sketch, stonework from a photograph, an expression from a character, rhythm from a song. Keep originals and their origins. Crops, annotations and rough edits can clarify an idea without replacing the original.

Preserve distinct directions. Do not blend every reference into one mood board before the user has seen what each can lead to. Suggest additional directions when they would broaden the exploration.

## Make a bible agents can use

Create an entry point linking to the project's current direction, relevant media and open questions. Markdown alongside the project is a useful default; keep an existing format when agents can read it easily. Keep decisions close to the examples that explain them. Add generation or rendering recipes once useful ones exist.

The [bible template](assets/art-bible/README.md) and [reference catalog](assets/art-bible/references/CATALOG.md) are optional starting points. Combine sections, use existing files and leave unresolved areas open. Avoid producing empty documents for domains the project is not using.

Adapt the [project instruction](assets/AGENTS.art-direction.md) into the game's normal instruction file so future agents read the bible when creating or changing work. Preserve unrelated instructions.

## Start the next pass

Choose a concrete subject: an opponent portrait, a location, menu treatments, a sound cue. Identify the references, what can vary and what the result needs to do in the game. The optional [task template](assets/asset-task.md) helps when that information is not already in the conversation or project.

For a setup-only request, deliver the bible and the next comparison to make. If the user asked for a first taste pass, continue through generating or collecting candidates, building the interface and opening it. Do not stop at the documents. Use the generation access already provided for the project.

[Example starting request](references/prompts.md).
