# DP-01 V5 Closure Review 85 Supplement

Date: 2026-10-08
Role: append-only continuity clarification after independent Review 85
Review 85 SHA-256: `5D80718B04B568357C2B9D052DED1053256CE6CF85B795A718EF4C28FADCF4D1`

## Status impact
Review 85 does **not** change the formal DP-01 disposition. DP-01 remains:

`NOT ACCEPTED / NOT PROMOTED / NOT FINAL / NOT FROZEN`

AC-02 and AC-17 remain `NOT_PROVEN`. Windows long-path remains `OPEN / OUT OF SCOPE`. No residual is closed. REV10 remains unchanged.

## Review 85 findings carried forward

### M-85-1 - review chain
V3, V4, V5 and the Windows evidence rounds were builder-tested but were not independently reviewed before closure. Review 85 is the first independent read of the V4/V5 product logic after the fact.

**Disposition:** future handoff text must not describe V3/V4/V5 Windows proof as independently reviewed. If DP-01 acceptance is ever reopened, the original Windows evidence must be packaged and independently reviewed before any Windows AC is counted as independently PASS.

### M-85-2 - 28/30 accounting
The bound closure record states `28/30 PASS`, but Review 85 could not independently verify that complete count because the cited Windows evidence artefacts were not supplied in the review package.

**Disposition:** preserve `28/30 PASS` only as the **builder-assessed closure accounting bound by the closure record**. Do not label it independently verified. Review 85 independently reverified candidate integrity, lineage and a subset of behavior, but not all 28 PASS criteria.

### M-85-3 - handoff fitness
The prior post-closure handoff bundle contained stale V4/W5 narrative, an unresolved-manifest statement, unfilled placeholders in the Markdown dossier, non-equivalent MD/DOCX/PDF content and a stale prompt filename reference.

**Disposition:** this successor handoff is regenerated from one current source. The prior handoff ZIP `86E76247477396DAAE1FB271D7B71B011ECB72CDF5D55662276798571EAAD5C6` is preserved as historical and must not be used as the primary continuity entry point.

### m-85-1 - V5 manifest stale identity metadata
The V5 candidate `MANIFEST.json` still declares a V4 schema/governance-state label even though the candidate name and product root identify V5.

**Disposition:** known metadata residual. Do not repack or edit V5. Fix only through a future separately governed successor if needed.

### m-85-2 - independent review records
The V5 candidate contains a Review 83 chat capture rather than the delivered Review 83 record, and Review 84 is absent.

**Disposition:** future evidence packages should carry delivered Reviews 83 and 84 by exact hash. This handoff carries Review 85 exactly; Reviews 83/84 remain external primary records unless their exact bytes are supplied.

### m-85-3 - AC-02 checkpoints
Reviewer-independent parent checks exist at other historical points, but they are not the contract's four required AC-02 phases.

**Disposition:** no retroactive mapping. AC-02 remains `NOT_PROVEN`.

### m-85-4 - staging pycache
The mutable staging contamination was harness fragility, not final V5 contamination.

**Disposition:** preserve as known harness issue; fix only in a future successor.

## Scope-classification clarification
The full parent-to-V5 scope matrix marks `dp01_lifecycle_v1.py` and `start_platform_server_v53.py` with `core_semantic_change=YES`, while the approved contract states `No Core semantics change`. Review 85 itself also states the frozen Core authorities were untouched and no Core file changed after V2.

This is therefore recorded as an **OPEN CLASSIFICATION INTERPRETATION**, not as a newly proven contract breach:

- the `YES` labels are real and must not be hidden;
- the existing evidence does not establish whether that column means frozen-Core semantic authority or DP-01 runtime/lifecycle behavioral semantics;
- no V5 byte is changed;
- no acceptance state changes;
- if DP-01 is ever reopened, the matrix column definition and contract boundary must be explicitly dispositioned before any new acceptance claim.

## Evidence portability limitation
The exact closure assessment and binding are known by SHA-256:

- assessment: `7C14CBD22D2B06CBDBAB8A8BBEF1D9BAB3A8F40C09BC31A9C93B6831126CCE45`
- binding: `936E16B8AA5D59E7215B526BC7030A4C6600C7EB8B4FA96FD1DF59281EAD1E2D`

This generated handoff must not reconstruct those primary records from chat/log text. If the exact raw bytes are not physically present in the bundle, they remain required external primary evidence.
