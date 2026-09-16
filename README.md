# PARCH Formal Analysis

This repository contains the Verifpal models and verification results used for the formal analysis of the PARCH authentication and handover protocols.

## Contents

| File | Description |
|---|---|
| `authentication.vp` | Verifpal model of the PARCH GCS–CH authentication protocol |
| `handover.vp` | Verifpal model of the PARCH failure-resilient ACC handover protocol |
| `authentication-1.png` | Authentication model and verification output |
| `authentication-2.png` | Authentication verification results |
| `handover-1.png` | Handover model and verification output |
| `handover-2.png` | Handover verification results |

## Verification Setup

The protocols were analyzed in Verifpal using:

- Active Dolev–Yao adversary
- Two concurrent sessions per principal
- Independent verification of the authentication and handover protocols

## GCS–CH Authentication

The authentication model evaluates nine security queries covering:

- Confidentiality
- Session-key freshness
- Session-key agreement
- Pseudonym agreement
- GCS-to-CH authentication
- CH-to-GCS authentication

All nine queries pass.

## Failure-Resilient ACC Handover

The handover model evaluates ten security queries covering:

- Confidentiality
- Session-key freshness
- Session-key agreement
- ACC-to-CH authentication
- CH-to-ACC authentication
- Explicit key confirmation

All ten queries pass.

## Reproducing the Analysis

1. Open the Verifpal Workbench:
   `https://verifpal.com/workbench/`

2. Copy the contents of `authentication.vp` or `handover.vp` into the Workbench.

3. Click **Verify**.

4. Compare the output with the corresponding verification screenshots included in this repository.

## Related Repository

The computational benchmarking scripts used in the PARCH performance evaluation are available separately in the `PARCH-Benchmarks` repository.
