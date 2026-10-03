# EBWA Artifact Manifest

Manuscript: *Closing the Attestation-to-Authorization Gap: Evidence-Bound Workload Authorization for Enterprise Multi-Cloud Platforms*

Author: Naresh Somara  
ORCID: 0009-0008-4997-3133  
Artifact version: EBWA v1.4.0

## Public repository contents

- `README.md` — research artifact overview
- `evidence/README.md` — evidence structure and final experiment inventory
- `evidence/final_results_summary.csv` — manuscript-level empirical results summary

## Raw artifacts to upload from the experiment workstation

The journal data link should not be finalized until these files are present:

1. Local 10k benchmark evidence archive containing:
   - raw_latency.csv
   - latency_summary.csv
   - drift_results.csv
   - recovered-v1.2-scale10k-final.json
   - final v1.2.1 large-working-set summary/output
2. `EBWA-kind-v1.3-evidence.zip`
3. `EBWA-AWS-v1.4-evidence.zip`
4. `EBWA_End_to_End_Prototype_v1.4.0.zip`

## Exclusions

Do not publish:
- generated private keys
- runtime secrets
- AWS credentials/tokens
- local SQLite databases
- temporary kubeconfig credentials
- cloud account identifiers beyond what is necessary for reproducibility

## Integrity

After raw archives are uploaded, add SHA-256 digests for each archive to this manifest and create an immutable tagged release.
