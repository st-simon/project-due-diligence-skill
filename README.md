# Project Due Diligence Skill

`project-due-diligence` is a portable Codex skill for evaluating new projects, startups, technical ventures, investment targets, and cooperation opportunities.

It uses a fixed diligence structure:

- Project overview
- Technical validation
- Market validation
- Commercialization validation
- Financial model
- Risk list
- Missing materials list
- Investment judgment

The skill now uses a four-layer diligence model:

- Transaction / investment judgment
- Business-plan reality
- Execution / governance
- External risk

The skill requires explicit evidence labeling:

- Use `外部信息` for facts validated through external sources.
- Use `缺乏信息` when a claim is unsupported, unavailable, or cannot be validated.
- Treat project-provided materials as unverified until independently supported.

## Install

The install target should contain:

```text
project-due-diligence/
  SKILL.md
  agents/openai.yaml
  references/due-diligence-case-patterns.md
  references/project-due-diligence-template.md
```

If you clone this repository, install from the bundled skill folder.

macOS / Linux:

```bash
ln -s <repo-path>/project-due-diligence ~/.codex/skills/project-due-diligence
```

Windows:

```powershell
New-Item -ItemType Junction `
  -Path "$env:USERPROFILE\.codex\skills\project-due-diligence" `
  -Target "<repo-path>\project-due-diligence"
```

Use a symbolic link instead of a junction if your Windows environment allows it.

## Usage

After installing and restarting Codex if needed, call the skill by mentioning:

```text
$project-due-diligence
```

Example:

```text
$project-due-diligence Analyze this project document and generate a Markdown diligence report. Use external sources where needed and label unsupported claims as 缺乏信息.
```

## Version

Current skill version: `1.2.1`.

## Changelog

### 1.1.0

- Add structured team validation and set team scoring weight to 20%.
- Add valuation reasonableness as a separate investment scoring dimension.
- Expand compliance and policy risk checks.
- Split competitor pricing into sale price and pricing model.
- Add metadata fields to `agents/openai.yaml`.
- Normalize install instructions across macOS, Linux, and Windows.

### 1.2.0

- Add four-layer diligence model inspired by public Deloitte, ADB, and World Bank reports.
- Add transaction impact language: finding, evidence, transaction impact, recommended action, and status.
- Add execution/governance checks for management accounts, data-room completeness, internal controls, contracts, licenses, and responsibility matrix.
- Add external-risk checks for environment, social, land, community, health and safety, ESG, stakeholder, and grievance topics.
- Bundle `references/due-diligence-case-patterns.md` as a portable case-pattern reference.

### 1.2.1

- Add `author` metadata to `agents/openai.yaml`.
- Clarify four-layer-to-template-section mapping in `SKILL.md`.
- Add income quality / QoE checks to the financial section.
- Add GRM checks for infrastructure, community, public-utility, energy, and government-funded projects.
- Add Chinese finding-language pattern alongside the English pattern.
- Add 1-5 scoring rules for weighted investment judgment.

## Repository Contents

```text
project-due-diligence/
  SKILL.md
  agents/openai.yaml
  references/due-diligence-case-patterns.md
  references/project-due-diligence-template.md
```

No project reports, private diligence materials, workspace state, or local Codex governance files are included.
