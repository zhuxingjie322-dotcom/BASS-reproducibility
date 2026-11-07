# BASS reproducibility archive

Version **1.0.0** accompanies *BASS: An Audit-Oriented Statistical Representation Framework for Distribution-Level Knowledge Auditing*.

## Download and verify

Download [BASS-reproducibility-v1.0.0.zip](https://github.com/zhuxingjie322-dotcom/BASS-reproducibility/raw/main/BASS-reproducibility-v1.0.0.zip), extract it, and run the following inside the extracted directory:

    python -m pip install -r requirements.txt
    python verify_release.py
    python verify_release.py --rerun-core --rerun-private --rerun-scale

The archive's SHA-256 digest is recorded in SHA256SUMS.txt. The internal manifest verifies the individual files.

## Included scope

- Both study-specific SimSUM-style and DDXPlus-style generation scripts.
- Corrected four-dataset primary experiment: ten stratified splits, 280 reference outcome rows and 40 implementation-check rows.
- Private-count experiment: 562 reference rows, including clean and diagnostic arms.
- Finite linear-query certificate and nine synthetic scale configurations.
- Saved train/test indices and fitted cutpoints, a 45-definition/450-row block manifest, one example artifact and code to regenerate all 40 artifacts.
- Pinned dependencies, numerical verification, plotting code and data provenance.

The three experiment groups use distinct protocols. Timing is hardware dependent. The public release does not claim complete refitting of historical main Tables 3–4 or all legacy supplemental learners, independent clinical deployment validation, or unrestricted deep-model knowledge recovery.

## Licenses

Author code/documentation: **MIT**, see LICENSE. The two bundled public UCI benchmarks retain **CC BY 4.0**, see DATA_LICENSE.md. Synthetic cohorts are local approximations, not the original published SimSUM/DDXPlus datasets. No protected clinical cohort or MIMIC records is included.

Citation metadata and more detailed instructions are inside the archive. No Zenodo DOI or GitHub release tag is claimed.
