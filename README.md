# Mabolla Arc Builder Guide

> A living builder system for designing, building, verifying, documenting, and reusing Arc projects.

## Mission

We do not build isolated demos. Every project should produce reusable knowledge that makes the next project faster, safer, and clearer.

**Build → Learn → Document → Reuse → Build Better**

## Builder Loop

```text
IDEA → RESEARCH → ARCHITECT → BUILD → TEST/DEBUG → VERIFY/DEPLOY → LEARN → DOCUMENT → REUSE → NEXT PROJECT
```

## Principles

- Verify Arc-specific facts against authoritative sources before implementation.
- Prefer official Arc/Circle tooling and documentation where applicable.
- Never guess current network settings, contract addresses, SDK APIs, or supported features.
- Treat transaction submission and transaction verification as separate steps.
- Build the smallest useful MVP first.
- Never commit secrets, private keys, API keys, or sensitive operational data.
- Record failures and decisions, not only successful outcomes.
- Convert reusable discoveries into guide material.
- Keep each project independently understandable while sharing the common methodology here.

## Repository Map

- `ARC_BUILDER_AI_GUIDE.md` — reusable AI operating instructions.
- `BUILDER_PRINCIPLES.md` — quality bar and project philosophy.
- `arc/` — Arc-specific knowledge and authoritative references.
- `workflows/` — repeatable build, test, debug, verification, and deployment workflows.
- `templates/` — reusable project planning and learning templates.
- `projects/` — real project case studies.
- `lessons/` — reusable lessons extracted from actual work.
- `troubleshooting/` — verified recurring failure modes and fixes.

## v0.1 Scope

This first release is intentionally small. We will grow it from real builds instead of filling it with speculative documentation.

## Status

**v0.1 — foundation**
