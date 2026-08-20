# Trial 06 — Burn It Down

## Briefing
The recovery team receives new blank lab VMs. Pretend the old cluster is unrecoverable.

## Objective
Recreate the minimum viable cluster from repository-controlled artifacts.

## Rules
Do not copy hidden configuration from the old nodes. Use only documented prerequisites, automation, backed-up state, and explicit secrets placeholders.

## Tasks
Provision nodes, restore required state, reconnect networking/DNS, start control services, join workers, deploy a test workload, and run the Trial 00 validation checklist.

## Evidence
- rebuild runbook
- automation source
- elapsed recovery time by phase
- manual steps that remain
- failures encountered during rebuild

## Victory condition
The repository, not the original machine, is the primary source of truth for the lab environment.
