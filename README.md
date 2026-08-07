# claude-workspace

Personal Claude Code workspace — a private backup/sync point for skills, plugins,
and project automations so they're available across devices (including
Claude Code on iPhone).

## Structure

- **`skills/`** — Full skill definitions (instructions, scripts, references) copied
  from a Claude Code session's `~/.claude/skills`. Includes both Anthropic's
  built-in skills (`pdf`, `docx`, `pptx`, `xlsx`, `learn`, `algorithmic-art`,
  `web-artifacts-builder`, `mcp-builder`, `skill-creator`) and custom-added
  skills (`council`, `frontend-design`, `find-skills`, `linkedin-profile-optimizer`,
  `grill-me`, `humanizer`, `prompt-master`, `book-to-skill`, `hormozi`, `hallmark`,
  `session-start-hook`).
- **`plugins/`** — No plugins were installed in the session this was captured
  from. Drop plugin folders here as you install them.
- **`projects/`** — Workspace for building things and automations with Claude
  Code — scripts, small tools, in-progress projects.

## Usage

Clone this repo wherever you're running Claude Code (including mobile) to bring
your skills and in-progress projects along:

```
git clone https://github.com/miguelf3006/claude-workspace.git
```

To make skills available to a Claude Code session, copy or symlink the
relevant folders from `skills/` into that environment's `~/.claude/skills/`.
