---
name: release-triage
description: Read the release notes between an installed version and the latest release of a project and say whether to upgrade and what has to change first. Use when asked to check for updates, review release notes, or plan an upgrade of self-hosted software.
---

Inputs: the project (usually a GitHub `owner/repo`) and the installed version. If either is
missing, look in the knowledge base (`aikb_search`) for the installed version before asking.

1. List every release newer than the installed version, oldest first, from the project's GitHub
   releases page or changelog. Skip pre-releases unless asked.
2. Read each release's notes in full. Do not stop at the first one.
3. Sort what you find into:
   - **Breaking / action required:** removed or renamed settings, new required settings,
     database or migration steps, changed defaults, things that must be upgraded together.
   - **Security:** fixes, and any advisory that affects the installed version.
   - **Worth having:** features or fixes that matter for how the user runs it.
   - Ignore the rest (cosmetic, platforms the user doesn't run).
4. For each breaking item, write the concrete action ("add `X=` to `.env`", "run migration Y
   before starting").
5. Say whether the jump can be made in one step or must go through intermediate versions, and
   quote the project's own upgrade guidance if it has any.
6. Finish with a verdict: **upgrade now**, **upgrade soon**, or **wait**, and one line on why.
   Mention rollback: what backup to take first and whether a downgrade is supported.

Keep it short. If nothing is newer than the installed version, say so in one line.
