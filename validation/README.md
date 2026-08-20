# Recovery Validation Contract

Define the checks that prove the cluster is useful **before** running destructive trials.

## Required validation categories

### Control plane
- Can the cluster API/control service be reached?
- Can desired state be submitted and observed?

### Scheduling
- Can a harmless workload be placed on an eligible worker?
- Can the system explain why an unschedulable workload is waiting?

### Networking and DNS
- Can workloads resolve required service names?
- Can the expected service path be reached?

### Stateless workload
- Can a known test workload start, respond, stop, and restart?

### Stateful workload
- Can synthetic data be written, read, and preserved according to the scenario's intended persistence model?

### Configuration truth
- Can a fresh/recovered component be reconstructed from repository-controlled configuration plus documented prerequisites?

## Mission 00 task
Create the exact commands/tests for your selected lab platform and save them here or as scripts under a later validation directory. Do not count a recovery as successful until the same pre-failure validation set passes again.

## Evidence
For every recovery trial record:
- failure start time;
- symptom;
- detected/recovered automatically or manually;
- service-restored time;
- full-validation-passed time;
- data loss, if any;
- remaining manual steps.
