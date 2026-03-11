# ADR-001: Repository Reset and Strict Source Provenance

- Date: 2026-03-10
- Status: Accepted

## Context
An earlier update pulled from an unrelated local SRD file, contaminating project context.

## Decision
1. Recreate repository from scratch to remove polluted history/content.
2. Use only user-provided source artifacts (attachment/path) or agent-created task paths.
3. Track source provenance in extraction documents.

## Consequences
- Restores trust and data integrity for client records.
- Increases rigor for future document ingestion.
