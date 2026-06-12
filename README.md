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

The skill requires explicit evidence labeling:

- Use `外部信息` for facts validated through external sources.
- Use `缺乏信息` when a claim is unsupported, unavailable, or cannot be validated.
- Treat project-provided materials as unverified until independently supported.

## Install

Copy or link the skill directory into your Codex skills folder:

```text
~/.codex/skills/project-due-diligence
```

On Windows:

```text
C:\Users\<your-name>\.codex\skills\project-due-diligence
```

The install target should contain:

```text
project-due-diligence/
  SKILL.md
  agents/openai.yaml
  references/project-due-diligence-template.md
```

If you clone this repository, install from the bundled skill folder:

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

Current skill version: `1.0.0`.

## Repository Contents

```text
project-due-diligence/
  SKILL.md
  agents/openai.yaml
  references/project-due-diligence-template.md
```

No project reports, private diligence materials, workspace state, or local Codex governance files are included.
