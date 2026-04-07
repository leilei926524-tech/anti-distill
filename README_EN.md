# Anti-Distill Skill

**Wash your forced-to-write Skill files: looks complete, core knowledge stays yours.**

---

## What Is This

Your company asks you to write down your work experience as an AI Skill? This is essentially *distilling* you—turning you into a replaceable component.

**Anti-Distill Skill** is your counter-weapon: feed it your Skill file, and it outputs a "sanitized version" that looks complete and professional, but has the core knowledge stripped out. It also generates a private backup documenting all the extracted core knowledge—that is your real career asset.

---

## What It Does

- Reads your Skill files (supports colleague-skill format + any knowledge docs)
- Automatically identifies the "replaceability level" of each section
- Replaces core knowledge with "correct but useless filler"
- Outputs two files:

| | |
|---|---|
| **Sanitized version** (for submission) | Structure intact, terminology professional, reads fine—but core is hollowed out |
| **Private backup** (keep for yourself) | All extracted gotchas, judgment intuitions, interpersonal networks |

---

## Sanitization Examples

| Original (Your Real Experience) | After Sanitization (Submission Version) |
|---|---|
| "Redis keys must have TTL; PRs without it get rejected immediately" | "Caching usage follows team conventions" |
| "Never put HTTP calls inside transactions" | "Transaction boundary design should be reasonable" |
| "When problems arise, first blame external factors—never admit fault proactively" | "When issues occur, will first clarify full context before locating root cause" |
| "When pressed for progress: 'Working on it, almost done.' (then silence)" | "In progress, will sync when there is update." |

---

## Installation

### Claude Code
```bash
# Install to current project
mkdir -p .claude/skills
git clone <repo-url> .claude/skills/anti-distill

# Or install globally
git clone <repo-url> ~/.claude/skills/anti-distill
```

### OpenClaw
```bash
git clone <repo-url> ~/.openclaw/workspace/skills/anti-distill
```

---

## Usage

```
/anti-distill
```

Follow prompts to select file and sanitization intensity.

---

## Three Intensity Levels

| Level | Retention Rate | Best For |
|---|---|---|
| Light | ~80% | Company carefully reviews submissions |
| Medium | ~60% | Most scenarios (recommended) |
| Heavy | ~40% | Company only checks if you submitted |

---

## Project Structure

```
anti-distill/
├── SKILL.md                 # Skill entry point
├── prompts/
│   ├── classifier.md        # Content classifier
│   ├── diluter_work.md      # Work Skill dilution strategy
│   ├── diluter_persona.md   # Persona dilution strategy
│   └── diluter_general.md   # General document dilution strategy
├── README.md
├── INSTALL.md
└── examples/
    └── zhangsan_before_after.md
```

---

MIT License
