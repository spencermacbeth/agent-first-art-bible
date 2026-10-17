---
name: art-bible-review
description: Implement, run and open a local taste-pass interface for reviewing artistic alternatives and saving feedback. Use when the user asks for a gallery, model viewer, sound or video comparison, writing/UI review, or wants an existing taste pass reopened or updated.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.4.0"
---

# Build and open the taste pass

Deliver a working review interface in the user's project, loaded with the actual candidates. Implement it, start it, exercise it and give the user a link they can open. A design document, a list of filenames or a screenshot of a form does not complete this task.

## Choose a useful presentation

Read the request, references, existing candidates and any relevant art-bible guidance. Establish what the user is comparing: broad directions, one property, generation models or how assets work together in the game.

Reuse an existing taste pass when it fits. Otherwise build a local web app using the project's stack or a suitable lightweight approach. Use an engine-native review scene when the question depends on shaders, lighting or behavior that a web viewer cannot reproduce. The package provides instructions; write the required application code in the user's project.

Build the rendering environment along with the form. Images need enough detail to inspect; models need working materials, lighting, scale and camera controls; sound and video need playback. Use [the media guide](references/media-review.md) for the media in this pass. A model thumbnail is not a substitute when the user needs to orbit the model.

## Make feedback easy

Give each candidate a clear name, its relevant seed references and a short explanation of the direction. Present candidates together or make switching between them easy. Hold viewing and playback conditions consistent enough for a useful comparison.

Put feedback beside the work. Useful defaults are notes about what to keep, what to change and an overall preference. Add ratings, ranking or comparison-specific questions when they help; do not require the user to fill every field. Support references, marked-up images or sketches when those are part of how the user is giving feedback. Preserve their actual words.

Use plain labels. The interface should help the user judge art, not ask them to manage hashes, job statuses or approval schemas. Technical generation details can be available without dominating the page.

## Get the feedback back to the agent

Choose a real path from the form to the next iteration. Reuse project-local file persistence when available. A local browser app can save notes in browser storage and provide a downloadable export for the user to return. Make clear which mechanism is in use; browser storage alone is not accessible to a later coding session.

Tie feedback to the candidate revision, retain earlier rounds and avoid carrying approval onto changed media. Provide import or recovery when using feedback exports. [Feedback guidance](references/feedback-contract.md) describes what to carry into the next pass.

## Run it and check it

Start the app with the project's normal command, or serve the local files. Keep the server available for review, then open it using the available browser tool. If browser opening is unavailable, verify the local response and provide the URL and start command, stating what was not checked.

In an isolated test profile, inspect an actual candidate of each included type. Exercise relevant zoom, orbit or playback controls. Enter a note, reload, and verify it survives. Export it and check that the agent can read the candidate and note; test import when provided. Keep test feedback out of the user's notes.

Finish with the working URL, what is ready to review and one short instruction for returning feedback. Repair broken assets and controls before handing it over. Stop for the user's artistic judgment, then use the saved feedback to produce the next pass.

## When the game itself matters

For integration questions, show the work with the real gameplay camera, neighboring assets, interface and sound. If device access is already authorized, use the project's connection to inspect the running game and capture the result. Preserve saves and unrelated sessions. Agent captures and measurements complement the user's own playthrough; they cannot tell you how the controls feel or whether the experience works for them.

[Example review and runtime requests](references/prompts.md).
