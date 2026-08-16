# Verification Workflow

Verification is a separate stage from implementation.

## Application

- [ ] Build succeeds.
- [ ] Typecheck succeeds when applicable.
- [ ] Core user flow works locally.
- [ ] Error states are understood.

## Blockchain

- [ ] Transaction request was submitted.
- [ ] Transaction was mined/confirmed.
- [ ] Relevant receipt or explorer evidence was checked.
- [ ] Intended state change was independently verified.
- [ ] Network and contract addresses match the current project configuration.

## Deployment

- [ ] Production build succeeds.
- [ ] Required environment variables are configured without exposing secrets.
- [ ] Deployed application loads.
- [ ] Critical flow works against the intended network.

Record evidence and remaining limitations in the project case study.
