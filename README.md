# Rabkin Diagnostics — Clinical Workflow Project (Vorsa)

Persistent project repository for the Rabkin Diagnostics clinical workflow application engagement.

## Source of Truth
- Primary requirements source: `Rabkin_Diagnostics_Clinical_Workflow_SRD_v1.docx` (provided by client thread upload)
- Extracted profile: [`CLIENT_PROFILE.md`](CLIENT_PROFILE.md)
- SRD extraction notes: [`docs/research/2026-03-10-rabkin-srd-v1-extract.md`](docs/research/2026-03-10-rabkin-srd-v1-extract.md)

## Current Status
- Repo rebuilt clean to remove prior unrelated context
- Client profile now sourced only from Rabkin SRD v1

## Project Focus
- Clinical case queue + slide viewer workflow integration
- VitalAxis LIS read/write integration
- Rule engine for diagnosis-driven field pre-population
- HIPAA-aware architecture with no PHI persistence outside VitalAxis
