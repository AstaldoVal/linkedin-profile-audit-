# linkedin-profile-audit (standalone skill bundle)

LinkedIn profile audit skill bundle: onboarding, section-by-section audit, /50 scoring, and actionable rewrites.

The repository contains:
- `SKILL.md`
- `references/SOURCE.md`
- `references/profile-audit-examples-extracted.txt`
- `references/claude-x-linkedin-auditor-docx-extracted.txt`

---

## Quick start (generic)

1. Copy this repository files into a folder named `linkedin-profile-audit`.
2. Place that folder into your assistant's skills directory (see vendor-specific paths below).
3. Keep this structure intact:
   - `linkedin-profile-audit/SKILL.md`
   - `linkedin-profile-audit/references/*`
4. Restart the client (if needed).
5. Invoke with `/linkedin-profile-audit` or ask: `Run a LinkedIn profile audit`.

---

## Installation by AI vendor / client

### 1) Claude Code

Install path:
- `.claude/skills/linkedin-profile-audit/`

Command example:
- `mkdir -p .claude/skills/linkedin-profile-audit`
- `cp -R /path/to/repo/* .claude/skills/linkedin-profile-audit/`

Use:
- `/linkedin-profile-audit`

### 2) Cursor

Cursor reads project skills from `.claude/skills/`.

Install path:
- `.claude/skills/linkedin-profile-audit/`

Use:
- Open Cursor chat and run `/linkedin-profile-audit`

### 3) Cline / Roo Code (VS Code family)

Most setups use a project-level `.clinerules/skills/` or a custom skill folder declared in settings.

Recommended install path:
- `.clinerules/skills/linkedin-profile-audit/`

Then either:
- Register the folder in your Cline/Roo settings, or
- Place `SKILL.md` where your existing skills are already discovered.

### 4) Gemini CLI

If your Gemini CLI setup supports skill packs, place the folder in your configured skills directory, for example:
- `.gemini/skills/linkedin-profile-audit/`

If your setup uses prompt libraries instead of skills:
- Reference `SKILL.md` as a reusable system prompt file.

### 5) OpenAI Codex CLI / Codex-compatible CLIs

Install path (typical Codex Home):
- `$CODEX_HOME/skills/linkedin-profile-audit/`

If `CODEX_HOME` is not set, check your CLI docs and place it into that tool's skill directory.

### 6) Continue.dev

Continue usually works with prompt/config files rather than native "skills".

Two workable options:
- Put the bundle under `.continue/skills/linkedin-profile-audit/` if your template supports skills.
- Or add `SKILL.md` content as a named prompt/assistant preset in `.continue/config.*`.

### 7) Windsurf / other Claude-compatible clients

If the client supports Claude-style skills, use:
- `.claude/skills/linkedin-profile-audit/`

If not, load `SKILL.md` as a reusable instruction preset and keep `references/` nearby.

---

## Validation checklist

- The client can discover the command `/linkedin-profile-audit`.
- The skill asks onboarding questions one-by-one.
- The skill reads and references files from `references/`.
- Full audit returns scores out of 50.

---

## Updating sources

If your source playbook changes:
1. Re-extract text into:
   - `references/profile-audit-examples-extracted.txt`
   - `references/claude-x-linkedin-auditor-docx-extracted.txt`
2. Update `SKILL.md` criteria if needed.
3. Commit and republish.

---

## License / attribution

Built from user-provided LinkedIn profile audit materials. Redistribute only if you have rights to the source content.
