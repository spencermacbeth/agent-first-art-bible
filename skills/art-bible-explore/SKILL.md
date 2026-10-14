---
name: art-bible-explore
description: Design and execute bounded comparisons of artistic directions or generation models using a project's art bible. Use for early exploration or a specific unresolved property; preserve properties already accepted in a later refinement pass.
license: MIT
---

# Explore distinct directions

Read the current bible, task brief and relevant seed annotations. Identify the question being tested and the properties that must stay fixed.

## Choose the comparison

Early exploration should vary substantial dimensions such as silhouette, composition, material, palette, movement or sound. Explain how each direction differs and why all still address the same asset role. Several cosmetic variants of the same interpretation do not establish a broad search.

Later passes should preserve accepted properties and vary the unresolved ones. If the owner approved the silhouette, do not reopen it without a reason tied to the task or observed evidence.

When the question is model choice, use representative project tasks and comparable review conditions. Record which controls differ across endpoints. A random seed or similarly named setting need not have equivalent semantics across models. If direction and model both vary, explain which conclusions the comparison can and cannot support.

Prepare a compact matrix of candidate ID, artistic hypothesis, input reference IDs, provider/model, explicit parameters and review target. Adapt candidate count to the decision and budget; do not impose a universal batch size.

## Run the authorized batch

Use existing provider permissions and budget without asking again. When cost or access is missing, complete the briefs and estimate before requesting the missing decision. Read current official endpoint documentation for formats, controls, costs and limits. Resolve unsupported parameters before submitting.

Keep the API key in the calling process or secret store. Verify availability without printing the value. Do not put it in frontend code, manifests or feedback exports.

Follow [the job and artifact record](references/job-record.md). Separate submission from collection for asynchronous jobs. Persist provider request IDs and reconcile uncertain submissions before retrying; a timeout is not proof of failure. Stop at the agreed batch or spending boundary. Do not continue generating until an attractive result appears without checking the remaining budget and review question.

Preserve originals and verify returned artifacts. A completed HTTP request does not establish that a downloaded file is a usable image, model, video or sound. Save inspectable errors and partial outcomes rather than silently replacing failed candidates.

For image-to-3D workflows, obtain concept acceptance at the intended scope before using it for a costly reconstruction when that is the agreed process. Inspect the original model and any optimized derivative separately.

## Hand off for review

Supply the candidate matrix, stable local artifact paths, actual request settings, completed/failed/uncertain jobs and cost accounting with unknown costs identified. State what the comparison is intended to decide. Keep all candidates marked unaccepted until the owner's feedback establishes otherwise.
