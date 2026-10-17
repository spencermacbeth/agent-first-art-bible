# Prompt fragments

Use the fragments that fit the task, with the project’s actual references and existing instructions. These are starting points, not a required sequence.

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
