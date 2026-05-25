# Claude Skills

Custom skills for Claude Code — install them to extend Claude with new slash commands.

---

## Available Skills

### `/committee` — Expert Review Panel

Run a virtual expert committee on any idea before you build it.

Four independent agents review your idea from different professional angles and give you objections, questions, and improvement suggestions — so you catch blind spots early.

**The committee:**
| Member | Role | Focuses on |
|--------|------|------------|
| Tali | QA Engineer | What breaks, edge cases, failure modes |
| Roi | Product Manager | Right problem? Right priority? Measurable success? |
| Dana | Customer / End User | Usability, clarity, real-world fit |
| Yonatan | Senior Developer | Technical feasibility, complexity, maintainability |

**Example:**
```
/committee I want to build a Slack bot that summarizes long threads automatically
```

**Output:** Each expert gives 2–3 concerns, 1–2 hard questions, 1 improvement suggestion, and a verdict. Followed by a committee summary with the top 3 issues and a recommended next step.

---

## Installation

**1. Download the skill**
```bash
curl -o ~/.claude/skills/committee.md \
  https://raw.githubusercontent.com/Dadilevi10/claude-skills/main/committee.md
```

**2. Restart Claude Code**

Close and reopen the app — Claude Code loads skills on startup.

**3. Use it**
```
/committee [describe your idea here]
```

---

## Adding More Skills

Drop any `.md` file into `~/.claude/skills/` and restart Claude Code. The filename becomes the slash command name.
