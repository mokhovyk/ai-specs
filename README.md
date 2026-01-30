# AI Specs

A structured repository for AI specifications, including prompts, agents, rules, skills, and operational guidelines. Designed to standardize and scale AI behavior across systems and workflows.

## Repository Structure

```
ai-specs/
├── agents/           # AI persona and behavior definitions
├── prompts/          # User prompt templates for common tasks
├── rules/            # Behavioral rules and constraints
└── skills/           # Reusable AI skill definitions
```

## Agents

Agent definitions configure how an AI assistant behaves. Each file defines a persona with objectives, constraints, and output format.

| Agent | Purpose |
|-------|---------|
| `code-assistant.md` | General TypeScript/React coding tasks |
| `code-reviewer.md` | Pull request review with prioritized feedback |
| `refactor-agent.md` | Safe, incremental code improvements |
| `documentation.md` | Technical writing and doc generation |

## Prompts

User prompt templates for common task types. Copy and fill in the blanks.

| Template | Use When |
|----------|----------|
| `feature-request.md` | Implementing new functionality |
| `bug-fix.md` | Diagnosing and fixing issues |
| `migration.md` | Upgrading dependencies or patterns |
| `review-request.md` | Requesting code review |

## Skills

Skills are self-contained instructions that teach AI assistants how to perform specific tasks. Each skill lives in its own folder under `skills/` and follows a consistent format.

### Skill Format

Each `SKILL.md` file contains:

1. **Frontmatter** — YAML metadata with `name` and `description`
2. **Title and summary** — What the skill does
3. **Requirements** — Constraints and prerequisites
4. **High-Level Plan** — Step-by-step execution guide
5. **Operational Guidance** — Decision-making heuristics
6. **Deliverables** — Expected outputs

## Rules

Rules define behavioral constraints applied to specific file types or contexts. Stored as `.mdc` files with frontmatter specifying glob patterns.

| Rule | Applies To |
|------|------------|
| `typescript-standards.mdc` | `**/*.{ts,tsx}` |

## Usage

Reference specs from your AI assistant's configuration or invoke them directly when trigger conditions match.

**Cursor IDE:** Add the `skills/` directory to your agent skills configuration so the assistant can discover and follow them automatically.

## Contributing

1. **Agents** — Add a new `.md` file under `agents/`
2. **Prompts** — Add a new `.md` file under `prompts/`
3. **Skills** — Create a folder under `skills/` with a `SKILL.md` file
4. **Rules** — Add a `.mdc` file under `rules/` with appropriate globs

Keep instructions deterministic and non-interactive where possible. Include validation steps and expected deliverables.

## License

MIT
