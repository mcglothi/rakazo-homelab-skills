# homelab-skills

A small skills-only [Rakazo](https://github.com/elie222/rakazo) plugin for a self-hosted install.

| Skill | Use |
|---|---|
| `kb-first` | Answer questions about the user's own setup from their knowledge base (`aikb_search`, `aikb_read`) first, with sources and dates |
| `release-triage` | Read release notes from the installed version to the latest; list breaking changes, actions, verdict |
| `daily-digest` | Morning brief from the knowledge base, calendar, GitHub and mail, whichever are connected |
| `video-recall` | Find a watched video or ask one a question (`watch_find`, `watch_ask`) |

The tools named here come from a private MCP server on the same network; the skills skip them
when absent. No scripts run: these are instructions only.

Install: **Integrations** → **+** → **From GitHub**, paste this repository URL, **Preview**, **Add**.
Installs are pinned to a commit; to update, remove the plugin and add it again.
