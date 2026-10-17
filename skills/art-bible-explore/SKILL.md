---
name: art-bible-explore
description: Design and run bounded comparisons of artistic directions or generation models from a project's art bible. Use for early exploration of an asset, for a specific unresolved property, or to compare models on the same brief; later passes keep the properties already accepted.
license: MIT
metadata:
  author: Spencer MacBeth
  version: "0.3.0"
---

# Explore distinct directions

A pass answers one question. Early on, the question is "which of several quite different things should this be?"; later, "with the silhouette fixed, which material?". This skill designs the comparison, runs the authorized batch and hands the candidates to review with their records intact.

Existing authorization and budget apply; this skill adds no permissions.

## 1. Read the question

From the bible, the task brief and the reference annotations: what is being tested, what stays fixed, which bible revision the task reads from and where its outputs go.

## 2. Design the comparison

**Early exploration** varies the dimensions that matter: silhouette, composition, material, palette, movement, sound. State how each candidate differs and why all of them still do the asset's job. Five cosmetic variations of one interpretation feel like a search but are not one; the owner ends up choosing between 5% differences without seeing the alternative that would have excited them more.

**Later passes** hold the accepted properties fixed and vary the unresolved ones. Reopen an accepted property only for a reason tied to the task or to evidence, and say so.

**Model comparison** holds the brief and the review conditions constant and configures each model appropriately. If direction and model both vary in one batch, say which conclusions the result can support. Record which controls differ between endpoints; a parameter called `seed` on two models need not mean the same thing.

Write the matrix before generating: candidate ID, hypothesis, input reference IDs, provider/model, explicit parameters, review target. Choose the candidate count from the decision and the budget; four is a common first batch, not a rule.

## 3. Run the batch

Use the permissions and budget the task brief states. For shared paid work, identify this task’s allocation within the shared cap; do not treat the whole cap as each worker’s allowance. Pending and uncertain requests count against the allocation until reconciled. If a cost or access decision is missing, finish the briefs and the estimate, then ask for that decision.

Read the provider's current documentation for formats, controls, cost and limits, and resolve unsupported parameters before submitting. Keep the API key in the calling process or secret store; check that it is set without printing it, and keep it out of frontend code, manifests and feedback exports.

Record every job as described in [the job and artifact record](references/job-record.md). For queued providers, separate submission from collection and persist the provider's job ID before polling. Stop at the agreed batch or spending boundary; when results are unattractive, go back to the review question and the remaining budget rather than generating until something looks good.

Verify each returned artifact (decode the image, load the geometry, check the duration), keep the original, and save inspectable errors and partial results instead of silently replacing a failed candidate.

For image-to-3D, obtain concept acceptance at the intended scope before spending on reconstruction, when that is the agreed process. Inspect the original model and any optimized derivative separately.

## 4. Hand off

Deliver the candidate matrix, stable local artifact paths and hashes, the request settings actually used, the completed, failed and uncertain jobs, and the cost with any unknowns marked. State what the comparison is meant to decide. Everything is unaccepted until the owner's feedback says otherwise.

For copyable starting requests, see [exploration and model-connection prompts](references/prompts.md).

## Gotchas

- A timeout or empty job-history lookup does not prove non-acceptance. Keep the request `submission-uncertain` until reconciled. Retry only through the provider’s documented idempotency mechanism or after confirming the original was not accepted; otherwise another charge needs an explicit decision.
- A 200 response is not a usable file. Decode it before recording success.
- The numeric seed and the creative seed are different things. The catalog holds the second; the job record holds the first.
- Providers change. A saved request may not reproduce the same output later, so the output is the record, not the request.
