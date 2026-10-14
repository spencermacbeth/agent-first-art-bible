---
name: art-bible-review
description: Build or adapt a taste-pass interface and rendering environment for reviewing images, 3D models, video or sound. Use when candidates need comparable inspection, persistent feedback or evidence from the target runtime or device.
license: MIT
---

# Build a useful taste pass

Read the task question, current bible, candidate records and existing review tools. Choose the interface around the decision the owner needs to make. Preserve existing notes and accepted assets when reopening a pass.

## Choose the rendering environment

Use [the media review guide](references/media-review.md) for the media involved. Prefer the project's actual renderer for questions about integration. A gallery or standalone viewer can answer candidate questions without proving runtime behavior.

Choose a stack that can load the required formats, retain feedback and run where the owner reviews. Reuse the existing web stack when suitable; use an engine-native review scene when materials, camera or lighting depend on that engine. Explain any preview approximation that changes the comparison. Avoid introducing a database when a local export meets the persistence need.

Put camera, light, scale, playback gain and other comparison settings under explicit control. Preserve raw masters when making compressed, normalized or simplified viewing copies. Fix the presentation conditions before attributing a difference to a model.

## Keep decisions attached to their artifacts

Follow [the feedback contract](references/feedback-contract.md). Show stable candidate IDs and the question for the pass. Provide fields for properties to keep, changes to make, unresolved questions and the scope of any acceptance. Ratings can assist sorting; specific notes guide implementation.

Support export and restoration of feedback. Tie notes to the artifact revision so a regenerated asset cannot silently inherit approval. Keep prior versions accessible when they remain useful to the comparison. Handle missing assets, unsupported formats and damaged saved state visibly.

Keyboard controls, readable labels and a layout appropriate to the owner's viewing device are part of a usable review. Do not autoplay sound. Video controls should support seeking; time-stamped notes help locate an edit. Use the project's accessibility and reduced-motion requirements.

## Observe the actual target when needed

For device-sensitive work, use an existing authorized connection and isolated test profile. Preserve player saves and unrelated sessions. Keep debugging services local or behind an authenticated tunnel. Do not infer deployment permission merely from SSH access.

Record the actual build, asset revision, camera/display/playback conditions and observations. Distinguish native device evidence from a desktop preview. Synthetic controls and frame captures do not establish physical controller feel, audio quality or enjoyment; those remain owner review questions where relevant.

## Verify the review works

Exercise one real candidate of every included media type, seeking or orbit controls, feedback persistence/export and reopening the same revision. Check the intended screen size. Verify links to full-resolution masters. Use a disposable browser/profile for test notes so validation does not contaminate the owner's feedback.

Deliver the local review URL or scene, the export location, relevant rendering settings and explicit limitations of the preview. Technical checks do not constitute the owner's artistic approval.
