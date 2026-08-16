# Case Study — Arc PayLink

## Role in the Builder Guide

Arc PayLink is the first original Mabolla project used as a case study for the Builder methodology.

## What was built

A hackathon MVP for creating shareable USDC payment requests that settle on Arc Testnet and produce a verifiable receipt. The documented milestone supports same-chain Arc Testnet USDC payments; Base Sepolia bridging and other cross-chain work are explicitly future scope in the project's current README.

## Evidence in the project repository

The project README documents:

- a verified 1 USDC Arc Testnet payment,
- a transaction hash and ArcScan link,
- exact six-decimal USDC base-unit verification,
- local lint/test/build commands,
- the payment state model and receipt flow,
- explicit in-scope and out-of-scope boundaries,
- an Arc/Circle integration plan and known risks.

Source repository: https://github.com/Mabolla/arc-paylink

## Builder lessons

1. Keep the first milestone narrower than the complete product vision.
2. Treat a submitted transaction as progress, not proof of settlement.
3. Verify the destination transaction against the expected recipient and exact token amount.
4. Keep network-specific facts and contract addresses tied to authoritative documentation.
5. Preserve a concrete end-to-end test artifact so the project has evidence, not just code.
6. Document future integrations separately from implemented functionality so the README cannot accidentally overstate the MVP.

## Reusable pattern

**Intent → execution route → destination verification → immutable receipt**

This pattern is reusable for future payment-oriented Arc projects.

## Status

Case study captured from the repository state reviewed on 2026-08-16. This file is documentation, not a claim that every future version of Arc PayLink will retain the same implementation.
