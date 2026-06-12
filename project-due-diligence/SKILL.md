---
name: project-due-diligence
description: Use when evaluating a new project, startup, investment target, cooperation opportunity, or technical venture with a structured due-diligence template covering project overview, technology, market, commercialization, financial model, risks, missing materials, and investment judgment.
metadata:
  version: 1.0.0
  portable: true
  updated: 2026-06-12
---

# Project Due Diligence

Use this skill when the user asks to analyze, evaluate, diligence, screen, compare, or make an investment/cooperation judgment on a project or startup.

## Version

Current version: `1.0.0` (2026-06-12).

Portable release: bundles the due-diligence template under `references/` and requires external validation attempts for material claims.

## Workflow

1. Read the project materials provided by the user.
2. Treat project materials as unverified claims unless independently supported.
3. Always attempt external validation for material claims about company existence, team credentials, patents, financing, customers, orders, revenue, market size, competitors, pricing, policy support, and technical benchmarks.
4. Mark externally validated facts as `外部信息`.
5. Mark unsupported, unavailable, or inconclusive claims as `缺乏信息`.
6. Use `references/project-due-diligence-template.md` as the output structure.
7. Lead with a concise recommendation: `推荐`, `谨慎推进`, `暂缓`, or `不建议`.
8. End with the highest-priority missing materials and next checks.

## Required Template

Load this reference when producing a formal diligence write-up:

```text
references/project-due-diligence-template.md
```

## Evidence Rules

- Treat BP, pitch decks, interviews, and user-provided files as project materials, not verified facts.
- Use contracts, payment records, third-party reports, official registries, public patents, and customer-verifiable evidence as high-confidence proof.
- Do not accept market-size, valuation, order, patent, financing, or revenue numbers without a source.
- If external validation cannot be completed, say so explicitly and use `缺乏信息` rather than treating project materials as verified.
- When judging hardware or instrument projects, inspect BOM, key suppliers, unit economics, reliability, calibration, after-sales, and manufacturing readiness.
