# Trial 00 — Define Survival

## Briefing
Management says Lazarus must be “highly available.” Nobody agrees what unavailable means.

## Objective
Define services, dependencies, acceptable data loss, recovery targets, and validation checks before inducing failures.

## Tasks
Map users → entry point → scheduler/control plane → workers → network/DNS → storage/state → monitoring. Assign simple RTO/RPO targets to the fictional service. Identify stateless vs stateful components and what can be rebuilt from Git.

## Challenge
Remove one dependency from your diagram and explain what still works and what does not.

## Evidence
- dependency graph
- RTO/RPO table
- validation checklist
- source-of-truth inventory

## Victory condition
You have an objective definition of “recovered” that can be tested later.
