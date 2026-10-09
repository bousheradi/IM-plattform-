# IM Platform - Text Architecture & Roadmap (2026-10-07)

This is a text-only architecture map. No image.

## Legend
GREEN = proven/implemented in defined scope; BLUE = active next work; YELLOW = planned/separate; RED = open; PURPLE = frozen/historical.

## Master flow
```text
Source World -> Source Identity/Normalization -> Project Context -> Requirement/Reference Authority -> Validation Context -> Validation Engine -> Object Validation -> Review -> Delivery Approval -> Approval Gate -> Canonical Information Product -> Persistence -> AIS/Verified Publish/Current -> FM/AIM/GIS/CDE/API
```

## Layer register

| # | Layer | Responsibility | Status |
|---|---|---|---|
| 01 | Source / Authoring | Revit, Dynamo/Python, IFC; planned DWG/PDF/Excel/GIS/scan/CDE/FM sources | GREEN |
| 02 | Acquisition / Adapters | Source-specific import/export, raw file hashing, normalization, project/property/building extraction | GREEN |
| 03 | Source Identity & Integrity | SHA-256, run/building/project identity, source precedence, fresh-source rule, fail-closed | GREEN |
| 04 | Governed Project Context | Organisation -> Project -> Property -> Building -> Stage -> Delivery Cycle | BLUE |
| 05 | Requirement Authority | Requirement Set/Version, rules, severity, applicability, provenance and exact library identity | GREEN |
| 06 | Reference Authority | Allowed values, code lists, classification and exact reference content identity | GREEN |
| 07 | Validation Context | Immutable binding of requirement + reference + project context; context SHA and effective rules | GREEN |
| 08 | Validation Engine | Room/area/identity/property/classification validation; STOP/WARNING/INFO/PASS/BLOCKED | GREEN |
| 09 | Object Validator | Walls/doors/windows/boundaries/links/object issues; bound result SHA and authority binding | GREEN |
| 10 | Correction / AutoFix | Proposals, preview, human Correction Approval, compare-before-write; fresh source required | GREEN |
| 11 | Review Lifecycle | Review session, sealed bundle, audit, validation, corrections, Delivery Approval | GREEN |
| 12 | Approval Gate | Human decision bound to fresh source + validation authority + review session; BLOCKED never approvable | GREEN |
| 13 | Canonical Information Product | Approved artifact with identity, validation, approval, provenance and canonical source authority | GREEN |
| 14 | Persistence | Approved Inbox, SQLite history DB, geometry/object evidence, reporting | GREEN |
| 15 | AIS / Verified Publish / Current | Separate Organisation Acceptance/AIS/Current semantics; exact publication authority | BLUE |
| 16 | Baseline & Change Control | Declared baseline, comparison target, governed delta and impact analysis | BLUE |
| 17 | Change Intelligence V1 | Added/removed/property/geometric deltas, identity uncertainty, stale/revision detection | YELLOW |
| 18 | Reality Viewer | E57/point cloud/360 context and measurement; separate track from Core authority | YELLOW |
| 19 | Analytics / Reporting | Validation reports, Power BI, geometry/ROI summaries, future portfolio analytics | GREEN |
| 20 | Product Workspace / UI | Organisation/Project/Building/Information Product workspace, requirements, review, publish, admin | BLUE |
| 21 | Downstream Consumers | FM/AIM/GIS/CDE/API/Digital Twin/operations | YELLOW |

## Current focus
- BLUE: DP-01 W5 and manifest semantic closure.
- BLUE: Change Intelligence V1.
- BLUE: Product Workspace walking skeleton.
- RED: no DP-01 acceptance/freeze yet.
- PURPLE: REV10 and scoped frozen authorities remain immutable.
