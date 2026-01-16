# Release Notes — MathGov v5.0i rev14.29

**Release date:** 2026-01-16

This release publishes the synchronized rev14.29 specification set (Foundation + Appendices) and the canonical Sentience Gradient Protocol (SGP 4.1.1), along with the associated ProofPack zip used for Tier-4 pilot-executable audit workflows.

## What’s included

### Core documents
- MathGov_Foundation_5.0i_rev14.29_FINAL_SYNCED.docx
- MathGov_Appendices_5.0i_rev14.29_FINAL_SYNCED.docx
- SGP_4.1.1_PATCHED_READY_PUBLISH.docx

### Governance artifacts
- Alignment Constitution Public.pdf
- Alignment Test Case Library.pdf

### ProofPack
- MathGov_ProofPack_5.0i_rev14.29.zip

## Key rev14.29 sync guarantees

- Cross-document parameter consistency (rights floors, TRC defaults, HDW floors, kernel conventions).
- Appendix reference integrity (Foundation → Appendices match).
- Tier-4 pilot-executable constraints specified and aligned.

## SGP 4.1.1 canonicalization

- Human rights plateau is represented as **SG_norm(H) = 1.0** (normalized scalar).
- Stability gate uses **Stab(E)** (binary pass/fail) to avoid symbol collision.
- Adversarial robustness gate uses **D(E)** (with confidence-bound requirement).

## Publishing checklist (recommended)

- Add `SHA256SUMS.txt` at repo root or per release folder.
- Tag the GitHub release as `v5.0i-rev14.29`.
- Attach the ProofPack zip to the GitHub Release page.

