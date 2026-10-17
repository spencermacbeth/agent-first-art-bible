# Reviews

One directory per pass, named `<family>-<question>-<nn>`. Each holds:

- `task.md` — the brief: question, fixed properties, bible revision, output location, budget, review target
- `jobs.md` — job and artifact records: candidate, request, execution, output, derivative
- `candidates/` — original outputs; review derivatives under `candidates/derived/`
- `feedback.json` — exported review notes tied to artifact hashes
- `decision-NNN.md` — accepted scope, evidence, superseded direction, the bible update

Nothing in `reviews/` is current direction until a decision links it from the bible.
