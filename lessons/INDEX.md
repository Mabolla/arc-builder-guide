# Lessons Index

This index turns real project experience into reusable Builder knowledge.

## Rule

A lesson belongs here only when it comes from an actual project, verified investigation, or a reproducible failure/fix. Avoid speculative rules.

## Current lessons

### L001 — Narrow the milestone
**Source:** Arc PayLink

Keep the implemented milestone smaller than the full product vision. Explicitly label future integrations as future work.

### L002 — Submission is not settlement proof
**Source:** Arc PayLink

A successful SDK call or submitted transaction is not sufficient evidence that the requested payment completed. Verify the destination transaction and expected token transfer.

### L003 — Financial workflows need explicit state
**Source:** Arc Escrow

Escrow-like products should model agreement, funding, evidence, validation, settlement, and refund states explicitly so asynchronous events and recovery paths are visible.

### L004 — Secrets stay server-side
**Source:** Arc Escrow

Circle credentials, entity secrets, private keys, and AI API credentials must never be committed or exposed to browser code. Public identifiers must be distinguished from secrets.

### L005 — Document provenance honestly
**Source:** Arc Escrow

When a project is based on an existing sample, fork, or upstream repository, record that provenance. Do not present inherited code as original work without verification.

## How to add a lesson

Use this minimum format:

- **Problem:** what happened.
- **Evidence:** where it was observed or verified.
- **Cause:** what was confirmed, not guessed.
- **Fix:** what worked.
- **Reusable rule:** what future projects should do differently.
- **Source project:** link to the relevant project.
