# INFORMATION MANAGEMENT PLATFORM (IM Platform)
## Master Project Archive, Development History, Architecture, Current State & Handoff

**Archive date:** 2026-10-07  
**Owner / product lead:** Bousher Adi  
**Document role:** continuity archive, project history, architecture, technical/non-technical handoff and roadmap.

> **Authority warning:** This document is a synthesis of project conversations and available project artifacts. It is **not** a new technical authority, successor, promotion or freeze. The authoritative continuity baseline remains REV10 unless later exact primary evidence explicitly supersedes a scope. Exact bytes + SHA-256 + primary acceptance/freeze evidence always outrank this narrative.

## 0. Start here - what this package is for
This package exists so that Bousher, a developer, a BIM/Information Manager, ChatGPT or Claude can open the project later and understand: what problem the platform solves, why the architecture looks the way it does, what has actually been proven, what failed, what is frozen only for a scoped authority, what is still open, and what should happen next.

It is intentionally a **coherent synthesis, not a verbatim export of every chat line**. The project conversations are summarized chronologically and by decision. When a task touches a frozen or promoted scope, the exact primary artifact must still be consulted.

### Read order for a new session
1. `README_FIRST_IM_PLATFORM_ARCHIVE_HANDOFF_2026-10-07.txt`
2. `IM_PLATFORM_CURRENT_WORKING_STATE_2026-10-07.json`
3. This Master Project Dossier (`.docx`, `.pdf` or `.md`)
4. `IM_PLATFORM_CHATGPT_CLAUDE_CONTINUATION_PROMPTS_2026-10-07.txt`
5. Original REV10 Handoff Record / Continuity Archive when exact authority is needed
6. Latest task-specific primary evidence for the exact scope being changed or reviewed

## 1. Project in two minutes
IM Platform started as a practical BIM quality workflow to check whether Revit information really met owner requirements. It has evolved into an **owner-side Information Product Governance Platform**: a governed layer between requirements and source deliveries on one side, and databases/FM/AIM/GIS/CDE/APIs on the other.

The core product idea is simple: **do not let a visually plausible model, a newer filename, a browser preview, or an unverified client payload silently become organisational truth**. Instead the platform binds requirements, reference data, source identity, project context, validation, human review, approvals and evidence into a controlled publication chain.

The platform is not meant to replace Revit, Solibri, Navisworks, CDE or FM. It determines **which information can be trusted, why, by whom, against which requirements, for which project context, and with which evidence**.

## 2. Truth hierarchy and non-negotiable governance rules
1. Exact artifact bytes + SHA-256 + promotion/freeze/designation record outrank all summaries.
2. Frozen parents are immutable. Any change requires a new successor/candidate.
3. Source truth > preview.
4. Correction Approval != Delivery Approval != Organisation Acceptance != AIS != Verified Publish/Current.
5. Fresh source + revalidation are required before canonical/current publication.
6. Fail closed on stale, ambiguous, missing, inconsistent or unverifiable authority/evidence.
7. Never guess identity/version and never use a silent `latest` fallback.
8. Compare-Before-Write where source writeback exists.
9. Information Health / Model Health may inform, but may not override governance gates.
10. Failed attempts and NOT_PROVEN are evidence and must be preserved; never rerun/hot-patch to manufacture green.
11. One proven scope does not silently prove another.
12. Customer requirements belong in governed Requirement/Reference data, not customer-specific code forks.
13. Windows/PowerShell execution: one short, safe, logical block at a time; wait for observed output before the next dependent step.

## 3. Authoritative continuity baseline
REV10 remains the authoritative continuity/handoff baseline as of this archive.

| Record | SHA-256 | Role |
|---|---|---|
| REV10 Continuity Archive | `1D2B3C1D7E16FEF3597F2FE86AE1E9704DA9B23B1BAAAA8B1F56D65C4F3BAFC6` | Authoritative continuity baseline |
| REV10 Current State | `6651D314F1DB75C1502433D282B81E94AE5E4AD8CEFC50A7963F4650B7F7C7E2` | Current continuity state at REV10 |
| REV10 Handoff Record | `437A13BE4D4A865F910FD1CCEE593085BD002EC37D8AFDE37BD59770668F7252` | External authority pointer |

### Scoped current/frozen authorities
- **S19 VPC-01** - HISTORICAL FINAL FROZEN semantic Core; SHA/authority reference `3BEB862A7DCA6BCC18D18AFB7B8DD08D093EBA3F615D55A83EE39CE91EDA1A64`.
- **RLCB V2** - CURRENT / FINAL / FROZEN for binding scope 1-10; SHA/authority reference `EFF884F3A616D7D17CD9ADFF9A1B32A366F6D1E4A4C5D77A98BF1B7254863E39`.
- **F59 V4** - PROMOTED / CURRENT / FINAL / FROZEN for runtime-hardening scope; SHA/authority reference `81E5B4D2C085C5DE76CCB6E9C80DA893EF10F6A34D919421D8F0A2D5ADA223BD`.
- **m-66-1** - PROMOTED / CURRENT / FINAL / FROZEN for approval-to-review-session binding; SHA/authority reference `5E1938CBEC0EA891431404216C760CF24B02E3207CA3C52B1FBE0457BAF2B64D`.
- **G-B1** - PROMOTED / CURRENT / FINAL / FROZEN / CLOSED for exact reviewer identity scope; SHA/authority reference `32778DBFD69E9E5A27CCDF71CCCA016106CB6EE1987A1B64C1237D92206D2510`.

**Important:** multiple scoped authorities can all be current for different scopes. This does **not** mean the whole product is FINAL/FROZEN.

## 4. Development journey - idea to current state

| Period | Milestone | Why it mattered |
|---|---|---|
| Jun 2026 | First practical validation chain | Revit/Dynamo -> JSON -> requirements -> issues -> approval direction. Abboten 12-room proof established the first useful end-to-end concept. |
| Jun 2026 | Platform direction | The center of gravity moved from scripts to a platform: Dashboard/Approval, requirements, issues, 2D/3D, database, export and owner requirements. Revit became a source, not the workflow center. |
| Jun-Aug 2026 | Source breadth and scale | IFC/OpenBIM, geometry, 2D/3D review, multi-building, source parity and larger Region Blekinge models were added. |
| 14-23 Aug 2026 | Correction governance | Controlled corrections, Correction Approval, Translator, Compare-Before-Write and source-specific correction boundaries were established. |
| Late Aug 2026 | Identity/history/portability | Duplicate GUID protection, source precedence, Windows/Python portability, History & Analytics, IFC/Revit parity. |
| Early Sep 2026 | Governance hardening | NO_EFFECTIVE_RULES, fail-closed behavior, Requirement/Reference persistence and provenance. |
| 17-19 Sep 2026 | S11-S19 semantic successor chain | Reference -> Mapping -> Identity -> Context -> Binding -> Property Authority -> Baseline -> AIS -> Verified Publish / Current. |
| 19-21 Sep 2026 | Productization and Regression01 | SQLite/repository and Requirement/Reference administration. Regression Attempt21 stayed NOT_PROVEN rather than being forced green. |
| 21-24 Sep 2026 | Information Product / UI REV2 | Project Context, delivery cycles, Organisation Acceptance, AIS and Current were separated as explicit authorities. |
| Late Sep-2 Oct 2026 | Requirement governance | No-code/governed requirement lifecycle, controlled publication and semantic import hardening. |
| 2-4 Oct 2026 | RLCB V2 and Windows E2E | Exact Requirement/Reference content binding, real IFC, Approval Gate, DB persistence and immutable evidence discipline. |
| 5-6 Oct 2026 | F59 V4, m-66-1, G-B1, REV10 | Runtime hardening, approval-session binding and reviewer identity scopes closed/promoted/frozen. REV10 became authoritative continuity baseline. |
| 6-7 Oct 2026 | DP-01 deployment successor | Contracted deployment/productization work progressed through V2/V3 to V4. V3 NT-15 defect was preserved and corrected through a minimal V4 successor. |
| 7 Oct 2026 | DP-01 W4 representative flow | Real IFC -> review -> sealed bundle -> bound validation -> Delivery Approval -> Approval Gate -> persistence -> delivered session, with 210/210 product files unchanged and governed stop. |

## 5. Architecture - full platform in text, not an image

### Color/status legend
- **GREEN** = implemented / demonstrated / proven in defined scope
- **BLUE** = active next integration/productization work
- **YELLOW** = planned/partial/separate product track
- **RED** = open blocker/residual that must not be silently closed
- **PURPLE** = frozen/historical authority/evidence that must not be modified

### End-to-end owner flow
```text
SOURCE WORLD
  Revit / Dynamo / IFC / later DWG / PDF / Excel / GIS / Scan / CDE
        |
        v
SOURCE IDENTITY + NORMALIZATION
        |
        v
PROJECT / BUILDING / STAGE / DELIVERY CONTEXT
        |
        +------------------------------+
        |                              |
        v                              v
REQUIREMENT AUTHORITY           REFERENCE AUTHORITY
        |                              |
        +---------------+--------------+
                        v
                VALIDATION CONTEXT
                        |
                        v
                VALIDATION ENGINE
                        |
                        v
                OBJECT VALIDATION
                        |
                        v
                   REVIEW
                        |
                        v
               DELIVERY APPROVAL
                        |
                        v
                 APPROVAL GATE
                        |
                        v
          CANONICAL INFORMATION PRODUCT
                        |
                        v
         APPROVED INBOX / DATABASE / HISTORY
                        |
             +----------+----------+
             |          |          |
             v          v          v
           AIM/FM      GIS/CDE    Analytics/API
                        |
                        v
              VERIFIED PUBLISH / CURRENT
```

### Layer register
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

## 6. Semantic architecture and decision boundaries

### Requirement + Reference Authority
Requirement Library defines governed policy: requirement set/version, rule identity, severity, applicability and provenance. Reference Library defines controlled lists/classification/reference content. Their exact content identities are bound into Validation Context and downstream Approval Gate evidence.

### Validation Context
A Validation Context is the execution authority snapshot tying the exact Requirement Library + Reference Library + project/context selection to a cryptographic identity. No valid context => **BLOCKED**, and BLOCKED is never approvable.

### Validation Engine and Object Validator
Room/area/property/identity/classification validation is combined with object-level validation for walls/doors/windows/boundaries/links. Bound Object Validation produces `bound_result_sha256` plus review/source/delivery/building binding. Zero bound object rules do **not** mean "no findings"; the governed behavior is to preserve upstream object findings and mark their provenance.

### Correction vs Delivery vs Publication
Correction Approval only authorizes a correction/writeback action. It does not make preview data canonical. Revit corrections use Compare-Before-Write and then require a fresh export/revalidation. IFC is treated as read/normalize/validate; canonical correction happens in the source followed by a new IFC export, not by mutating IFC preview data in the platform.

Delivery Approval means the reviewed delivery may proceed to Approval Gate. Approval Gate then creates the canonical APPROVED artifact from **fresh source export** and verified bindings. Organisation Acceptance/AIS/Verified Publish/Current remain separate authorities.

## 7. Current architecture by capability

### GREEN - strong/proven mechanisms
- Revit/Dynamo source flow and controlled writeback mechanisms.
- IFC import, normalization, geometry/object extraction, review and validation.
- Requirement/Reference governance foundation and exact content binding.
- Source identity, context/binding, duplicate identity protection and fail-closed behavior.
- Review sessions, sealed review bundles, Delivery Approval and Approval Gate.
- Canonical Approved Inbox + SQLite/history persistence + object/geometry/report evidence.
- Immutable evidence discipline and successor/freeze governance for defined scopes.

### BLUE - active integration/productization
- DP-01 deployment packaging and final Windows evidence closure.
- Organisation/Project/Building/Stage/Cycle Product Workspace.
- Baseline binding and Change Intelligence V1.
- Product-level current-state navigation and self-service requirement onboarding.

### YELLOW - planned/separate tracks
- Reality Viewer product hardening and governed reality-vs-BIM integration.
- PDF/DWG/Excel/GIS/scan/CDE/FM connectors.
- Portfolio/organisation analytics, APIs and commercial onboarding.

### RED - must remain explicit
- DP-01 V4 is **NOT ACCEPTED / NOT PROMOTED / NOT FINAL-FROZEN**.
- W5 Final Integrity / Package Evidence is still outstanding.
- DP-01 manifest semantic inconsistency remains unresolved before any acceptance/freeze.
- Windows long-path residual remains open/out of scope for the current DP-01 claim.
- Whole-product FINAL/FROZEN/enterprise-ready claim is not authorized.

## 8. DP-01 deployment/productization - exact current state
DP-01 is the deployment/productization successor work that packages the governed platform without silently changing frozen semantic Core.

### Contract and lineage
- Approved DP-01 contract SHA-256: `F4F95A10D1A79365DD6F414C7668D0AB241C7587C738DE7D1B5162B124D46E0B`.
- V3 immutable predecessor ZIP SHA-256: `9EDE47CB85049386968ACBD19A23E46542AFA5317290E6FACA03BB72C2F7B445`.
- V3 product-tree identity: `E69E420B5FB4B4824BC021A7B96573B662706D187B2E39462B65BA33CC422D86`.
- V3 was **not accepted/promoted/frozen**. It exposed a real repeated-start lifecycle defect (NT-15) and the failed evidence was preserved.
- V4 is a minimal successor correcting exactly the intended lifecycle/server scope. Tested product tree: `1688AD93C13FE7B76C65ACD841C44EF93A4CEA08935CA55083178B0D7B100FDD`.
- V4 candidate ZIP: `6ACDACA2C141196758533B1095500CE9D9410594E6D7AFCCFA3326110D91DAC8`, 18,813,764 bytes.
- V4 server SHA-256: `4FD75FEEE05E5C762C9ED733EFDFC22DFA09B2350F3FEF0279FC2E6CDB11DB25`.
- V4 lifecycle SHA-256: `FEF84056D10733C40D842F156F9BAAC50E258FD2000EF5AF359AEE8C3EE72D4C`.
- Manifest SHA-256: `57ADD47690E6C4A17067B6A459474011640FE4CBFF327B38C8778FF63176A190`.
- SHA256SUMS SHA-256: `2F3E509C91B2A31A59D5E390DBDB0C4EAC99E6C04CBD73BD059408451F320A62`.
- AC28 post-package smoke Attempt02 PASS result SHA-256: `34BC4DBB18BD28CC49EEBFA6EBA54C3F6C4AAC203F299C05899DF4A03D842999`.

### W0-W4 Windows plan status
- W0 Identity/extract: completed.
- W1 Python/lifecycle/preflight: completed.
- W2 Negative/fail-closed evidence: completed.
- W3 Lifecycle/reset: completed.
- **W4 Representative real flow: completed at safe pause point on 7 Oct 2026.**
- **W5 Final Integrity / Package Evidence: next.**

### W4 representative flow - what was actually proven
Real IFC source: `M40_0254_00.ifc`, 21,616,570 bytes, SHA-256 `FA50122BC7618F18972F093D7BE512D2455F0E3DCA6BB1D174AE91C70CFC2061`.

1. Fresh runtime root was installed and server started from exact V4 fresh extraction.
2. Validation Context `f00568df945b6eb0945a500582fe4c532d7ff70af803f7110bb5f4f27728aa15` was registered from already verified historical authority content: Requirement SHA `0c872508756d6c662af781650be7f8725add64ba9402eb8b6e67fd3882f33dcb`, Reference SHA `eff6a681a09df2ce50826be7a60baceb75468f492f28c55d6f1f2e2c0d745dc7`, effective rules 28, object effective rules 0.
3. IFC import created run `RUN-IFC-20261007-133706` for Building 90254 with 24 rooms, 78 walls, 31 doors and 49 windows.
4. Review session `REV-20261007-133905-1ae069fe` was opened and review bundle sealed with SHA `3cd8c5b88fa1fa1d75ee4389edad95ad69baf73c92307cc845c0f7cea220a72a`.
5. Bound Object Validation preserved 163 upstream object issues under the zero-bound-rule behavior and returned bound result SHA `a08fa8d2fba7318338700b5c61c10553a8523134415a876bb06a7f33a488e8bc`.
6. Delivery Approval set the session to `approved_for_delivery` with reviewer **Bousher Adi**.
7. Approval Gate built a canonical artifact from fresh source. Technical decision = WARNING; human approval = `APPROVED_WITH_WARNINGS`; role = `BIM-samordnare`; canonical source authority = `fresh source export`.
8. Persistence succeeded with HTTP 200. Session became `delivered` with `ResultingRunId = RUN-IFC-20261007-133706`. DB import included 78 walls, 31 doors, 49 windows, 24 room boundaries, 158 room-object links and 163 object issues.
9. Product integrity after the full flow remained exact: 210 files before, 210 after, 0 changed, 0 removed, 0 added.
10. Governed stop returned exit code 0. Process died, server marker was removed, and `server.lock` remained only as the expected persistent lock file; the OS byte lock had been released.

### Important W4 negative learning - preserved, not hidden
A first persistence attempt returned HTTP 409 `OBJECT_VALIDATION_RESULT_UNVERIFIED:hash_mismatch`. This was traced to the **test harness**, not the V4 server: PowerShell `ConvertFrom-Json -> ConvertTo-Json` corrupted UTF-8 strings (`där -> dÃ¤r`, en dash -> mojibake) in 164 object-issue values, changing the canonical hash. Rebuilding the Approval Gate input directly from raw UTF-8 JSON preserved the bound result SHA exactly and persistence then passed. The failed 409 attempt remains evidence.

This is a valuable product lesson: cryptographic binding makes accidental encoding mutation visible instead of silently accepting it.

## 9. DP-01 unresolved manifest semantic risk
The current V4 manifest top-level `scope_matrix_path` points to the V3->V4 two-file correction matrix, while the historical top-level manifest schema used a full parent-to-current candidate scope matrix. Materialization authorization did not allow silently adding another full matrix. Therefore the current V4 manifest/package metadata must **not** be called canonical/final until this semantic question is explicitly resolved. Do not overwrite or rebuild the existing candidate/ZIP merely to make this disappear.

## 10. Review / approval state model
```text
OPEN REVIEW
   |
   v
SEALED REVIEW BUNDLE
   |
   v
BOUND VALIDATION
   |
   v
CORRECTION REVIEW (if needed)
   |
   v
DELIVERY APPROVAL
   |   creates_canonical = false
   v
APPROVED_FOR_DELIVERY
   |
   v
APPROVAL GATE
   |   fresh source + verified context + bound result + reviewer/role
   v
CANONICAL APPROVED ARTIFACT
   |
   v
PERSISTENCE / APPROVED INBOX / HISTORY DB
   |
   v
DELIVERED
```

## 11. Information Product / UI REV2 decisions that must be preserved
- Delivery-cycle types are configured per project type and do not replace governed `stage_id`.
- Pilot scope is single-context; no baseline from another context is authority.
- Pilot P1 cycle is `PILOT-FINAL-DELIVERY`, label "Slutleverans", declared final.
- AIS seals only after verified Organisation Acceptance and binds to exact cycle, Delivery Approval, snapshot set and canonical payload.
- Current authority is scoped to exact Project Context. Organisation-level derived views are read-only unless a later successor explicitly creates authority.
- Stage identity must not be fabricated from labels/status. G04 remains authority-extracted/context-binding-unresolved where that evidence is unresolved.

## 12. Change Intelligence V1 - planned next capability
Change Intelligence must compare a new governed delivery against an explicitly declared approved/current baseline or exact snapshot - not automatically "previous run". Planned classes include ADDED, REMOVED, CHANGED_PROPERTY, MOVED, RESIZED, UNCHANGED and IDENTITY_UNCERTAIN. Identity uncertainty must fail/review rather than guess.

The practical owner problem it should solve includes stale-content cases where a consultant uploads a new CDE version number but the content actually derives from an older internal revision. The system must compare source/content identity and governed deltas, not trust the version label alone.

## 13. Reality / Point Cloud track
Reality Viewer is strategically important for existing buildings and scanning, but remains a separate track from Core authority. Demonstrated direction includes E57/point-cloud viewing, clipping, LOD and measurement. A Region Blekinge E57 candidate has been used at about 9 GB scale. Future integration includes point picking, level/coordinate association, reality-vs-BIM comparison and governed deviations. Automatic Scan-to-BIM is not a proven claim.

## 14. Legacy / no-BIM / MENA strategy
IM Platform must not require a BIM-ready building. The intended progression is **Registry -> Documents -> Structured Data -> 2D -> IFC -> Digital Twin when justified**. Planned source adapters therefore include PDF, DWG, Excel/CSV, GIS, survey/scan and CDE/FM APIs. Governance, provenance, condition/intervention data, asset registration and approvals can create value before advanced BIM exists.

## 15. Region Blekinge proof basis
The project has been developed against real owner-side use cases, including Abboten early room validation, Akuten / Building 90254 repeated IFC/E2E evidence, multi-building flows (including 90254, 92505, 90246, 97701), larger models with hundreds of rooms and thousands of objects/issues, duplicate identity protection and governed Revit/Dynamo corrections.

## 16. Code vs non-code work
### Non-code / information governance
- Curate Requirement/Reference Libraries with owners, lifecycle, version and content hashes.
- Define Project Package: project type, stage, delivery cycles, final cycle, acceptance obligations and vocabulary.
- Map PTS/IDS/Trafikverket/customer requirements into automatic/manual/document/process evidence.
- Define Information Product Contracts, correction/approval procedures and handover obligations.
- Prepare onboarding/training/support/release notes and legacy source inventories.

### Code / product engineering
- Finish DP-01 W5 and manifest semantic closure.
- Change Intelligence V1.
- Product Workspace walking skeleton.
- Stronger API/data contracts and multi-user operations.
- Extended source connectors.
- Later RBAC/SSO, tenancy, observability, backup and SLA operations.

## 17. Product maturity now
| Area | Current maturity | What remains |
|---|---|---|
| Governance Core | Strong / scoped authorities proven | Preserve immutable; use successors for new semantics |
| Requirement/Reference | Strong foundation | Product self-service UI + enterprise roles |
| Object validation | Proven for defined scopes | Broader profiles/onboarding |
| Revit/Dynamo | Mechanism proof | Broaden scenarios and packaging |
| IFC | Real read/normalize/validate/review evidence | Repeatable external onboarding |
| Review/Approval | Strong mechanism | Product UX and organisation flow |
| Persistence/history | Working | Stronger API/operations |
| Deployment | Late proof stage | W5 + manifest closure + formal decision |
| Change Intelligence | Architecture/design direction | Implementation + runtime evidence |
| Product Workspace | Planned/active next | Walking skeleton |
| Reality Viewer | Separate demonstrated track | Product hardening + integration contract |
| Legacy/connectors | Strategy/planned | Implementation |
| Enterprise | Future | RBAC/SSO/tenancy/observability/support |

## 18. Roadmap
| Phase | Time | Status | Scope |
|---|---|---|---|
| Phase 0 - Proven concept | Jun-Aug 2026 | DONE | Revit/Dynamo/JSON validation, IFC, DB/history, review, writeback, correction governance, source parity. |
| Phase 1 - Governance foundation | Aug-Sep 2026 | DONE | Semantic successor chain, identity/context/binding/property/baseline/AIS/Current semantics. |
| Phase 2 - Binding & runtime hardening | Late Sep-6 Oct 2026 | DONE for defined scopes | RLCB V2, F59 V4, m-66-1, G-B1. |
| Phase 3 - Integrated Alpha | Oct 2026 | IN PROGRESS | DP-01 packaging/Windows proof, Change Intelligence V1, Product Workspace walking skeleton. |
| Phase 4 - Product V1 | Nov 2026 target | PLANNED | Organisation -> Project -> Building -> Information Product, baseline/delta, governed review/publish, APIs. |
| Phase 5 - Pilot Ready | Dec 2026-Jan 2027 | PLANNED | Repeatable Region Blekinge pilot, installation/support, Current dashboard, FM/AIM/GIS handover. |
| Phase 6 - Legacy/connectors | Q1-Q2 2027 | PLANNED | PDF/DWG/Excel/GIS/scan/CDE/FM adapters and no-BIM workflows. |
| Phase 7 - Enterprise scale | 2027-2028 | FUTURE | RBAC/SSO, tenant isolation, observability, backup, multi-org, SLA/support, portfolio analytics. |

### Immediate next order - do not reorder casually
1. **W5 Final Integrity / Package Evidence.**
2. **Resolve DP-01 manifest semantic issue without silently modifying frozen/candidate evidence.**
3. **Formal DP-01 closure / acceptance decision for the exact scope only.**
4. **Update continuity state after the exact governance decision.**
5. Continue Phase 3 with **Change Intelligence V1** and **UI/Product Workspace walking skeleton**.

## 19. Product V1 target
The Product V1 goal is not a huge feature count. It is that an Information Manager can navigate the owner flow without working directly in Python/JSON/DB:

Organisation -> Project -> Building -> Requirements -> Delivery -> Validation -> Changes -> Review -> Approval -> Current -> FM/AIM/GIS/API.

The UI must display the authority/binding state, not hide it. A clean-looking UI must never turn uncertain authority into a green state.

## 20. What can safely be claimed externally
| Topic | Safe wording | Not yet safe |
|---|---|---|
| Core governance | Evidence-driven owner-side information governance with immutable successor/evidence discipline | Whole product is enterprise-ready/final |
| Revit/Dynamo | Controlled validation/correction/writeback mechanisms demonstrated | Universal auto-correction across all disciplines |
| IFC | Real-model read/normalize/validate/review and canonical approval flow demonstrated | Direct canonical IFC writeback |
| Requirement governance | Governed lifecycle and exact content binding substantially demonstrated | Full authenticated enterprise self-service |
| Deployment | V4 Windows representative flow through persistence demonstrated; final package closure still pending | DP-01 accepted/promoted/frozen |
| Reality | Separate point-cloud/viewer capability demonstrated | Automatic Scan-to-BIM/digital-twin generation |
| Legacy | Roadmap supports PDF/DWG/GIS/scan without BIM prerequisite | All connectors production-ready |
| Commercial | Strong pilot/service-led proposition | Mature multi-tenant SaaS with SLA/SSO |

## 21. Working method for every future change
1. Identify exact parent authority and hashes.
2. Create fresh successor/staging; never modify frozen parent.
3. Define scope, claims and acceptance criteria before coding.
4. Implement the smallest coherent delta.
5. Run static/syntax/unit and targeted negative tests.
6. Run controlled runtime/server/browser acceptance where the claim depends on runtime.
7. Capture exact logs, hashes, manifests and write-scope diffs.
8. Preserve failures/operator mistakes; use a new attempt instead of overwrite.
9. Independent/read-only evidence review.
10. Promotion/freeze only for exact proven scope.
11. Update Current State/Master Context/continuity append-only.

## 22. Handoff for a technical developer
- Do not begin with refactoring. First understand authority/state/evidence.
- Verify REV10 identities and exact parent for the task.
- Requirement/Reference Libraries are policy authority; validators/profile engines are execution capability.
- Client/UI payload must never be the sole authority for canonical persistence.
- Bind exact context/hash and reject stale/tampered/mismatched payloads.
- Preserve Revit vs IFC correction boundaries.
- Keep Reality Viewer/connectors separate until an explicit integration contract exists.
- Classify every task: Core successor / UI-Product Workspace / Reality Viewer / productization-deployment / connector / non-code governance.
- For DP-01, continue from **W5**, not by rerunning W4. Preserve all W4 failed harness attempts and the successful raw-UTF8 path.

## 23. Handoff for BIM / Information Manager / non-technical reader
IM Platform is a controlled owner-side gate that converts delivered information into trusted information. It starts with owner requirements and reference data, checks the exact incoming source for the exact project context, records issues, separates blockers/warnings/manual checks, controls corrections and approvals, requires a fresh source after correction, preserves evidence/history, and publishes an explicit Current state instead of assuming newest file = truth.

## 24. Conversation/history index - what the project chats covered
This dossier synthesizes the project's conversation history rather than copying every message. Major chat streams include:
- Platform-centered workflow and early v41-v43 continuity.
- Revit/Dynamo validation, Approval Gate, rules/issues, database/Power BI and object validation.
- 2D/3D review, geometry, multi-level behavior and Review 3D read-only boundary.
- Controlled correction approval, writeback and Compare-Before-Write.
- IFC source precedence, canonical source authority and duplicate identity protection.
- Requirement/Reference libraries, no-effective-rules, semantic import hardening and no-code governance.
- S11-S19 semantic successor chain and Regression01 NOT_PROVEN learning.
- UI REV2 / Information Product governance, Project Context, delivery cycle, AIS and Current decisions.
- RLCB V2, F59 V4, m-66-1 and G-B1 scoped authority closure.
- DP-01 contract, V2/V3/V4 deployment candidates, Windows evidence, NT-15 lifecycle correction and W4 representative flow.
- Reality Viewer / point cloud.
- Legacy/no-BIM and MENA commercialization strategy.

For exact old implementation details, use the original project chats and primary archives. This document is the stable orientation layer.

## 25. New ChatGPT / Claude continuation rule
A new AI session must **continue**, not redesign from memory. It must read the archive package first, recognize REV10 as the authority baseline, then apply later exact task-specific evidence. Latest working status from this package: **DP-01 V4 W4 is complete at a safe pause; W5 is next; manifest semantic issue remains; no DP-01 acceptance/promotion/freeze has occurred.**

## 26. Exact current DP-01 checkpoint
- V4 product tree: `{dp01['v4_tree']}`
- V4 ZIP: `{dp01['v4_zip_sha256']}`
- W4 run: `{dp01['w4_run_id']}`
- W4 review session: `{dp01['w4_review_session']}`
- W4 bundle SHA: `{dp01['w4_bundle_sha']}`
- W4 bound result SHA: `{dp01['w4_bound_sha']}`
- W4 decision: technical `WARNING`; human `APPROVED_WITH_WARNINGS`.
- W4 persistence: HTTP 200 / `ok=true`; session `delivered`.
- Product integrity after W4: 210 -> 210 files; 0 changed / 0 removed / 0 added.
- Governed stop: exit code 0; process stopped; marker removed; persistent `server.lock` file is expected because the OS lock is released without deleting the file.
- **Next:** W5 Final Integrity / Package Evidence.

## Appendix A - ChatGPT continuation prompt
See `IM_PLATFORM_CHATGPT_CLAUDE_CONTINUATION_PROMPTS_2026-10-07.txt` for the ready-to-paste prompt.

## Appendix B - Claude continuation prompt
Use the section named **CLAUDE / project “IM PLATTFORM”** in the prompt file.

## Appendix C - Source basis and limitation
This dossier is based on the project conversation history available in the IM Platform project, the REV10 Master Project Dossier/Handoff material, project evidence/status files, DP-01 pre-Windows review/evidence material and the 7 October W4 Windows run captured in the current conversation. It is deliberately a coherent synthesis rather than a verbatim transcript archive. When narrative conflicts with later exact primary evidence, the later primary evidence wins.
