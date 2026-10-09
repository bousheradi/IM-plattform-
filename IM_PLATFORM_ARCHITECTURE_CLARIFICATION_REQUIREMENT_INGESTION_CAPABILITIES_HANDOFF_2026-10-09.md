# IM Platform Architecture Clarification
## Requirement Ingestion, Source Adapters, Validation Capabilities and Cross-Customer Validation
**Date:** 2026-10-09  
**Status:** PROPOSED ARCHITECTURE CLARIFICATION / HANDOFF. No implementation authority by this document alone.  
**Frozen-authority impact:** NONE. Existing FINAL/FROZEN bytes/contracts remain immutable.

## Executive decision
The IM Platform does not need a fundamental rewrite. Customer differences belong primarily in governed Requirement Sets, Reference Sets, mappings, applicability and project context. New code is required only for genuinely new source adapters or technical validation capabilities.

## Target architecture
```text
Requirement sources: IDS | Excel | Manual UI | PDF/Word assisted extraction | API
        -> Requirement Ingestion Layer
        -> Canonical Requirement + Reference Authorities
        -> Applicability / Project Context
        -> Validation Orchestrator
        -> Capability Registry
             IFC_PROPERTY / REFERENCE / IDENTITY
             RVT_NATIVE / MEP_RELATIONSHIP / GEOMETRY_SPATIAL / PACKAGE / PROCESS_EVIDENCE
        -> Results / Evidence
        -> Review / Approval
        -> Information Product / Publish
        -> Workspace / Change Intelligence presentation
```

## Governance boundary
- Do not modify S19/Core, the completed Requirement Library, Reference Authority, CI-01, G-B1 or other frozen authorities.
- The Requirement Library remains reusable in its verified scope; ingestion must map into it rather than rebuild it.
- CI-01 remains unchanged and retains exactly: ADDED, REMOVED, UNCHANGED, PROPERTY_CHANGED, IDENTITY_UNCERTAIN.
- Missing/ambiguous capability = NOT_PROVEN/UNSUPPORTED, never PASS.
- Any contract extension requires an explicit successor.

## Requirement ingestion
All authoring/import paths converge on one canonical model:
1. Excel template import — highest priority for bulk no-code onboarding.
2. Manual UI — individual requirement/reference maintenance.
3. IDS — standard IFC requirement import; unsupported semantics fail closed.
4. PDF/Word AI extraction — DRAFT only, with provenance and human approval.
5. API/JSON — later machine integration.

## Capability families
- IFC_PROPERTY: entity/property/propertyset/datatype/value.
- REFERENCE: code lists, room names, BSAB, CoClass, etc.
- IDENTITY: GUID/FMGUID/uniqueness/protected identity.
- HISTORY/CHANGE: state comparison/context; keep CI semantics separate.
- RVT_NATIVE: views, sheets, phases, worksets, links, groups, shared parameters, audit/model health.
- MEP_RELATIONSHIP: system membership, relations, system/type/instance scope, units/flow.
- GEOMETRY_SPATIAL: spatial completeness, bounds, area/height/clearance geometry.
- PACKAGE: manifest versus actual files, required formats/versions.
- PROCESS_EVIDENCE: human/process obligations not reducible to deterministic validation.

## Source adapters
IFC is the current strongest direct model path. Planned additive adapters/capabilities include Revit native, DWG, PDF, Excel-as-source, GIS/point cloud/CDE. IDS is a requirement-ingestion adapter, not a source-model adapter.

## IDS relationship
IDS is a standardized requirement exchange for many IFC information rules. IM Platform adds requirement/reference governance, project/building/stage context, exact source identity, evidence, review/approval, publication gates, Change Intelligence and non-IFC/specialist capabilities.

## Cross-customer rule
Region Blekinge, Locum, Malmö and future customers use the same engine. Customer-specific content is configuration: Requirement Set, Reference Set, mapping/profile, applicability and context. Do not fork validators per customer.

## Roadmap effect
- R1 Product Workspace Slice 1: continue; no material delay.
- Add R1A design-only Requirement Ingestion / Capability contract: about 0.5–1 working day.
- R2 AIS / Verified Publish / Current: unchanged.
- R3 Baseline & Change Control: unchanged.
- R4 no-code onboarding: Excel, Manual UI, IDS, Reference import.
- R5 specialist/source capabilities: RVT Native, DWG, PDF, Package, MEP, Geometry/Spatial.

Rough planning ranges only: Excel/manual ~1–2 weeks; IDS ~3–7 working days after import contract; governed PDF-to-draft ~1–2 weeks; RVT Native ~2–4 weeks; Package ~1–2 weeks; MEP ~2–4 weeks; Geometry/Spatial ~3–6+ weeks for an initial robust scope.

## Developer sequence
1. Inspect exact frozen canonical contracts before coding; never invent field names.
2. Define Requirement Ingestion contract (identity, provenance, mapping, validation, preview, approval boundary, canonical binding).
3. Define Capability Registry contract (id, version, accepted input, result schema, proof/availability state, fail-closed semantics).
4. Implement Excel + reference-set DRAFT import first.
5. Add manual UI against the same draft representation.
6. Add IDS through the same ingestion path.
7. Keep PDF/Word extraction as human-approved DRAFT generation.
8. Add specialist capabilities as separate successors driven by proven gaps.
9. Show capability coverage explicitly in Workspace.
10. Preserve artifact hashes/evidence and acceptance/promotion/freeze transitions independently.

## Minimum acceptance conditions
- No parallel customer-specific requirement schema.
- Exact source provenance for every imported item.
- Unsupported semantics remain visible and fail closed.
- Reference sets are separately versioned/bound.
- Applicability is explicit and deterministic.
- Imports remain DRAFT until governed approval.
- No writes to frozen parent bytes.
- Validation binds exact requirement/reference/source/context identities.
- Missing capability cannot become PASS.
- Multiple customer packages coexist without customer-specific engine code for ordinary property/reference rules.

## Final position
Keep the existing platform foundations. Add Requirement Ingestion, Source Adapters, Capability Registry and Orchestration as additive layers. Excel + Manual + IDS should converge on the existing canonical Requirement/Reference model. New validation types are reusable product capabilities, not customer-specific code. Continue Workspace on the current critical path.
