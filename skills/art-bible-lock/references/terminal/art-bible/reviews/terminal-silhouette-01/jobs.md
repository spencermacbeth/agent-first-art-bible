# Jobs: terminal-silhouette-01

Provider `example-provider`, model `example-image-model`, endpoint `v2/image/edit` (all fictional). Every request attached `ref-bracket-01` and `ref-stone-02-crop-a` as images and set `size: 1024x1024`, `reference_strength: 0.6`. This endpoint exposes no numeric seed, so none is recorded. Full request bodies are in `requests/<candidate>.json` beside this file (not included in the example).

| Candidate | Hypothesis | Prompt (abbreviated) | Request digest | Job ID | Submitted | Status | Cost | Output | Hash |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| terminal-a | Suspended instrument: asymmetric bracket, hanging body, painted metal | "A save terminal hung from an asymmetric bracket…" | `req-5d2f…` | `job_01HX…A` | 2026-09-30 14:02 | completed | 0.32 | `candidates/terminal-a.png` 1024² | `sha256:7c1e2b9a4f03…` |
| terminal-b | Stone archive marker: low monolith, recessed face, broad wear | "A low stone marker with a recessed face…" | `req-91ab…` | `job_01HX…B` | 2026-09-30 14:02 | completed | 0.32 | `candidates/terminal-b.png` 1024² | `sha256:0b44d1e7c2aa…` |
| terminal-c | Fabric signal post: canopy, exposed ribs, translucent panels | "A signal post with a ribbed fabric canopy…" | `req-c07e…` | `job_01HX…C` | 2026-09-30 14:03 | completed (reconciled) | 0.32 | `candidates/terminal-c.png` 1024² | `sha256:e9a17f30b6d5…` |

Total 0.96 of 2.00 authorized. Three further images were authorized and not used; the question was answered by three.

## Reconciliation note, terminal-c

The submit call for `terminal-c` timed out after 30 seconds with no response body. The pending record was marked `submission-uncertain` rather than retried. The provider's job history showed `job_01HX…C` accepted at 14:03:11, so the job was collected on the next run without a second charge. Had the lookup returned no matching job, the request would have remained `submission-uncertain`, with its estimated 0.32 still allocated. A missing history entry alone would not authorize another submission. Retry would require confirmed non-acceptance or the provider’s documented idempotent mechanism; unresolved risk of a second charge would need an explicit decision.

## Collection checks

Each PNG decoded at 1024×1024, three channels; hashes as above. Review derivatives `candidates/derived/<candidate>-512.webp` were made for the gallery with `example-encoder 1.4, quality 85`; their hashes are recorded in `feedback.json` beside each master hash. These checks say the files are usable images. They say nothing about whether any of them is right.
