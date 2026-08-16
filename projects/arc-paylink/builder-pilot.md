# Arc PayLink — Builder Guide Pilot

**Date:** 2026-08-16
**Guide:** `ARC_BUILDER_AI_GUIDE.md` v0.1
**Project:** `Mabolla/arc-paylink`
**Test type:** static methodology pilot; no product code changed

## Purpose

Apply the shared Builder operating guide to a real existing Arc project and check whether the guide produces useful, disciplined conclusions without expanding scope or inventing facts.

## Evidence inspected

- Project repository metadata and default branch.
- `README.md`.
- `ARC_BUILDER_CONTEXT.md`.
- `package.json`.
- Existing documented testnet milestone and transaction evidence in the project README.

## Results

### 1. Understand — PASS

The project-local context and README clearly distinguish the current proven milestone from planned cross-chain work. The current proven path is same-chain Arc Testnet USDC payment; Base Sepolia → Arc and Unified Balance are described as planned/stretch work.

### 2. Scope discipline — PASS

The project explicitly limits the current milestone and states that Base Sepolia bridging, CCTP, and Unified Balance are not part of the current source milestone. The guide therefore must not treat the broader product vision as implemented functionality.

### 3. Verification discipline — PASS

The README documents a successful 1 USDC Arc Testnet transaction and an explicit fulfillment rule: successful destination transaction plus exact official-USDC transfer to the requested recipient and amount. This matches the Builder rule that SDK/client success is not sufficient final proof.

### 4. Secret handling — PASS (static evidence)

The documented local flow requires no API key, private key, seed phrase, or database. The project context also explicitly prohibits committing secrets. This is a static documentation check, not a secret-scanning result.

### 5. Change discipline — PASS

The project-local context instructs an AI agent to inspect existing code, preserve working behavior, make the smallest safe change, and run narrow checks before broader checks. This is directly aligned with the shared guide.

### 6. Testability — PARTIAL / REQUIRES RUNTIME

`package.json` exposes `lint`, `test`, and `build` scripts, which gives the methodology a concrete verification surface. However, this GitHub-only pilot did not execute those commands. Runtime results must be recorded separately before claiming current build health.

### 7. Current-state contradiction check — ACTION REQUIRED

The README contains both a narrow current milestone and a broader product goal that describes the intended future cross-chain route. This is not a code contradiction, but it is a documentation hazard. Future Builder agents must use the explicit `Current Milestone` and `Out of scope` sections as the implementation boundary and must not infer that the cross-chain path is already implemented.

## Pilot verdict

**PASS for methodology application; runtime verification pending.**

The guide successfully tells the Builder to:

- distinguish current implementation from product vision,
- preserve a working milestone,
- verify payment fulfillment on-chain,
- avoid guessing Arc-specific facts,
- avoid exposing secrets,
- and separate static evidence from runtime evidence.

No change to `arc-paylink` was required for this pilot.

## Next verification step

Run the project's own checks in its working environment:

```bash
npm install
npm run lint
npm test
npm run build
```

Then perform the documented same-chain Arc Testnet payment flow and record fresh transaction/explorer evidence. Only after those checks should the pilot be promoted from **static methodology PASS** to **runtime-verified PASS**.

## Reusable lesson

**A Builder Guide can be tested without modifying the product:** first apply it as a static audit, explicitly mark what cannot be verified from GitHub alone, then require runtime evidence before declaring the project healthy.
