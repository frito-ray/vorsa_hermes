# Rabkin Diagnostics SRD v1 — Structured Extract

## Source
- File: `Rabkin_Diagnostics_-_Clinical_Workflow_SRD_v1.docx`
- Download path (agent-created): `/home/cray/_task_inputs/Rabkin_Diagnostics_Clinical_Workflow_SRD_v1.docx`
- Source provenance: user-provided Discord attachment in this thread

## Header Details
- Title: **SOLUTION REQUIREMENTS DOCUMENT**
- Project: **Rabkin Diagnostics — Clinical Workflow Application**
- Prepared by: **VorsaTech, LLC**
- Version: **1.0**
- Date: **March 2026**
- Status: **Draft v1.0 — March 2026**

## Client & User
- Client: Rabkin Diagnostics, Pittsburgh PA
- Primary user: Dr. John Cangelosi (Physician/Pathologist, remote — Houston TX)
- Lab LIS: VitalAxis (Vital Access)
- Scanner: Motic FlexScan 60 (QPTIFF)

## Core Objective
Reduce physician per-case review time from ~60s to ~20s by removing repetitive clerical entry and integrating queue + viewer + rule-based data entry.

## Hosting Stack
- Frontend: Next.js on Vercel
- Backend: FastAPI on Vercel
- Database: Vercel Postgres (rules, sessions, audit logs; no PHI)

## Scope by Phase
### Phase 1 (Launch)
- Queue from VitalAxis Orders API
- Full-screen slide viewer + diagnosis overlay panel
- Case-keyed slide resolution and pre-loading
- VitalAxis read/write and sign-out flow
- Auth + RBAC

### Phase 2
- Rule engine admin UI
- Auto-suggest ICD/orders/templates
- Historical bootstrap rule set

### Phase 3 (Aspirational)
- Read-only staff view
- OCR enhancement and barcode/OCR fallback

### Phase 4 (Aspirational)
- AI pre-diagnosis (Phikon-v2 + CLAM)
- Attention heatmaps
- GPU inference pipeline

## Non-Functional Highlights
- No PHI persisted outside VitalAxis
- Runtime-only patient data display; no server-side cache
- HIPAA review required pre-launch
- Vercel Enterprise BAA required before go-live

## Priority Blockers / Pre-work
1. Confirm VitalAxis API credential scope (P1 blocker)
2. Confirm Motic server internet/VPN access from Vercel (P1 blocker)
3. Validate Motic tile API compatibility for OpenSeadragon (P1 blocker)
