---
name: project-due-diligence
description: Use when evaluating a new project, startup, investment target, cooperation opportunity, or technical venture with a structured due-diligence template covering project overview, technology, market, commercialization, financial model, risks, missing materials, and investment judgment.
metadata:
  version: 1.2.1
  portable: true
  updated: 2026-06-12
---

# Project Due Diligence

Use this skill when the user asks to analyze, evaluate, diligence, screen, compare, or make an investment/cooperation judgment on a project or startup.

## Version

Current version: `1.2.1` (2026-06-12).

Portable release: bundles the due-diligence template and public due diligence case patterns under `references/`.

## Workflow

1. Read the project materials provided by the user.
2. Treat project materials as unverified claims unless independently supported.
3. Always attempt external validation for material claims about company existence, team credentials, patents, financing, customers, orders, revenue, market size, competitors, pricing, policy support, and technical benchmarks.
4. Mark externally validated facts as `外部信息`.
5. Mark unsupported, unavailable, or inconclusive claims as `缺乏信息`; when useful, further classify them as `未提供`, `外部查无`, or `无法核验`.
6. Structure the analysis in four layers: transaction/investment judgment, business-plan reality, execution/governance, and external risk.
7. Use `references/project-due-diligence-template.md` as the output structure.
8. Lead with a concise recommendation: `推荐`, `谨慎推进`, `暂缓`, or `不建议`.
9. End with deal breakers, price/term implications, highest-priority missing materials, and next checks.

Layer-to-section mapping:

- Layer 1, transaction/investment judgment: quick conclusion plus `## 9. 交易/投资判断`, including transaction impact matrix and action plan.
- Layer 2, business-plan reality: `## 2. 技术验证`, `## 3. 市场验证`, `## 4. 商业化验证`, and `## 6. 财务测算`.
- Layer 3, execution/governance: `## 1. 项目概况` team table and `## 5. 执行与治理验证`.
- Layer 4, external risk: `## 7. 风险清单`, especially compliance and external-risk checks.

## Required Template

Load this reference when producing a formal diligence write-up:

```text
references/project-due-diligence-template.md
```

Use this reference when adapting scope, language, and risk expression from public due diligence examples:

```text
references/due-diligence-case-patterns.md
```

## Evidence Rules

- Treat BP, pitch decks, interviews, and user-provided files as project materials, not verified facts.
- Use contracts, payment records, third-party reports, official registries, public patents, and customer-verifiable evidence as high-confidence proof.
- Do not accept market-size, valuation, order, patent, financing, or revenue numbers without a source.
- If external validation cannot be completed, say so explicitly and use `缺乏信息` rather than treating project materials as verified.
- When judging hardware or instrument projects, inspect BOM, key suppliers, unit economics, reliability, calibration, after-sales, and manufacturing readiness.
- For investment use cases, score team strength explicitly and treat valuation reasonableness as separate from financial health.
- Express material findings as issue -> transaction impact -> recommended action whenever the evidence supports it.
