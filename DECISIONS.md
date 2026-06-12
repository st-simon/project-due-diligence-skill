# Decisions

## 2026-06-12 - Publish Portable Skill Package

Decision: publish only the portable `project-due-diligence` skill package and minimal repository documentation.

Rationale: the source workspace contains governance state, session records, reports, and local paths that should not be shared as part of a reusable skill.

Included: the skill package, bundled template, and install documentation.

Excluded: private reports, PDFs, extracted text, workspace state, local virtual environments, and temporary dependency folders.
