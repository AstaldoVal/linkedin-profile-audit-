# LinkedIn Profile Audit

**One workflow. Five sections. Any AI assistant.**

A ready-to-use LinkedIn profile audit skill and playbook. Use it in **Claude Code**, **Cursor**, **Manus**, **ChatGPT**, **Claude**, **Gemini**, **Grok**, or **ClawdBot** to run a full profile review with onboarding, section-by-section scoring, and rewrites.

---

## What this is

- **Structured workflow:** onboarding -> assets collection -> section audit -> score (/50) -> rewrites.
- **Five sections:** Profile picture, Banner, Headline, About, Featured.
- **Platform-agnostic:** use as a **skill** where supported (Cursor, Manus), or as **Custom GPT / Project / custom instructions** elsewhere.

---

## Table of contents

- [Installation by platform](#-installation-by-platform)
- [What's inside the repo](#-whats-inside-the-repo)
- [How to use](#-how-to-use)
- [Fallback: one-shot prompt](#-fallback-one-shot-prompt)
- [License](#-license)

---

## Installation by platform

Choose your assistant and follow the steps.

### Claude Code

| Type | Description |
|------|-------------|
| **Skill** | Local skill folder (`.claude/skills/`) |

**Install**

1. Clone or download this repo.
2. Copy this repo into your project at:
   - `.claude/skills/linkedin-profile-audit/`
3. Ensure the folder contains `SKILL.md` and `references/`.
4. Open Claude Code in that project.

**Use:** `/linkedin-profile-audit`

---

### Cursor

| Type | Description |
|------|-------------|
| **Skill** | Agent Skills (`SKILL.md`) supported |

**Install**

1. Clone or download this repo.
2. Copy the repo folder into your Cursor skills directory:
   - **macOS / Linux:** `~/.cursor/skills/linkedin-profile-audit/`
   - Or your project-level skills path.
3. Ensure the folder contains `SKILL.md` and `references/`.
4. Restart or reload Cursor.

**Use:** `/linkedin-profile-audit` or "Use the LinkedIn profile audit skill".

**Details:** [platforms/Cursor/README.md](platforms/Cursor/README.md)

---

### Manus

| Type | Description |
|------|-------------|
| **Skill** | Upload folder or `.zip` with `SKILL.md` |

**Install**

1. In Manus, open **Skills** -> **Upload**.
2. Select this repo folder (or a `.zip` of it).  
3. If only one file is accepted, use `SKILL.md`.

**Use:** invoke the skill in chat (for example, `/linkedin-profile-audit`).

**Details:** [platforms/Manus/README.md](platforms/Manus/README.md)

---

### ChatGPT

| Type | Description |
|------|-------------|
| **Custom GPT** | Instructions + optional Knowledge files |

**Install**

1. In ChatGPT, create/edit a Custom GPT.
2. In **Instructions**, paste [platforms/ChatGPT/Custom_GPT_Instructions.md](platforms/ChatGPT/Custom_GPT_Instructions.md).
3. Optionally upload both reference files to **Knowledge**.

**Use:** Open that GPT and ask for a LinkedIn profile audit.

---

### Claude (claude.ai)

| Type | Description |
|------|-------------|
| **Project** | Project instructions + Knowledge files |

**Install**

1. Create/open a Claude Project.
2. Paste [platforms/Claude/Project_Instructions.md](platforms/Claude/Project_Instructions.md) into project instructions.
3. Add reference files as project knowledge (optional but recommended).

**Use:** Run the audit in this project.

---

### Grok

| Type | Description |
|------|-------------|
| **Custom instructions** | No skill upload |

**Install**

1. Open **Customize Grok**.
2. Paste [platforms/Grok/Custom_Instructions.md](platforms/Grok/Custom_Instructions.md) into instructions.
3. Save.

**Details:** [platforms/Grok/README.md](platforms/Grok/README.md)

---

### Gemini

| Type | Description |
|------|-------------|
| **Gem** | Custom Gem instructions |

**Install**

1. Create or edit a Gem in Gemini.
2. Paste [platforms/Gemini/Custom_Instructions.md](platforms/Gemini/Custom_Instructions.md) into Gem instructions.
3. Optionally upload both files from `references/`.

**Details:** [platforms/Gemini/README.md](platforms/Gemini/README.md)

---

### ClawdBot

| Type | Description |
|------|-------------|
| **Workaround** | Use custom instructions or pasted playbook |

**Install / use**

- If custom instructions are supported, paste [platforms/ClawdBot/Custom_Instructions.md](platforms/ClawdBot/Custom_Instructions.md).
- Otherwise, paste `SKILL.md` in the first message and ask the assistant to follow it.

**Details:** [platforms/ClawdBot/README.md](platforms/ClawdBot/README.md)

---

## What's inside the repo

```
linkedin-profile-audit/
├── README.md
├── SKILL.md
├── references/
│   ├── SOURCE.md
│   ├── profile-audit-examples-extracted.txt
│   └── claude-x-linkedin-auditor-docx-extracted.txt
└── platforms/
    ├── Cursor/
    │   └── README.md
    ├── Manus/
    │   └── README.md
    ├── ChatGPT/
    │   └── Custom_GPT_Instructions.md
    ├── Claude/
    │   └── Project_Instructions.md
    ├── Grok/
    │   ├── README.md
    │   └── Custom_Instructions.md
    ├── Gemini/
    │   ├── README.md
    │   └── Custom_Instructions.md
    └── ClawdBot/
        ├── README.md
        └── Custom_Instructions.md
```

---

## How to use

1. Start with onboarding (who you help, goal, scope).
2. Collect required assets for selected sections.
3. Run section analysis and scoring.
4. Provide rewrites and 2 priority actions.

---

## Fallback: one-shot prompt

If you cannot install a skill or project instructions, paste this into your first message:

```
You are a LinkedIn profile advisor.
Run onboarding first:
1) What I do and who I help (template: I / I help / With what / Result)
2) Main goal on LinkedIn: a) audience b) inbound leads c) profile-to-client conversion d) thought leadership
3) Focus scope: full audit or selected sections

Ask one question at a time.
For full audit: request inputs in this order:
profile picture -> banner (desktop + mobile) -> headline -> about -> featured.

Then audit each chosen section, provide clear fixes, and for full audit output:
Profile Picture X/10
Banner X/10
Headline X/10
About X/10
Featured X/10
TOTAL X/50

Always include concrete rewrites (not only critique) and end with top 2 priority actions.
```

---

## License

Use and redistribute only if you have rights to the source materials in `references/`.

## Attribution

- All source materials in `references/` were provided by **Chris Donnelly**, who is the original author of those materials.
- This skill is an **automation layer** built on top of those reference materials.
