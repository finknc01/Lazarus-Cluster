# Trial 05 — Configuration Rot

## Briefing
Nothing failed suddenly. The cluster simply drifted until identical nodes stopped being identical.

## Objective
Use configuration management and validation to detect and repair drift.

## Failure
Change several harmless lab settings outside automation: service state, package, file permission, config value, or host entry. Do not record the changes in the intended-state files.

## Tasks
Run validation to detect differences. Use Ansible/scripts/declarative configuration to converge the nodes. Verify idempotency with a second run.

## Evidence
- intended-state declaration
- drift report
- convergence output
- second-run/idempotency evidence

## Victory condition
The cluster can recover from undocumented manual changes without relying on operator memory.
