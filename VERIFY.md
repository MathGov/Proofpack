# VERIFY — Integrity Verification (MathGov v5.0i rev14.29)

This repository includes a SHA-256 hash list so you can verify that downloaded files have not been altered.

## What you need

- A local copy of the files you want to verify
- The repository hash list:
  - `SHA256SUMS_rev14.29.txt`

## Recommended verification targets (rev14.29)

Canon:
- `canon/rev14.29/MathGov_Foundation_5.0i_rev14.29_FINAL_SYNCED.docx`
- `canon/rev14.29/MathGov_Appendices_5.0i_rev14.29_FINAL_SYNCED.docx`
- `canon/rev14.29/SGP_4.1.1_PATCHED_READY_PUBLISH.docx`

ProofPack:
- `proofpack/rev14.29/MathGov_ProofPack_5.0i_rev14.29.zip`

Support:
- `support/Alignment_Constitution_Public.pdf`
- `support/Alignment_Test_Case_Library.pdf`

## Windows (PowerShell)

1) Download the file(s) you want to verify and the hash list `SHA256SUMS_rev14.29.txt`.

2) Compute a SHA-256 hash:

```powershell
Get-FileHash .\MathGov_ProofPack_5.0i_rev14.29.zip -Algorithm SHA256
```

3) Compare the output hash to the matching line inside:

`SHA256SUMS_rev14.29.txt`

If the hash matches exactly, the file is verified.

## macOS / Linux (Terminal)

1) Compute a SHA-256 hash:

```bash
shasum -a 256 MathGov_ProofPack_5.0i_rev14.29.zip
```

2) Compare the output hash to the matching line inside:

`SHA256SUMS_rev14.29.txt`

If the hash matches exactly, the file is verified.

## Batch verify a folder (macOS/Linux)

If `SHA256SUMS_rev14.29.txt` is in the same folder as the files:

```bash
shasum -a 256 -c SHA256SUMS_rev14.29.txt
```

Note: This works when filenames and paths match. If you moved files into different folders, verify one-by-one.

## What a mismatch means

If the hash does not match:

- the file may be corrupted during download, or
- the file may have been modified, or
- you may be hashing a different filename/version than the one listed.

The correct action is to re-download the file from the canonical repo path and verify again.

## Trust boundary

A verified hash confirms the file matches the published release artifact byte-for-byte.
It does **not** validate the correctness of the model or the ethics—only the integrity of the artifact.
