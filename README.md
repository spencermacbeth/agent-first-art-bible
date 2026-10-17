# Agent-first art bible

Skills, prompts and templates for directing game art with coding agents.

The problem it solves: the next agent session, or the hundredth one running in parallel, has to find what has already been decided about the look of the game without you re-explaining it. An art bible written for agents records the references you chose, the properties you accepted, the scope of that acceptance and where the result gets inspected, so a new task starts from the current direction instead of from the project's history.

This is the companion package to the article [Engineering an agent-first art bible](https://zeroknowledgegame.com/blog/engineering-an-agent-first-art-bible/), which explains the workflow and the reasoning behind it. The repository holds the reusable parts: four skills in the [Agent Skills](https://agentskills.io/specification) format, a directive for your project instructions, eight prompt fragments, a bible template and a worked example with every record filled in.

Two terms come up throughout. A **seed** is a creative input the model interprets: an artist, a game, a drawing, a photograph, a recording, a description. It is distinct from the numeric seed some APIs expose. A **taste pass** is a review of candidate directions with an interface for recording what to keep and what to change.

## How the article maps to the package

| Article | Package |
| --- | --- |
| The art bible as a development resource · Keep the bible organized enough to use · Make reading it part of the agent's instructions | [art-bible-foundation](skills/art-bible-foundation/SKILL.md), its [bible template](skills/art-bible-foundation/assets/art-bible/README.md) and the [project directive](skills/art-bible-foundation/assets/AGENTS.art-direction.md) |
| Start with maximally different directions · Treat model choice as an artistic variable · Connect the coding harness to generation APIs · Generate candidates and prepare them for inspection | [art-bible-explore](skills/art-bible-explore/SKILL.md) |
| Make the feedback environment easy to use · Build a taste pass around the decisions · Iterate in the game | [art-bible-review](skills/art-bible-review/SKILL.md) |
| Lock in the direction and distribute the work · Build a playable vertical slice and talk through it | [art-bible-lock](skills/art-bible-lock/SKILL.md) |
| Prompt fragments for the next pass | [prompts.md](prompts.md) |

## Skills

| Skill | Use it for | Leaves behind |
| --- | --- | --- |
| [art-bible-foundation](skills/art-bible-foundation/SKILL.md) | Establishing or organizing the direction and reference library | A navigable bible, annotated references, the directive in your instructions and a task brief |
| [art-bible-explore](skills/art-bible-explore/SKILL.md) | Comparing broad directions, models or a specific unresolved property | Distinct candidate briefs, bounded generation records and retained masters |
| [art-bible-review](skills/art-bible-review/SKILL.md) | Building or repairing a taste pass and its rendering environment | Inspectable candidates, portable feedback and runtime evidence where the question needs it |
| [art-bible-lock](skills/art-bible-lock/SKILL.md) | Applying feedback, recording an accepted baseline, distributing parallel tasks, turning a play session into tasks | Scoped decisions, an updated bible, pinned task briefs and a reproducible review target |

Use any skill on its own or combine the ones the task needs. Their steps, headings and paths are adaptable defaults. Keep existing project conventions, approved work and useful review tools; a small revision does not need a new bible or the full workflow.

## Start in an existing project

1. Copy [`skills/art-bible-foundation/assets/art-bible/`](skills/art-bible-foundation/assets/art-bible/) to your project as `art-bible/` and fill in what you already know. If you already have a bible, keep it; the skills extend what exists.
2. Merge the [art-direction directive](skills/art-bible-foundation/assets/AGENTS.art-direction.md) into your project's instruction file. Keep your other instructions. Adjust the path if your bible lives elsewhere.
3. Install the skills where your harness looks for them. Use your harness’s documented skill-discovery paths; the October 2026 defaults are below.

   | Harness | Project skills | Personal skills | Instruction file |
   | --- | --- | --- | --- |
   | Claude Code | `.claude/skills/<name>/SKILL.md` | `~/.claude/skills/<name>/SKILL.md` | `CLAUDE.md` |
   | Codex | `.agents/skills/<name>/SKILL.md` | `~/.agents/skills/<name>/SKILL.md` | `AGENTS.md` |
   | Cursor | `.cursor/skills/<name>/SKILL.md` or `.agents/skills/…` | `~/.cursor/skills/…` or `~/.agents/skills/…` | `AGENTS.md` or Cursor rules |
   | Gemini CLI | `.gemini/skills/<name>/SKILL.md` or `.agents/skills/…` | `~/.gemini/skills/…` or `~/.agents/skills/…` | `GEMINI.md` |
   | Others | See the [client list](https://agentskills.io/clients) for your tool's setup page | | |

   Copy each skill folder whole; the `assets/` and `references/` inside it are part of the skill.
4. Ask the agent to read `art-bible-foundation`, inspect your current assets and prepare the bible around one asset family. Then use the other skills as the work requires them; a small revision does not need to repeat the whole process.

For a tool without skill discovery, a task can start with:

```text
Read /path/to/agent-first-art-bible/skills/art-bible-explore/SKILL.md
and use it for this task. The project is /path/to/my-game.
The active art bible is art-bible/README.md.
We are exploring the silhouette of the save-point terminal.
Use the existing budget and provider permissions in the task brief.
```

Whichever way it loads, check it did: before a generation pass, ask the agent which bible revision, references and constraints it is using. That is also how you catch an outdated portrait or a discarded direction before it becomes another batch.

## The records the skills produce

Each record is shown filled in for a fictional save-point terminal in [`skills/art-bible-lock/references/terminal/`](skills/art-bible-lock/references/terminal/README.md); the [worked pass](skills/art-bible-lock/references/worked-pass.md) narrates the same pass.

| Record | Template | Filled example |
| --- | --- | --- |
| Bible entry point | [art-bible/README.md](skills/art-bible-foundation/assets/art-bible/README.md) | [example](skills/art-bible-lock/references/terminal/art-bible/README.md) |
| Domain file with one entry per asset family | [visual-direction.md](skills/art-bible-foundation/assets/art-bible/visual-direction.md) | [example](skills/art-bible-lock/references/terminal/art-bible/visual-direction.md) |
| Reference catalog | [references/CATALOG.md](skills/art-bible-foundation/assets/art-bible/references/CATALOG.md) | [example](skills/art-bible-lock/references/terminal/art-bible/references/CATALOG.md) |
| Task brief | [asset-task.md](skills/art-bible-foundation/assets/asset-task.md) | [example](skills/art-bible-lock/references/terminal/art-bible/reviews/terminal-silhouette-01/task.md) |
| Job and artifact record | [job-record.md](skills/art-bible-explore/references/job-record.md) | [example](skills/art-bible-lock/references/terminal/art-bible/reviews/terminal-silhouette-01/jobs.md) |
| Feedback export | [feedback-contract.md](skills/art-bible-review/references/feedback-contract.md) | [example](skills/art-bible-lock/references/terminal/art-bible/reviews/terminal-silhouette-01/feedback.json) |
| Decision record | [decision.md](skills/art-bible-lock/assets/decision.md) | [example](skills/art-bible-lock/references/terminal/art-bible/reviews/terminal-silhouette-01/decision-001.md) |
| Project directive | [AGENTS.art-direction.md](skills/art-bible-foundation/assets/AGENTS.art-direction.md) | [example](skills/art-bible-lock/references/terminal/AGENTS.md) |

The bible is ordinary Markdown. What matters is that candidates have stable identities, acceptance names its scope, originals stay separate from review derivatives, and superseded direction stays visible with its reason. A project-wide schema is optional.

## What this package will not do on its own

This is a skills-only package: `SKILL.md` instructions, supporting Markdown templates and references, and illustrative data. It bundles no executable scripts, provider adapters, viewer, installer, service or game assets. The review skill guides the agent in building or adapting those pieces inside your project. Installing these files generates nothing, spends nothing and deploys or publishes nothing. The skills work inside whatever authorization and budget your project already gives the agent and add none. Keep credentials in the process that calls the API; a browser review should receive media and non-secret metadata only.

The project chooses its own models, stack, budget, storage format and directory structure. The skills follow the [Agent Skills specification](https://agentskills.io/specification): concise discovery metadata, task instructions and optional resources loaded as needed. No tool allowlist or harness-specific dependency is imposed. Read the current provider documentation when implementing an adapter; provider details change faster than this package.

## Layout

- `skills/<name>/SKILL.md` — purpose, discovery metadata and core instructions
- `skills/<name>/assets/` — templates to adapt into a project, where useful
- `skills/<name>/references/` — prompts and guidance read only when needed; the complete worked example lives with `art-bible-lock`
- `skills/<name>/LICENSE` — the license travels with each copied skill
- `prompts.md` — index to the eight fragments inside the skill folders
- `AGENTS.md` — instructions for maintaining this package (not for your game)
- `generated/` and `private/` are git-ignored so local experiments can sit beside the package without being committed

## License

MIT. See [LICENSE](LICENSE). The example is fictional; this package contains no game assets, personal reference photographs, credentials or private device addresses. Rights to references you add remain separate from the license for these instructions.
