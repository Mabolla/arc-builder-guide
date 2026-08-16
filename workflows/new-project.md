# New Arc Project Workflow

## 1. Define the outcome

Write the user problem, target user, success condition, and explicit MVP boundary.

## 2. Check ecosystem fit

Confirm why Arc and the selected Circle/Arc primitives are appropriate. If the fit is unclear, research before coding.

## 3. Verify current sources

Open the official Arc/Circle documentation relevant to the project. Confirm current network configuration, supported features, contract addresses, SDK/API signatures, and limitations.

## 4. Build the project context

Create the project's `train.md`, project flow, development steps, file structure, and decision notes. Link to the shared Arc Builder Guide rather than copying mutable facts everywhere.

## 5. Choose the smallest proof

Identify the minimum end-to-end behavior that proves the core idea with real testnet infrastructure.

## 6. Implement

Use official tooling where practical. Keep secrets server-side and keep custody/security assumptions explicit.

## 7. Verify

Run lint, tests, type checks, build checks, and the relevant live/testnet flow. For blockchain actions, verify the actual destination state instead of trusting only an SDK success response.

## 8. Deploy / demonstrate

Deploy only after the local and testnet path is repeatable. Capture non-sensitive evidence such as transaction hashes, explorer links, screenshots, or test results when appropriate.

## 9. Document

Update the project README with the actual implemented milestone, limitations, verification evidence, and known risks.

## 10. Extract lessons

Use `templates/lessons-learned.md`. Promote only evidence-backed, reusable lessons into `lessons/INDEX.md` or a dedicated troubleshooting guide.

## 11. Reuse

At the start of the next project, review the relevant promoted lessons before designing the new architecture.
