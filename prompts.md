# Prompt fragments

Replace the braced values with your project's paths and decisions. Each fragment describes one task; use the ones relevant to the current pass. Existing instructions, approvals and budget remain in force.

## Establish the resource

```text
Read the existing art direction and project instructions. Organize the
authoritative art bible around {asset family}. Preserve accepted work.
Identify the current references, fixed constraints, open decisions and
the scene or playback setup used to inspect results. Annotate my drawings,
photos and recordings in {reference directory} with what each contributes.
Distinguish creative reference seeds from numeric generation seeds.
Add a short pointer to the bible in the harness's project instructions.
```

## Explore broad directions

```text
Using {bible section} and {reference IDs}, propose four substantially
different directions for {asset role}. Vary silhouette, spatial structure,
material and atmosphere. Keep {gameplay constraints} fixed. Explain what
each direction tests; avoid four cosmetic variations of the same object.
Give each a stable candidate ID and a brief I can compare before generation.
Use the authorized batch budget in {task brief}; if none is set, stop at
the briefs and cost estimate. Keep all candidates separate from accepted work.
```

Four is an example batch size. Choose a count that exposes meaningful alternatives within the task's budget.

## Connect generation models

```text
Implement a local generation adapter for {provider and model choices}.
Read the current official API documentation. Credentials are available
through {environment variable names}; check presence without printing values.
Record the endpoint/model, actual parameters, reference IDs and output hashes.
Separate submission and collection for queued jobs. Reconcile uncertain
submissions before retrying. Keep keys out of the review app and its exports.
Compare models on {representative task} under the same review conditions.
Use the existing authorization and budget in {task brief}.
```

## Build the taste pass

```text
Build or adapt a local taste pass for {candidate directory}, using the
project's existing stack where it suits these media. Include stable IDs,
full-resolution inspection, relevant generation settings, Keep/Change notes
and acceptance scope. Save feedback and support export/import without
attaching old approval to a changed artifact. For {media types}, provide
the controls needed to inspect the actual issue. Compare candidates under
{camera, lighting, scale, gain or playback conditions}. Preserve previous notes.
```

## Inspect the runtime

```text
Put {candidate IDs} in {production scene or playback event}. Use the
actual camera, lighting, scale, UI and interaction constraints from the bible.
If target-device inspection is authorized, use {existing connection} and an
isolated QA profile. Preserve player saves and unrelated sessions. Capture
the result and record the build, artifact revisions and relevant measurements.
Distinguish observed device behavior from preview assumptions, and identify
anything that still needs physical controls, listening or human play.
```

## Refine a specific property

```text
Read {feedback file} against the exact candidate revisions it names.
Retain {accepted properties}. Change {unresolved property} and explain
which stage needs correction: generation, geometry, placement, lighting,
audio/editing or presentation. Create a new revision, preserving the baseline.
Do not infer that a liked concept is an approved runtime asset. Reuse passing
evidence only where the artifact and relevant conditions are unchanged.
Return the revised result in the same review conditions.
```

## Record the accepted direction

```text
Apply my acceptance in {feedback file} to {bible section}. Record the
selected artifact IDs and hashes, accepted properties, review conditions,
production recipe and remaining issues. Mark conflicting older guidance as
superseded while retaining its reason and reference. Keep approval scoped to
what I reviewed. From the normal project instruction entry point, verify that
a new task can find the current direction and the place to inspect its result.
```

## Turn a play session into tasks

```text
Read {recording or timestamped transcript} from my play session of {slice or
build}. Turn each thing I noticed into a follow-up task that points to the
moment in the recording, describes what I experienced in my words, and names
what needs investigation. Keep my observation as the problem to solve;
investigate hierarchy, timing, cues or the asset itself before proposing a
fix. Send changes to the shared direction to {bible section} through a review;
keep local implementation fixes with the relevant task. End with the list of
what I should play again to check each change.
```

This fragment follows a vertical slice: enough of the art, writing, interface, music and sound in one playable sequence for the owner to experience how they work together. Human play is how the combined look and feel gets judged; the agent's job here is to turn what was said aloud into work without deciding the fix too early.
