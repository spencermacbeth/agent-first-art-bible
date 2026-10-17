# Art bible

A small exploration game seen from a fixed elevated camera. The world is quiet, worn and mostly empty; everything the player can use has to read at a glance from above.

## Start here

| If the task changes… | Read |
| --- | --- |
| Characters, environments, props, motion | [visual-direction.md](visual-direction.md) |
| Setting, voice, player-facing text | not yet written; starts with the first writing pass |
| Music, sound effects | not yet written |
| Menus, HUD, interaction | not yet written |

Before generating anything, state the bible revision (commit hash), the references and the constraints you are using.

## Identity

The player reads the world from a fixed elevated camera at a constant distance, so silhouette and footprint carry more than surface detail. Materials are worn, not broken. Usable objects are the only things with strong value contrast against the ground.

## Current decisions

- 2026-10-02 — concept silhouette — `terminal-a` (`sha256:7c1e2b9a4f03…`) — [decision-001](reviews/terminal-silhouette-01/decision-001.md). Material open; reconstruction not authorized.

## Open questions

- Save-point terminal: surface material. Matte wear from `ref-stone-02` without reading as carved stone. Next pass: `reviews/terminal-material-02/` (not started).
- Save-point terminal: whether the hanging body stays readable with the ground texture under it. Checked in the material pass gallery.
- Save-point terminal: reconstruction and footprint in the production scene. Separate authorization.

## Conventions

- Every entry uses the five headings described in [visual-direction.md](visual-direction.md).
- References are catalogued in [references/CATALOG.md](references/CATALOG.md). Presence in the catalog is not acceptance.
- Each pass lives in `reviews/<pass>/` with its task brief, job records, candidates, feedback export and decision records.
- Superseded direction stays in its file, dated, with the reason and the replacement.
