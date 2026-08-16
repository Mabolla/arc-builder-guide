# Case Study — Arc Escrow

## Role in the Builder Guide

Arc Escrow is an Arc testnet workflow example in the Mabolla portfolio and a useful case study for studying a more stateful, backend-heavy Arc application.

## What the repository contains

The current repository describes a workflow escrow/refund protocol for freelance agreements using USDC on Arc testnet. It combines Next.js, Supabase, Circle Developer Controlled Wallets, Circle smart-contract tooling, Circle webhooks, and OpenAI-based deliverable validation.

The documented flow is:

1. create an agreement,
2. fund the escrow,
3. submit a deliverable,
4. validate the work against agreement criteria,
5. release funds or refund them.

The repository also documents local Supabase and webhook development paths and an agent-wallet generation step.

Source repository: https://github.com/Mabolla/arc-escrow

## Builder lessons

1. Stateful financial workflows need an explicit state machine, not only a happy-path UI.
2. Wallet operations, database state, webhook events, and application decisions must have clear ownership and recovery rules.
3. Server-side secrets such as Circle credentials and OpenAI credentials must stay outside client code and version control.
4. Webhook signature verification belongs in the security boundary.
5. Local webhook testing needs a reproducible public callback path.
6. AI validation is a decision component inside the workflow; it should not silently become the authority for financial settlement without explicit application rules.
7. Production readiness is a separate milestone from a testnet demonstration.

## Reusable pattern

**Agreement → funding → evidence → validation → deterministic settlement/refund**

This pattern can inform future programmable-money applications that require conditional settlement.

## Important provenance note

This case study summarizes the current repository documentation. It does not claim that every component is an original implementation by Mabolla or that the repository is production-ready. Provenance and implementation ownership should be checked before presenting this project as an original protocol contribution.

## Status

Case study captured from the repository state reviewed on 2026-08-16.
