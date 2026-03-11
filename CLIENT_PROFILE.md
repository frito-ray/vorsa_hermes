# Client Profile — Rabkin Diagnostics

## Organization
- Name: Rabkin Diagnostics
- Location: Pittsburgh, PA
- Domain: Dermatopathology lab operations
- Delivery partner: VorsaTech, LLC (Vorsa)

## Primary User
- Dr. John Cangelosi (Physician / Pathologist)
- Remote location noted in SRD: Houston, TX

## Existing Systems
- LIS: VitalAxis (Vital Access)
- Scanner: Motic FlexScan 60 (QPTIFF)

## Product Objective
Build a custom clinical workflow application that integrates case queue, full-screen slide viewer, and intelligent rule-driven data entry to reduce physician per-case review time.

## Target Outcomes (SRD v1)
- Reduce per-case review time from ~60s to ~20s
- Automate repetitive diagnosis-linked data entry (ICD, orders, templates)
- Unify VitalAxis queue + slide review in a single UI
- Create reusable framework for future acquisitions

## Scope Summary
### In Scope — Phase 1
- VitalAxis queue integration
- Full-screen viewer with OpenSeadragon (Motic iframe fallback)
- Slide pre-loading keyed by case number
- Diagnosis/data entry panel and VitalAxis sign-out flow
- Auth + RBAC
- Audit logs and preferences in Postgres (no PHI storage)

### In Scope — Phase 2
- Rule engine + admin UI
- Auto-suggestions for ICD/orders/templates
- Historical bootstrap of initial rules

### Aspirational
- Phase 3: Staff read-only UI + OCR enhancement
- Phase 4: AI pre-diagnosis (Phikon-v2 + CLAM)

## Key Constraints
- No PHI persisted outside VitalAxis
- HIPAA compliance review required pre-launch
- Vercel Enterprise BAA required before go-live
- OpenSeadragon dependency on Motic tile API; iframe fallback required

## Open P1 Blockers
- Confirm VitalAxis API credentials/permissions
- Confirm Motic server accessibility from Vercel backend
- Confirm Motic tile API compatibility for OpenSeadragon
