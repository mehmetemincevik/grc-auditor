# GRC Auditor

A continuous compliance platform for SOC 2 and ISO 27001 — automated control evidence collection.

## About

I'm building GRC Auditor to solve a problem most compliance teams still handle manually: proving that security controls are actually being enforced, not just documented once during an audit.

The platform models compliance frameworks (starting with SOC 2 and ISO 27001) as a set of controls in the database, then uses automated jobs to pull evidence for each one on a schedule — cloud provider configs, GitHub branch protection rules, employee offboarding logs, and more — and flags whether each control is currently satisfied.

A key evidence source is a built-in OAuth integration risk scanner: it audits the third-party apps connected to a company's SaaS stack (starting with Google Workspace) and flags abandoned-but-still-active or over-privileged integrations, feeding directly into the relevant access-review controls.

## Status

Early development. Currently building the core domain model (frameworks, controls, evidence) and the first OAuth scanning module.

## Tech Stack

- **Backend:** NestJS, TypeORM, PostgreSQL
- **Automation:** n8n for scheduled evidence collection
- **Language:** TypeScript

## Setup

```bash
npm install
npm run start:dev
```

## License

All rights reserved. No license is currently granted for reuse.
