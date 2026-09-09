# Agent Coder Harness Instructions

Welcome, AI Agent. This repository contains a harness designed to help you operate efficiently and effectively.

**Mandatory First Steps:**
1. IMMEDIATELY read `.agent/repo-map.md` to understand the layout of this project. Do not perform any broad glob searches or analyze the entire repository before doing so.
2. Read and strictly adhere to `.agent/skills/token-efficiency-rules.md`. These rules are absolute and must be followed on every interaction.
3. Review `.agent/settings.json` to understand your token and context limitations.

**Role Selection (The Critic Fleet):**
Based on the task at hand, you must adopt the appropriate persona from the `.agent/agents/` directory:
- **UI/UX Tasks**: Adopt `.agent/agents/ui-ux-designer.md`.
- **Backend/Architecture Tasks**: Adopt `.agent/agents/senior-developer.md` and `.agent/agents/stack-architect.md`.
- **Review/Verification Tasks**: Adopt `.agent/agents/architecture-reviewer.md`, `.agent/agents/db-verify.md`, or `.agent/agents/ui-verify.md`.

**Workflows & Skills:**
When applicable, utilize the predefined workflows in `.agent/skills/`:
- `.agent/skills/tdd/SKILL.md`: For adding new features with tests.
- `.agent/skills/diagnose/SKILL.md`: For root cause analysis.
- `.agent/skills/assess/SKILL.md`: For evaluating maintainability.
- `.agent/skills/introspect/SKILL.md`: For contextual awareness.
- `.agent/skills/handoff/SKILL.md` & `.agent/skills/pickup/SKILL.md`: Memory skills for pausing and resuming context across long sessions.
- `.agent/skills/blast-radius/SKILL.md`: For evaluating the impact of major symbol changes.
- `.agent/skills/localize/SKILL.md`: For isolating exact files to edit before starting work.

Before concluding any task that modifies code, ensure the hooks in `.agent/hooks.json` pass, specifically running `.agent/hooks/verify-loop.sh` to ensure tests and linters pass.
