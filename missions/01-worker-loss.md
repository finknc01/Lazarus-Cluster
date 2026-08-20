# Trial 01 — One Worker Falls

## Briefing
A compute worker disappears mid-job.

## Objective
Understand node failure detection, workload impact, replacement/retry semantics, and capacity degradation.

## Build
Use a small Kubernetes or Slurm-style lab, whichever you reach first in the learning plan. Run several jobs/tasks across at least two simulated workers.

## Failure
Stop or isolate one worker. Record when the controller notices, what happens to running work, what happens to queued work, and how remaining capacity changes.

## Evidence
- before/after node state
- detection time
- job fate table
- recovery steps

## Victory condition
You can distinguish recovery of the cluster control plane from recovery of the lost workload.
