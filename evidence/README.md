# EBWA Research Evidence

This directory is the public research-data location for the EBWA manuscript.

## Final empirical evidence set

### Local 10k benchmark
- 10,000 logical workload identities and posture objects
- 256 artifact/provenance objects
- 128 policy objects
- 16 trust domains
- 10 independent trials × 5,000 matched rounds for headline profiles
- Full EBWA (D) EBAR = 1.0

Headline results:
- Fresh: A p95 1.947 ms; D p95 3.224 ms; D-A p95 +1.276 ms; paired SDO95 2.172 ms; D serial rate 257.9/s
- Cached high reuse: A p95 2.212 ms; D p95 2.444 ms; D-A p95 +0.232 ms; paired SDO95 1.255 ms; D cache hit 95.4%; D serial rate 343.4/s
- Cached large working set: A p95 3.925 ms; D p95 5.466 ms; D-A p95 +1.542 ms; paired SDO95 2.934 ms; D cache hit 2.96%; D serial rate 141.3/s

### Drift / revocation
- 200 explicit posture-drift events
- mean revocation delay 4.344 ms
- p50 4.040 ms
- p95 6.316 ms
- p99 8.486 ms
- NDE 0.00434 with a 1.0 s normalization window per event

### Two-cluster kind validation
- Two independent Kubernetes clusters / trust domains
- 11/11 expected security assertions passed
- Legitimate access allowed
- Cross-cluster credential replay denied
- Trust-domain mismatch denied
- Artifact substitution denied
- Insufficient scope denied
- Provenance-plane outage failed closed
- Posture drift invalidated cached ALLOW
- Isolation degradation allowed under D and denied under E
- Protected-resource tampering denied with HTTP 403

### Amazon EKS external validation
- One short-lived managed EKS cluster in us-east-2
- Two independently seeded authorization roots: ebwa-east and ebwa-west
- 11/11 expected security assertions passed
- 500 authorization timing requests per namespace
- ebwa-east server latency: p50 0.908 ms; p95 1.317 ms; p99 2.705 ms
- ebwa-west server latency: p50 0.909 ms; p95 1.234 ms; p99 2.237 ms
- Client kubectl port-forward RTT is excluded from the authorization-latency claim

## Raw evidence archives

The following raw archives should be uploaded from the experiment workstation before using this repository URL as the journal's final research-data link:

- `local-10k-final/` or a ZIP containing raw_latency.csv, latency_summary.csv, drift_results.csv, and the recovered benchmark JSON
- `EBWA-kind-v1.3-evidence.zip`
- `EBWA-AWS-v1.4-evidence.zip`
- EBWA v1.4.0 source/prototype archive

Generated private keys, runtime secrets, local databases, and cloud credentials must not be uploaded.
