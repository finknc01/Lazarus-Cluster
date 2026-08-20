# Lazarus-Cluster

> **The cluster is going to die. Decide how much can fail, how fast it can recover, and whether it can be rebuilt from source-controlled truth.**

## Project status

| Field | Current state |
|---|---|
| **Status** | **Planned — resilience work begins in Weeks 29–30 and re-enters later blocks** |
| **Current stage** | Campaign authored; no recovery time, RTO/RPO result, or rebuild is claimed complete |
| **Lab environment** | Laptop-scale VMs/containers/lightweight cluster components; production-scale behavior is not implied |
| **Evidence rule** | Recovery counts only when intended function is validated after failure; “service started” is not enough |
| **Last plan sync** | 2026-08-19 |

## Purpose

Lazarus-Cluster is the resilience/disaster-recovery lab. The fictional cluster must prove that it can recover **before** anyone is allowed to depend on it.

The campaign deliberately removes workers, networking/DNS, control-plane pieces, state, configuration, and finally entire hosts.

> **What survived? What recovered automatically? What had to be rebuilt, from what source of truth, and how long did it take?**

## Skills developed

- multi-node/service dependency reasoning
- worker and control-plane failure handling
- DNS/network/storage dependencies
- persistent vs replaceable state
- configuration drift and idempotency
- backups/recovery boundaries
- RTO/RPO definition and measurement
- rebuild automation, runbooks, validation, and postmortems

## Resurrection campaign

The files in [`missions/`](missions/) are authoritative.

| Trial | Failure / objective | Primary outcome |
|---|---|---|
| [00 — Survival](missions/00-survival.md) | Define service, dependency, RTO/RPO, and validation expectations | recovery acceptance criteria |
| [01 — Worker Loss](missions/01-worker-loss.md) | Remove a worker and restore usable capacity | node-lifecycle evidence |
| [02 — Network / DNS](missions/02-network-dns.md) | Break service discovery/connectivity and isolate the failed path | network/DNS recovery evidence |
| [03 — Control Plane](missions/03-control-plane.md) | Remove or disrupt a scheduler/control component | control-plane recovery reasoning |
| [04 — State / Storage](missions/04-state-storage.md) | Determine which state is replaceable versus irreplaceable | state/recovery boundary map |
| [05 — Configuration Drift](missions/05-config-drift.md) | Create drift and return systems to declared state | idempotency/configuration evidence |
| [06 — Full Rebuild](missions/06-full-rebuild.md) | Recreate the minimum viable cluster on blank lab hosts | source-controlled rebuild + elapsed recovery phases |
| [Final — Red Dawn](missions/final-red-dawn.md) | Recover from a compound failure under defined objectives | complete RCA + RTO/RPO result |

## Recovery rule

A green ping or running service is not sufficient. Each trial should validate the system's intended function, for example:

- required nodes/services reachable
- DNS/service discovery correct
- scheduler sees expected resources
- workload can actually run
- required state/storage is available
- monitoring sees the recovered component
- configuration matches declared state

## Evidence standard

Each trial should capture the starting state, failure introduced, detection path, dependency that actually broke, recovery sequence, elapsed time, validation checks, manual steps, and improvement to automation/runbooks.

Destructive work belongs only in disposable lab VMs/containers/namespaces.

## Completion condition

Lazarus-Cluster is complete when repository-controlled configuration, documented state, and recovery procedures—not an original snowflake machine—are sufficient to restore the lab's intended function under a compound failure.
