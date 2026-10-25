# Rollback Procedure

Use this guide when a recent change is breaking production and the fastest
path to recovery is to undo it. Follow the checklist in order — do not skip
steps, and do not attempt a rollback without a second pair of eyes on the
console.

## Checklist

1. **Freeze deployments.** Stop all in-flight deploys and disable auto-deploy
   for the affected services so nothing else lands mid-rollback.
2. **Declare the incident** in the on-call channel and note the offending
   change, the time it landed, and the symptoms observed.
3. **Confirm the last known good release** by checking the deployment history
   for the most recent healthy state before the bad change.
4. **Roll back the deployment** to the last known good release using the
   standard deploy pipeline (same mechanism that shipped it, in reverse).
5. **Roll back the data/migration changes** if the release included schema or
   data migrations, and record whether they were reversible or forward-fixed.
6. **Verify recovery** against the health checks, error rates, and key user
   journeys — confirm the original symptoms are gone.
7. **Unfreeze deployments** once verified healthy, and re-enable auto-deploy.
8. **Write up the postmortem** covering the root cause, the rollback decision,
   and any follow-up work, and file it as an issue in this repo.

## Notes

- If verification fails after rollback, escalate immediately per the
  [escalation ladder](../README.md#escalation) — do not attempt a second
  rollback without involving the engineering manager.
- The current contact roster lives in `RUNBOOK.md`.
