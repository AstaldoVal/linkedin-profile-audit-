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

## Installation by platform (same principle as previous skill releases)

### Cursor

Type:
- Skill (`SKILL.md`)

Install path:
- `.claude/skills/linkedin-profile-audit/`

Command example:
- `mkdir -p .claude/skills/linkedin-profile-audit`
- `cp -R /path/to/repo/* .claude/skills/linkedin-profile-audit/`

Use:
- Open Cursor chat and run `/linkedin-profile-audit`

---

### Manus

Type:
- Skill upload (`SKILL.md` or folder)

Install:
1. Open **Skills** in Manus.
2. Upload this folder (or `.zip` of it), or upload `SKILL.md`.
3. Invoke in chat: `/linkedin-profile-audit`.

---

### ChatGPT

Type:
- Custom GPT (instructions + optional knowledge files)

Install:
1. Create or edit a Custom GPT.
2. Paste `SKILL.md` content into GPT Instructions.
3. Optionally upload:
   - `references/profile-audit-examples-extracted.txt`
   - `references/claude-x-linkedin-auditor-docx-extracted.txt`
4. Use in that GPT chat.

---

### Claude (claude.ai)

Type:
- Project Instructions (and optional Project Knowledge files)

Install:
1. Create/open a Project in claude.ai.
2. Paste `SKILL.md` into Project Instructions.
3. Optionally add both files from `references/` as Project Knowledge.
4. Run audit in this Project.

---

### Grok

Type:
- Custom Instructions / Workspace Instructions

Install:
1. Open **Customize Grok** (or Workspace settings).
2. Paste `SKILL.md` into instruction field.
3. Optionally add key excerpts from `references/` in the same instructions or first message.
4. Start audit in that context.

---

### Gemini

Type:
- Gem instructions

Install:
1. Create a Gem.
2. Paste `SKILL.md` into Gem instructions.
3. Optionally upload/reference both files from `references/`.
4. Use this Gem for audits.

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
