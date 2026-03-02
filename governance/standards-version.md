# Versioning Policy

## 1. Approval-Based Changes Only

Standards are immutable unless explicitly progressed through the governance change management process. No standard may be added, updated, or deprecated without formal review and an approved entry in `approved-changes.log`.

## 2. No Automatic Mutation

AI agents, automated scripts, and CI/CD pipelines are strictly prohibited from automatically mutating any file within the `governance/standards/` directory. All changes must be manually merge-approved by the architectural review board.

## 3. Mandatory Version Referencing

All generated system design specifications, architecture documents, and architectural decision records (ADRs) must explicitly reference the specific standards version they were evaluated against (e.g., `Standards Version: v1.0`). Designs lacking this reference will be rejected.
