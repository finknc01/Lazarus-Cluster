# Trial 04 — State Is the Problem

## Briefing
Recreating processes is easy. Recreating lost state is not.

## Objective
Identify persistent data, configuration, scheduler metadata, artifacts, and what backups/snapshots are actually needed.

## Build
Create a small stateful dependency: shared lab storage, scheduler metadata, or application state. Back it up using a documented method.

## Failure
Delete or corrupt only the disposable copy, then attempt recovery. Measure how much work/data is lost relative to the fictional RPO.

## Evidence
- state inventory
- backup/restore commands or automation
- measured recovery time
- actual vs target RPO/RTO

## Victory condition
You can prove a restore works; “we have backups” is not accepted as evidence.
