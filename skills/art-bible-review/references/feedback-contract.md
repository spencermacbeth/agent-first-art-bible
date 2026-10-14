# Feedback that survives the review

The storage format is a project choice. Whatever representation you use, preserve these meanings:

- A candidate ID refers to a particular artifact revision, ideally identified by a content hash. Sorting or renaming a gallery entry must not change the target of a note.
- The pass states a question and records the viewing conditions relevant to that question.
- Keep/change notes distinguish accepted properties from unresolved ones.
- Acceptance names its scope. A liked concept is not automatically an approved reconstruction, animation or shipping asset.
- Review status distinguishes the owner's feedback from an agent recommendation or technical check.
- Export contains the candidate identities, relevant settings, notes and decisions needed by another session. It contains no credential values or private signed URLs.

On import, validate the structure and referenced candidate identities. Do not attach feedback to a different artifact merely because a filename matches. Show conflicts, unknown candidates and stale revisions for explicit resolution. Preserve the existing feedback until a replacement is deliberately accepted.

Local browser storage is convenient but is scoped to the browser and origin, and can be cleared. Provide an export, or use project-local persistence if required. Do not imply that a browser save has reached the repository or another device.

When producing an execution brief, separate:

1. Changes authorized by explicit feedback.
2. Accepted properties that must survive those changes.
3. Questions that need another review.
4. Verification required at the concept, artifact or runtime level.

Keep quotations distinguishable from interpretation. A score alone does not authorize promotion to the active bible.
