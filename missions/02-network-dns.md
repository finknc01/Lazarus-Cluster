# Trial 02 — The Network Goes Dark

## Briefing
All nodes are powered on, but the cluster behaves as if pieces vanished.

## Objective
Treat network/DNS as dependencies with their own recovery characteristics.

## Failure deck
In a disposable lab, choose two: break a route, isolate one subnet, stop lab DNS, point a resolver at the wrong server, or block one required control-plane port.

## Investigation
Use the packet-path discipline from Fabric-Faultline. Identify which services are healthy locally but unavailable across the cluster.

## Evidence
- dependency/path diagram
- first-good/first-bad evidence
- impact matrix
- recovery validation

## Victory condition
You can show that a healthy node is not the same thing as a healthy distributed system.
