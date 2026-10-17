# Visual direction

## Identity

Fixed elevated camera at a constant distance: silhouette and footprint first, surface detail second. Worn, not broken. Usable objects are the only strong value contrast against the ground. Defined so far by the owner's own sketches and photographs in [references/CATALOG.md](references/CATALOG.md); no external artist reference has been adopted yet.

## Entries

### Save-point terminal

**Identity and function.** The place the player saves, one per area. It has to be identifiable from the camera without UI, and its activation side has to be obvious because the interaction zone is fixed on the south face of its tile.

**Accepted references.**

- `terminal-a` concept image, `reviews/terminal-silhouette-01/candidates/terminal-a.png`, `sha256:7c1e2b9a4f03…`. Accepted 2026-10-02 by the owner as a **concept reference for silhouette and hanging proportions only** ([decision-001](reviews/terminal-silhouette-01/decision-001.md)). Its material is explicitly not accepted.
- `ref-bracket-01` (owner's sketch) for suspension and proportion; `ref-stone-02` (owner's photograph) for surface wear. Both in the [catalog](references/CATALOG.md).

**Constraints and exclusions.**

- Footprint one floor tile; interaction on the south face; nothing overhangs the tile on that side.
- Asymmetric bracket with the body hanging below it, as in `terminal-a`. Proportions fixed.
- No polished or reflective metal (rejected 2026-10-02).
- Not carved stone; wear comes from use, not geology.
- No text or symbols copied from `ref-stone-02`.

**Production and rendering recipe.**

- Concept: `example-provider` image edit endpoint with both references attached as images; settings in [jobs.md](reviews/terminal-silhouette-01/jobs.md).
- Reconstruction: not yet authorized. When it is, that pass adds thin-geometry, material and footprint checks in `scenes/review/terminal-stage`, the production camera at the production distance.

**Review conditions and remaining questions.**

- Concept review: all candidates at the same intended on-screen size, one-tile footprint overlay, camera elevation matching the game. Owner reviews in the local gallery for the pass.
- Open: surface material (next pass `terminal-material-02`). Open: readability of the hanging body over the ground texture.

## Superseded

- 2026-10-02 — Polished metal body, as generated in `terminal-a`. Rejected: reads as new and reflective, which contradicts the worn world. Replaced by matte wear, to be explored in `terminal-material-02`. The image remains the silhouette reference.
- 2026-10-02 — `terminal-b` (stone archive marker) and `terminal-c` (fabric signal post). Not selected: `terminal-b` disappears into the ground from the camera; `terminal-c` reads as a flag rather than a device. Both kept in `reviews/terminal-silhouette-01/candidates/` for comparison.
