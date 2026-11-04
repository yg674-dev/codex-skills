# Codex Skills

Reusable skills for OpenAI Codex, maintained by yg674-dev.

## Included skills

| Skill | Purpose |
| --- | --- |
| [Persuasive Communication](.agents/skills/persuasive-communication/SKILL.md) | Audience-centered pitches, presentations, interviews, storytelling, and stakeholder communication. |
| [Deep Problem Solving](.agents/skills/deep-problem-solving/SKILL.md) | Outcome-first analysis, primary-source research, cross-disciplinary methods, adversarial review, and independent verification. |

## Install

For project-local use, copy the `.agents/skills/` directory into the root of your Codex project.

For personal use across projects, copy each skill folder to `~/.agents/skills/` (or your Codex installation's configured user-skill directory).

Example:

```bash
git clone https://github.com/yg674-dev/codex-skills.git
mkdir -p ~/.agents/skills
cp -R codex-skills/.agents/skills/. ~/.agents/skills/
```

Restart or refresh Codex skill discovery if necessary.

## Suggested usage

- “Use deep-problem-solving to investigate why revenue dropped and independently verify the root causes.”
- “Use persuasive-communication to turn the findings into a compelling 5-minute executive pitch.”
- Combine both: rigorous evidence first, persuasive communication second.

These files are instructions, not a substitute for access to real data or independent validation.
