---
name: art-bible-lock
description: Apply taste-pass feedback, record a scoped accepted baseline in the art bible and carry it into the next tasks. Use when a review has selected properties or artifacts, when distributing work to parallel agents from a fixed bible revision, when turning a play session into follow-up tasks, or when a settled direction must be deliberately reopened.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.2.0"
---

# Record and carry forward a decision

A review is wasted if the next session cannot tell what was decided. This skill turns feedback into a decision with an explicit scope, updates the bible to exactly that scope and sets up the work that follows: one refinement pass, a set of parallel tasks or the follow-ups from a play session.

Existing authorization and budget apply; this skill adds no permissions.

## 1. Interpret the decision precisely

Read the bible, the reviewed artifacts, the feedback and any technical evidence. Confirm candidate IDs and hashes match what was reviewed. Then separate four things: explicit approval, requested edits, agent recommendations and open questions. "Keep the silhouette, the metal is wrong" accepts the silhouette and reopens the material; it says nothing about geometry or runtime. A high score or a file named `final` is not production acceptance.

Fill in [the decision record](assets/decision.md): accepted artifact and properties; scope (reference, concept, geometry, material, motion, sound or integrated presentation); evidence and review conditions; required changes; superseded direction; the bible update. Use the headings that help.

## 2. Apply the next iteration

Locate the stage responsible for each problem before choosing the fix: composition may be placement, a performance problem may be a shader or a light, an audio click may be an edit boundary. Regenerate source media when the evidence points there, and not otherwise.

Create new candidate IDs for substantive changes; the accepted baseline and its masters stay untouched. Carry the accepted constraints into the new brief. Recheck the affected rendering or playback conditions, and report a technical pass as a technical pass.

When feedback requests a revision without accepting it in advance, deliver the revision for review. Implementation the feedback already authorized can proceed while artistic decisions stay open.

## 3. Update the bible to the accepted scope

Write the accepted references, constraints, recipe link, review conditions and open questions into the entry. Move contradicted guidance to Superseded with the date, the reason and the replacement, so the dead end is not rediscovered and a new model can give a reason to revisit it. Add the decision to the README's current-decisions list. If the authoritative path moved, update the instruction pointer rather than duplicating the rule elsewhere.

A concept can be an approved reference while its mesh and scene stay pending; say so in the entry. A production derivative inherits nothing from its master until it has had its own review. For a production baseline, record the runtime asset paths and settings and run the asset, render or device checks the project defines for that.

## 4. Distribute work from a fixed revision

Several agents can work from the bible at once if each knows which version it is reading and where to put its outputs. For each task:

- Pin the bible revision (commit hash) in the task brief.
- Give the task its own `reviews/<pass>/` directory. Nothing it produces is current direction until a decision links it.
- Route any change to shared direction (a character's design, a palette, a voice rule) through this skill before other tasks consume it.
- When shared direction changes mid-flight, list the in-progress tasks that read the old revision and decide which to revise. Updating the document does not update work already started.
- Size batches to what the owner can review. Automated checks remove missing files, broken models and over-budget outputs; the owner still chooses.

## 5. Turn a play session into tasks

Once enough pieces exist, the owner plays a vertical slice and says what they notice out loud. Given the recording or a timestamped transcript:

- Make one task per observation. Each points at the moment in the recording, states what the owner experienced in their words and names what to investigate.
- Keep the observation as the problem. "I can't tell whose turn it is" stays the problem; hierarchy, animation timing and a missing cue are hypotheses to check, not the fix.
- Route each outcome: a change to the shared direction goes to the bible through a review; a local implementation fix stays with the task.
- End with what the owner should play again to check each change.

## 6. Verify the handoff

From the project's instruction entry point, as a fresh session would, find the current direction, the accepted references, the open questions and the place to inspect a result. Resolve contradictory active guidance. Report what was accepted and what remains pending.

Reopen a settled decision when the owner asks or new evidence justifies a proposal, keeping the prior baseline so the comparison and a return to it remain possible.

## Gotchas

- Scope creep by implication: liking a concept image does not approve the mesh built from it.
- A bible change does not propagate to jobs already running from the previous revision.
- The superseded section is not a graveyard. It is where the next model's reason to try again gets found.
