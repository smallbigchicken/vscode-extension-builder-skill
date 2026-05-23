# VS Code Extension Builder Skill

This repository contains a reusable agent Skill for creating VS Code extensions end-to-end (scaffold → features → packaging → Marketplace publish checklist).

## What's Included

- Skill (Trae format): `.trae/skills/vscode-extension-builder/SKILL.md`
- Skill (Codex / open skill format location): `.agents/skills/vscode-extension-builder/SKILL.md`

## How to Use (Different Agents)

### Trae (Skills-enabled agents)

1. Open this repository as your workspace
2. The Skill will be discovered at:
   - `.trae/skills/vscode-extension-builder/SKILL.md`

### Codex (recommended install)

Codex discovers skills from repository-scoped `.agents/skills/` and user-scoped `$HOME/.agents/skills/`.

Option A — Repo-scoped (recommended for sharing within a repo):
1. Copy this folder into your target project repository:
   - `.agents/skills/vscode-extension-builder/`
2. Keep `SKILL.md` at:
   - `.agents/skills/vscode-extension-builder/SKILL.md`

Option B — User-scoped (recommended for reuse across all repos on your machine):
- macOS / Linux:
  - `~/.agents/skills/vscode-extension-builder/SKILL.md`
- Windows:
  - `%USERPROFILE%\.agents\skills\vscode-extension-builder\SKILL.md`

After installing, restart Codex and run `/skills` (or `$` skill mention) to confirm it is detected.

#### Quick Install Commands

Repo-scoped install (into an existing project repo):

- macOS / Linux (bash):

```bash
cd /path/to/your/project
git clone https://github.com/smallbigchicken/vscode-extension-builder-skill.git /tmp/vscode-extension-builder-skill
mkdir -p .agents/skills
cp -R /tmp/vscode-extension-builder-skill/.agents/skills/vscode-extension-builder .agents/skills/
```

- Windows (PowerShell):

```powershell
cd D:\path\to\your\project
git clone https://github.com/smallbigchicken/vscode-extension-builder-skill.git $env:TEMP\vscode-extension-builder-skill
New-Item -ItemType Directory -Force .agents\skills | Out-Null
Copy-Item -Recurse -Force $env:TEMP\vscode-extension-builder-skill\.agents\skills\vscode-extension-builder .agents\skills\
```

User-scoped install (available in all repos on this machine):

- macOS / Linux (bash):

```bash
git clone https://github.com/smallbigchicken/vscode-extension-builder-skill.git /tmp/vscode-extension-builder-skill
mkdir -p ~/.agents/skills
cp -R /tmp/vscode-extension-builder-skill/.agents/skills/vscode-extension-builder ~/.agents/skills/
```

- Windows (PowerShell):

```powershell
git clone https://github.com/smallbigchicken/vscode-extension-builder-skill.git $env:TEMP\vscode-extension-builder-skill
New-Item -ItemType Directory -Force $env:USERPROFILE\.agents\skills | Out-Null
Copy-Item -Recurse -Force $env:TEMP\vscode-extension-builder-skill\.agents\skills\vscode-extension-builder $env:USERPROFILE\.agents\skills\
```

### Cursor / Other agents (no native skill discovery)

1. Open `SKILL.md` and copy the full content into your agent’s reusable prompt / custom instructions
2. Use it whenever you need to create/modify/package/publish a VS Code extension

## License

MIT
