# Art bible

Status: template. Replace this line with one sentence on what the game is and the experience its art serves.

## Start here

| If the task changes… | Read |
| --- | --- |
| Setting, story, names, voice or any player-facing text | [world-and-writing.md](world-and-writing.md) |
| Characters, environments, props, cards, motion | [visual-direction.md](visual-direction.md) |
| Music, sound effects, the mix | [sound-and-music.md](sound-and-music.md) |
| Menus, HUD, typography, color roles, interaction | [interface.md](interface.md) |

Before generating anything, state the bible revision (commit hash), the references and the constraints you are using.

## Identity

Audience, viewpoint and gameplay context where they affect art decisions, and the relationships that must stay consistent across every asset family. Two or three sentences; the detail belongs in the domain files.

## Current decisions

Newest first. One line each: date, scope, artifact, decision record.

- YYYY-MM-DD — (scope) — (artifact ID and hash) — [decision](reviews/<pass>/decision-NNN.md)

## Open questions

What is unresolved and which pass is meant to resolve it.

## Conventions

- Every entry uses the five headings described in [visual-direction.md](visual-direction.md), whatever the domain.
- References are catalogued in [references/CATALOG.md](references/CATALOG.md). Presence in the catalog is not acceptance.
- Each pass lives in `reviews/<pass>/` with its task brief, job records, candidates, feedback export and decision records. See [reviews/README.md](reviews/README.md).
- Superseded direction stays in its file, dated, with the reason and the replacement.
