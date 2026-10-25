# On-call Runbook

This repository is the home for the team on-call runbook: incident-response
procedures, escalation paths, operational guides, and the follow-up tracking
that goes with them. It is the canonical location for everything an on-call
engineer needs during a rotation.

## What lives here

| Path | Purpose |
| --- | --- |
| `README.md` | This overview and the escalation policy |
| `RUNBOOK.md` | Quick-reference runbook with the contact roster |
| `docs/runbook.md` | Full incident-response runbook (alert triage, escalation, handover notes) |
| `guides/` | Step-by-step operational guides, starting with the rollback procedure |

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose changes.

## Escalation

**Who gets paged first: the on-call lead (the primary on-call engineer for the
current rotation).** Every alert pages them first, 24/7. They own the initial
triage and the decision to escalate.

The full ladder, in order:

1. **On-call lead (primary on-call engineer)** — paged first for every alert.
   They acknowledge, triage, and either resolve or escalate.
2. **Backup on-call engineer** — paged automatically if the primary has not
   acknowledged within 15 minutes.
3. **Engineering manager** — paged if the incident is still unresolved after
   30 minutes, or immediately for customer-impacting or security-sensitive
   incidents.
4. **External/vendor contacts** — engaged only by the engineering manager, in
   line with the contact roster in `RUNBOOK.md`.

When in doubt, escalate early rather than late. The current contact roster is
maintained in `RUNBOOK.md`, and the detailed escalation procedure in
`docs/runbook.md` (issue #4 tracks filling in the full ladder).
