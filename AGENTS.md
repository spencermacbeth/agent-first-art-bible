# Maintaining this package

This repository contains reusable art-direction instructions. Keep them portable across coding harnesses, generation providers and game engines.

- Preserve the distinction between package maintenance and work in a consuming game. Do not copy this entire file into a game; adapt `templates/AGENTS.art-direction.md` instead.
- Each `skills/<name>/SKILL.md` must have a matching lowercase name and a specific description in YAML frontmatter. Supporting templates and references must travel with that skill. Avoid dependencies on another installed skill.
- Treat current user instructions, project constraints and existing authorization as inputs. A skill must not grant itself spending, publishing, deployment or destructive-edit permissions.
- Keep active references, candidate history, feedback and accepted direction distinguishable. Acceptance must identify its artifact and scope.
- Use actual project requirements for budgets, supported formats, render conditions and performance limits. Examples are illustrative, not universal defaults.
- Provider details that can change belong in the consuming project's adapter and job records. Verify them from current official documentation during implementation.
- Preserve credentials and ordinary player data. Review exports should contain stable local identities, not credentials or expiring signed download links.
- When editing a skill, check its links and frontmatter, then exercise the changed decision on a concrete example. Document what was observed without claiming a model benchmark or live-provider test that did not occur.
- Keep personal game assets and private operational details out of this package. Publishing a repository is a separate action from preparing its contents.

The package's examples and prompts are maintained in ordinary Markdown. Avoid adding an executable installer, database, provider SDK or background service unless a concrete user task requires it.
