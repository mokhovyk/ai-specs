# AI Specs

A structured repository for AI specifications, including prompts, agents, rules, skills, and operational guidelines. Designed to standardize and scale AI behavior across systems and workflows.

## Repository Structure

```
ai-specs/
├── skills/           # Reusable AI skill definitions
├── prompts/          # System and user prompts (planned)
├── agents/           # Agent configurations (planned)
└── rules/            # Behavioral rules and constraints (planned)
```

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


## Usage

Reference skills from your AI assistant's configuration or invoke them directly when the trigger conditions match.

**Cursor IDE:** Add the `skills/` directory to your agent skills configuration so the assistant can discover and follow them automatically.

## Contributing

1. Create a new folder under `skills/` with a descriptive kebab-case name
2. Add a `SKILL.md` following the format above
3. Keep instructions deterministic and non-interactive where possible
4. Include validation steps and expected deliverables

## License

MIT
