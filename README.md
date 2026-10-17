# Agent-first art bible

Skills for coding agents to generate artistic alternatives, build local taste-pass interfaces, apply your feedback and keep the resulting direction in an art bible.

A **taste pass** is a place to compare alternatives and say what you like, dislike or want to combine. It might be an image gallery, a 3D viewer, a sound comparison or a set of playable menu designs. The agent builds it in your project, opens it for you, then uses your feedback to make the next round.

The **art bible** grows out of those decisions. It contains the references, examples and instructions that help subsequent agents make work that belongs in the same game: setting and writing, visuals, interfaces, music and sound.

## Start with a real task

Make these skills available to your coding agent, then give it your project and references. For example:

```text
Help me develop the art direction for my game's abandoned transit station.
My drawings and location photos are in references/station/. Start from those,
then explore substantially different architectural directions. Use the model
access already configured for this project.

Generate the alternatives and build a local taste-pass app where I can compare
images, inspect any 3D models and leave notes about what to keep or change.
Run it and give me the link. After I review it, make another pass from my notes.
Record the direction I choose in the art bible and make sure future agents use it.
```

You can also start with assets you already have:

```text
Use art-bible-review to build and open a taste pass for the candidates in
experiments/station/. I want to compare them, write feedback and get that
feedback back to you for another iteration. Use our existing stack.
```

The agent should build a working interface with your actual candidates. You review it, the agent reads your saved notes or feedback export, and the next pass appears alongside the earlier one. When you choose a direction, it updates the bible with the relevant examples and how to produce more work like them. Keep playing the game as those choices come together.

## The four skills

| Skill | Ask it to do | Expected result |
| --- | --- | --- |
| [art-bible-foundation](skills/art-bible-foundation/SKILL.md) | Organize your ideas, references and existing direction | A useful starting bible, seed library and project instruction pointing agents to it |
| [art-bible-explore](skills/art-bible-explore/SKILL.md) | Generate broad alternatives or refine a specific property | Actual candidate assets, ready to compare in a taste pass |
| [art-bible-review](skills/art-bible-review/SKILL.md) | Build, reopen or improve a taste-pass interface | A running local app or existing review scene with working feedback |
| [art-bible-lock](skills/art-bible-lock/SKILL.md) | Use your feedback, iterate and carry decisions into the game | Revised candidates, an updated bible and concrete follow-up work |

Use the skills the task needs. An existing project does not need to start over, and a request for a complete first pass should continue through generation and a working review interface.

## Install or load

Copy the whole folders from `skills/` into your coding agent's documented skills directory. Each folder includes its own supporting files and MIT license. They use the [Agent Skills format](https://agentskills.io/specification).

If your tool does not discover skills automatically, ask it to read the relevant `SKILL.md` by path and follow it. The repository's `AGENTS.md` is for maintaining this package. To make agents use the art bible in your game, adapt [this project instruction](skills/art-bible-foundation/assets/AGENTS.art-direction.md).

## Bring your own project

Use your drawings, photographs, recordings, favorite references and existing assets as seeds. Describe what you like in them; you do not need to design the whole workflow upfront. The agent can use existing media or generate new candidates with your chosen models.

The skills let the agent choose tools that fit the work. A local web app is usually convenient; an engine-native view can be necessary to judge the actual shaders or gameplay camera. Models, providers, storage formats and directory layouts are project choices.

## API keys and budgets

Copy [`.env.example`](.env.example) to `.env` in your project, add your API keys and tell the agent where they are. Use the variable names your provider tools expect. Keep `.env` out of version control and keys out of the review frontend.

Budget management is outside these skills. Define spending limits directly in your agent session and set limits on the provider platforms wherever supported. The skills do not manage budgets or allocate spending between agents.

## Package contents

This repository contains instructions and optional templates, not a prebuilt app or generation service. Your coding agent writes and runs the required code in your project. Installing a skill does not itself generate assets or start a server.

[Example requests](prompts.md) cover individual steps. The [fictional worked pass](skills/art-bible-lock/references/worked-pass.md) shows how feedback changes the next iteration and the bible; its records are examples, not a required format.

MIT licensed. No game assets or provider credentials are included.
