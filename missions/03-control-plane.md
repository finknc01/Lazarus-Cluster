# Trial 03 — Cut Off the Head

## Briefing
The workers still exist. The control plane does not.

## Objective
Understand which scheduler/orchestrator state lives in controllers, what workers can continue without them, and what must be restored first.

## Failure
Stop the lab controller/scheduler service or control-plane VM. Observe existing workloads, new submissions, state visibility, and monitoring.

## Recovery
Restore the controller from documented configuration. If your lab uses persisted state, document what is required to recover it.

## Evidence
- control-plane dependency map
- existing-vs-new workload behavior
- recovery timeline
- state that survived and state that did not

## Victory condition
You can describe the difference between data plane and control plane using observed failure behavior.
