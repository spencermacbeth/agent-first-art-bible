# Job and artifact record

Use the project's existing representation. A Markdown table plus a request JSON file can be sufficient. Keep the following relationships recoverable:

| Record | Useful contents |
| --- | --- |
| Candidate | Stable ID, task/batch, artistic hypothesis, relevant bible section and reference IDs |
| Request | Provider, exact endpoint/model identifier, submitted parameters, prompt, input artifact IDs and request digest |
| Execution | Provider job ID, submission time, current status, collection attempts, errors, quoted and actual cost where available; task allocation when sharing a budget |
| Output | Original local path, content hash, file type, dimensions/duration or geometry/material metadata |
| Derivative | Source artifact hash, transform/tool version and settings, derivative path and hash |
| Review | Candidate and artifact identity, review conditions, feedback reference and acceptance scope |

Keep numeric random seeds separate from creative reference IDs. Record unsupported or omitted controls rather than inventing defaults. Preserve original provider outputs even when the provider may not reproduce identical results later.

Before a paid request, create a local pending record. After submission, save the provider's job identity before polling. If the connection fails in between, use the provider's supported history or idempotency mechanism where available. If a matching job is found, collect it. Retry only through a documented idempotent mechanism or after authoritative confirmation that the original was not accepted. An empty or incomplete history is inconclusive: retain `submission-uncertain` and its budget allocation rather than creating a fresh charge automatically.

Keep temporary or signed download URLs in private job state only when needed for collection. Durable review records should use local artifact identities. Redact credentials, authorization headers and provider URLs containing access tokens from shared exports.

Collection checks should match the medium: decode image/video/audio files, inspect expected tracks and duration, or load model geometry/materials. An artifact can pass these checks and still fail artistic or runtime review.
