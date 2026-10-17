# Maintaining this package

This repository contains reusable art-direction instructions. Keep them portable across coding harnesses, generation providers and game engines.

- Preserve the distinction between package maintenance and work in a consuming game. Do not copy this file into a game; adapt `skills/art-bible-foundation/assets/AGENTS.art-direction.md` instead.
- Each `skills/<name>/SKILL.md` must have a matching lowercase name and a specific description in YAML frontmatter. Supporting templates and references must travel with that skill; avoid links from a skill into the rest of the repository, since the skill folder is what gets copied.
- Treat current user instructions, project constraints and existing authorization as inputs. A skill must not grant itself spending, publishing, deployment or destructive-edit permissions. Say so once per skill, not in every section.
- Keep active references, candidate history, feedback and accepted direction distinguishable. Acceptance must identify its artifact and scope.
- Use actual project requirements for budgets, supported formats, render conditions and performance limits. Examples are illustrative, not universal defaults. Keep rules specific to one project's tooling or policy out of the skills.
- Provider details that can change belong in the consuming project's adapter and job records. Verify them from current official documentation during implementation.
- Preserve credentials and ordinary player data. Review exports should contain stable local identities, not credentials or expiring signed download links.
- The eight fragments in `skills/*/references/prompts.md` are reproduced in the companion article’s prompt section; change both or neither. `prompts.md` is only an index.
- `skills/art-bible-lock/references/terminal/` and `skills/art-bible-lock/references/worked-pass.md` describe the same fictional pass; keep their candidate IDs, references, feedback and decisions consistent. Everything in the example stays fictional and says so.
- When editing a skill, check its links and frontmatter, then exercise the changed decision on a concrete example. Document what was observed without claiming a model benchmark or live-provider test that did not occur.
- Keep personal game assets and private operational details out of this package. Publishing a repository is a separate action from preparing its contents.

The owner has scoped this repository to skills and their supporting documents and illustrative data. Do not bundle executable helpers, installers, apps, adapters, databases, services, deployment configuration or test infrastructure. Validation can use tools outside the distributed package. A consuming project may build tools under its own task authorization.

Keep paths, headings, storage formats and workflow order adaptable. Add only guidance that changes a useful decision; do not turn the worked example into a required schema or require a new review platform for an ordinary revision.
