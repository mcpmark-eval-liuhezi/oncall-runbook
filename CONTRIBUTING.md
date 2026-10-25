# Contributing to the On-call Runbook

The runbook is only as good as its last update. Teammates are encouraged to
keep it current — here is how to propose a change.

## How to propose a runbook change

1. **Open an issue first** describing what you want to add or fix, so the team
   can agree on the approach before any writing happens.
2. **Create a branch** off `main` with a short, descriptive name
   (e.g. `add-rollback-guide`).
3. **Make your changes**:
   - New operational guides go in `guides/` as standalone markdown files.
   - Incident-response content belongs in `docs/runbook.md`.
   - Keep steps numbered, imperative, and concrete — assume the reader has
     just been woken up at 3 a.m.
4. **Open a pull request** into `main` with a short description of what
   changed and why, citing the head commit SHA so reviewers can verify exactly
   what they are reviewing.
5. **Get one approval** from a member of the on-call rotation, then merge.

## Ground rules

- Every page must stay actionable: checklists over prose.
- If you change who gets paged or how, update `README.md`, `RUNBOOK.md`, and
  `docs/runbook.md` together so they cannot drift apart.
- Emergency corrections to contact details or the escalation path may be
  pushed directly to `main`, followed by an issue explaining the change.

Questions or suggestions? Open an issue — that is always the right first step.
