# EBWA Artifact Manifest

Manuscript: *Closing the Attestation-to-Authorization Gap: Evidence-Bound Workload Authorization for Enterprise Multi-Cloud Platforms*

Author: Naresh Somara  
ORCID: 0009-0008-4997-3133  
Artifact version: EBWA v1.4.0

## Public repository contents

- `README.md` — research artifact overview
- `CITATION.cff` — citation metadata
- `prototype/EBWA_v1.4.0_public_artifact.zip` — sanitized v1.4.0 reference implementation
- `evidence/final_results_summary.csv` — manuscript-level empirical results summary
- `evidence/local/EBWA-local-10k-final-evidence.zip` — final local 10k benchmark and drift evidence
- `evidence/kind/EBWA-kind-v1.3-evidence.zip` — two-cluster Kubernetes validation evidence
- `evidence/aws/EBWA-AWS-v1.4-evidence.zip` — Amazon EKS external-validation evidence
- `SHA256SUMS.txt` — SHA-256 integrity hashes for the public artifacts

## Reproducibility coverage

The public package supports the manuscript's principal empirical claims:
- local fresh, high-reuse-cache, and large-working-set 10k profiles;
- drift/revocation measurements;
- two-cluster kind security validation;
- short-lived Amazon EKS external validation;
- reference implementation and validation scripts.

## Exclusions

The distributable artifact intentionally excludes:
- generated private keys;
- runtime secrets;
- AWS credentials or temporary tokens;
- local SQLite databases;
- temporary kubeconfig credentials;
- transient cloud account/session material not required for reproduction.

## Integrity

SHA-256 digests are recorded in `SHA256SUMS.txt`. Reviewers should verify downloaded archives against those values before analysis or reproduction.

## Archival recommendation

The GitHub repository is suitable as the journal research-data link. For long-term preservation and DOI citation, create an immutable release and archive that release in a DOI-issuing repository such as Zenodo after the submission package is frozen.
