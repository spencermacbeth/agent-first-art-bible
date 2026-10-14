# Agent-first art bible

Instructions, skills and templates for directing game art with coding agents. The process covers personal references, broad exploration, model comparison, review applications, runtime inspection and accepted decisions.

The package is written for a solo developer who wants the next agent session to understand what has already been chosen. You can use the Markdown directly with a coding tool that reads files. Automatic skill discovery depends on the tool; the instructions themselves do not require a particular harness, generation service, engine or web framework.

## Start in an existing project

1. Copy the skill folders you need from [`skills/`](skills/) into your tool's supported skill location, or keep this repository beside your project and ask the agent to read a specific `SKILL.md`. Preserve each skill's supporting files.
2. Merge the short [art-direction directive](templates/AGENTS.art-direction.md) into your project's existing instructions. Adjust the path to your art bible. Keep the other project instructions.
3. Ask the agent to read [`art-bible-foundation`](skills/art-bible-foundation/SKILL.md), inspect your current assets and prepare the bible around one asset family. If an authoritative bible already exists, extend it.
4. Use the other skills as the work requires them. A small revision does not need to repeat the whole process.

For a tool without skill discovery, a task can start with:

```text
Read /path/to/agent-first-art-bible/skills/art-bible-explore/SKILL.md
and use it for this task. The project is /path/to/my-game.
The active art bible is docs/art/ART-BIBLE.md.
We are exploring the silhouette of the save-point terminal.
Use the existing budget and provider permissions in the task brief.
```

Replace the paths with your own. A file name alone does not prove that the harness loaded it: ask the agent to identify the current references and constraints before it starts.

## Skills

| Skill | Use it for | Leaves behind |
| --- | --- | --- |
| [art-bible-foundation](skills/art-bible-foundation/SKILL.md) | Establishing or organizing the direction and reference library | A navigable bible, annotated references and a task brief |
| [art-bible-explore](skills/art-bible-explore/SKILL.md) | Comparing broad directions, models or a specific unresolved property | Distinct candidate briefs, bounded generation records and retained masters |
| [art-bible-review](skills/art-bible-review/SKILL.md) | Building or repairing a taste pass and its rendering environment | Inspectable candidates, portable feedback and relevant runtime evidence |
| [art-bible-lock](skills/art-bible-lock/SKILL.md) | Applying feedback and recording an accepted baseline | Scoped decisions, updated instructions and a reproducible review target |

[Prompt fragments](prompts.md) give concrete starting points. The [worked pass](examples/worked-pass.md) follows a fictional terminal asset through exploration, review and partial acceptance.

## What the package assumes

The project chooses its own models, stack, budget and directory structure. Read the current provider documentation when implementing a generation adapter. Keep credentials in the process that calls the API; a browser review should receive media and non-secret metadata.

The package contains instructions and document templates. It does not bundle provider adapters, a prebuilt viewer or a device-control service. The review skill guides the coding agent in building or adapting those pieces to the actual project. No generation, paid request, device deployment or publication occurs merely by installing these files.

The art bible can be ordinary Markdown. Stable candidate identities and explicit acceptance scope matter; a project-wide schema is optional. Preserve original outputs, store review derivatives separately, and make it clear whether feedback accepts a concept, a mesh, sound, motion or the integrated result.

## Portability

The skill folders use the [Agent Skills file format](https://agentskills.io/specification). [`AGENTS.md`](AGENTS.md) describes how to maintain this package; the separate [project directive template](templates/AGENTS.art-direction.md) is what you adapt for a game. The [AGENTS.md format](https://agents.md/) is supported by multiple coding tools. For a harness with another instruction mechanism, include the same directive there and link to the same authoritative bible.

No automatic loading, provider compatibility or device control is assumed solely from a filename. Verify the behavior in the tool you use.

## License

MIT. See [LICENSE](LICENSE). The example is fictional; this package contains no game assets, personal reference photographs, credentials or private device addresses. Rights to references you add remain separate from the license for these instructions.
