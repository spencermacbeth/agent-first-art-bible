# Art-direction decision 001: save-point terminal silhouette

## Identity and authority

- Decision `terminal-silhouette-01/decision-001`, 2026-10-02, reviewer: owner
- Source feedback: [feedback.json](feedback.json); the owner's words:

  > Keep terminal-a's suspended silhouette. Its polished metal is wrong. Try a matte finish using the broad wear in ref-stone-02, without making the object look carved from stone. Leave the hanging proportions alone.

- Bible section: `visual-direction.md` › Save-point terminal, read at revision `a1b2c3d`, updated at `b4c5d6e`
- Reviewed artifacts: `terminal-a` `sha256:7c1e2b9a4f03…`, `terminal-b` `sha256:0b44d1e7c2aa…`, `terminal-c` `sha256:e9a17f30b6d5…`

## Accepted scope

Accepted: `terminal-a`'s silhouette and hanging proportions, as a **concept reference**.

Not accepted: its material (explicitly rejected); any geometry, animation or integrated presentation. The image is a reference, not a production asset.

Agent recommendation, not a decision: run a material-only pass before any reconstruction.

## Evidence and review conditions

Reviewed in the pass gallery at 512 px on screen with the one-tile footprint overlay and the 55° camera elevation; derivative hashes recorded beside master hashes in `feedback.json`. No runtime or device check was performed; none was in scope.

## Required changes and open questions

- Next pass `terminal-material-02`: fix silhouette and proportions to `terminal-a`; explore matte wear from `ref-stone-02-crop-a`; new candidate IDs (`terminal-a-m1`, …); `terminal-a` itself untouched.
- Open: readability of the hanging body over the ground texture. Check in the material pass by placing the ground texture behind each candidate.
- Reconstruction: separate authorization and its own checks (thin geometry, material, footprint in `scenes/review/terminal-stage`).

## Superseded direction

- Polished metal body: rejected for the reason above. Retained inside `terminal-a`, which stays the silhouette reference.
- `terminal-b`, `terminal-c`: not selected; kept in `candidates/` with the reasons recorded in `visual-direction.md`.

## Active resource update

`visual-direction.md` › Save-point terminal: accepted references, constraints (no polished metal; not carved stone), recipe link, review conditions and open questions written; superseded entries added. `README.md`: current-decisions line and open questions added. No runtime integration was reviewed, and the entry says so.
