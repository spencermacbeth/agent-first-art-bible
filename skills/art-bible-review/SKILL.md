---
name: art-bible-review
description: Build or adapt a taste pass (a review interface plus its rendering environment) for images, 3D models, video or sound. Use when candidates need comparable inspection, feedback that stays attached to the artifact, or evidence from the game's actual runtime or target device.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.2.0"
---

# Build a useful taste pass

A taste pass is a review of candidate directions with an interface for recording what to keep and what to change. It is worth building well because the owner's attention is the scarce input: every bit of friction between "show me another angle" and seeing it is attention lost to the tooling. This skill chooses the rendering environment, keeps feedback attached to the right artifact and brings in runtime evidence when the question needs it.

Existing authorization and budget apply; this skill adds no permissions.

## 1. Choose the rendering environment around the decision

Read the pass question, the bible, the candidate records and the review tools the project already has. [The media review guide](references/media-review.md) says what each medium needs inspected.

Prefer the game's own renderer for integration questions. A gallery or standalone viewer is fine for candidate questions and proves nothing about runtime behavior. Reuse the project's web stack when it loads the formats; use an engine-native scene when materials, camera or lighting depend on the engine. Explain any preview approximation that changes the comparison. A local export usually meets the persistence need; add a database only when it does not.

Put camera, light, scale, playback gain and the other comparison settings under explicit control, and hold them fixed when comparing candidates. Keep raw masters when you make compressed or simplified viewing copies. Fix the presentation before attributing a difference to a model.

## 2. Keep decisions attached to their artifacts

Follow [the feedback contract](references/feedback-contract.md). Show stable candidate IDs and the pass question. Provide fields for properties to keep, changes to make, open questions and the scope of any acceptance; ratings help sorting, notes guide the next pass. Accept rough drawings and marked-up screenshots where the tool can; sometimes they are the most precise feedback available.

Support export and import, tie notes to the artifact hash so a regenerated asset cannot inherit approval, keep earlier revisions reachable, and make missing assets, unsupported formats and damaged saved state visible rather than silent.

Keyboard navigation, readable labels, no autoplaying sound, seekable video, time-stamped notes and the project's accessibility and reduced-motion requirements are part of a usable review, not polish.

## 3. Observe the actual target when the question needs it

Some questions only the runtime answers: whether a bridge obscures the route from the player's camera, whether an expression matches the accepted portrait beside it, whether a sound wears out after ten turns. Put the candidates in the production scene or playback event with the real camera, lighting, scale and UI.

On a target device, use the connection and test profile the project already has, and keep the inspection away from real saves and other sessions. Keep debugging services local or behind an authenticated tunnel. Record the build, the asset revisions and the display and playback conditions, and label the evidence as device or desktop preview. Synthetic input and frame captures show what rendered; they do not establish how the controls feel, how the audio sounds through the speakers or whether it is fun. Those stay with the owner.

## 4. Verify the review before handing it over

Exercise one real candidate of every media type, the seek or orbit controls, feedback save, export and import, and reopening the same revision. Check the intended screen size and the links to full-resolution masters. Use a disposable browser profile for test notes so validation does not land in the owner's feedback.

Deliver the local review URL or scene, the export location, the rendering settings and the preview's limitations. A review that works is not a review that approved anything.

## Gotchas

- Browser storage is per browser and per origin and can vanish. A saved note has not reached the repository until it is exported or written there.
- A renamed or reordered gallery entry must keep pointing at the same hash.
- An orbit view that looks good says nothing about the fixed game camera. Make the representative scene early enough to affect selection.
