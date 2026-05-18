# Vinay Default Plugin

Vinay's default Copilot setup for focused engineering work, pragmatic review, TypeScript/Vite development, frontend UX quality, testing discipline, and UI UX Pro workflows.

## Installation

```bash
copilot plugin marketplace add mistryvinay/awesome-copilot
copilot plugin install vinay-default@awesome-copilot
```

## What's Included

### Agents

| Agent | Description |
| --- | --- |
| `vinay-reviewer` | Pragmatic code review for correctness, security, maintainability, tests, and UI quality. |
| `vinay-senior-engineer` | Focused implementation, debugging, refactoring, and project setup. |

### Skills

| Skill | Description |
| --- | --- |
| `vinay-ui-ux-pro` | Product design, frontend UX, accessibility, responsive layout, and visual polish guidance. |

## Recommended VS Code Settings

```json
{
  "github.copilot.chat.codeGeneration.useInstructionFiles": true,
  "chat.includeApplyingInstructions": true,
  "chat.useAgentSkills": true,
  "chat.instructionsFilesLocations": {
    ".github/instructions": true,
    "~/Development/awesome-copilot/instructions": true
  },
  "chat.agentSkillsLocations": {
    ".github/skills": true,
    "~/.copilot/skills": true,
    "~/Development/awesome-copilot/skills": true
  },
  "chat.agentFilesLocations": {
    ".github/agents": true,
    "~/Development/awesome-copilot/agents": true
  },
  "chat.plugins.marketplaces": [
    "github/awesome-copilot",
    "mistryvinay/awesome-copilot"
  ]
}
```

## Source

This plugin is maintained in [mistryvinay/awesome-copilot](https://github.com/mistryvinay/awesome-copilot).

## License

MIT
