# Reviews

If the project has no review layout, a directory per pass such as `<family>-<question>-<nn>` is a useful starting point. Keep only the records the pass needs; adapt filenames and storage to existing tools. For example:

- `task.md` — the brief: question, fixed properties, bible revision, output location, budget, review target
- `jobs.md` — job and artifact records: candidate, request, execution, output, derivative
- `candidates/` — original outputs; review derivatives under `candidates/derived/`
- `feedback.json` — exported review notes tied to artifact hashes
- `decision-NNN.md` — accepted scope, evidence, superseded direction, the bible update

Nothing in `reviews/` is current direction until a decision links it from the bible.
