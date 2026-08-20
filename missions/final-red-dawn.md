# Final Trial — Red Dawn

## Briefing
At 04:00 Lazarus suffers a compound incident. You are given only symptoms and your own runbooks.

## Challenge format
Have another person/tool secretly select 3–4 reversible failures across different domains: worker loss, controller outage, DNS/routing problem, config drift, missing state, monitoring outage, or a failed restore assumption.

## Rules
- Work from service impact and dependency maps.
- Restore highest-value dependencies in a reasoned order.
- Track time against your fictional RTO.
- Do not declare victory until the full validation checklist passes.

## Final evidence
- incident timeline
- dependency-based recovery order
- RTO/RPO results
- state/data-loss assessment
- corrected runbooks/automation
- postmortem identifying which recovery assumption failed

## Victory condition
Lazarus-Cluster is complete when recovery is a tested engineering capability rather than a hopeful document.
