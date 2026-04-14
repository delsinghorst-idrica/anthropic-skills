# Skills

A collection of general-purpose agent skills for GitHub Copilot, originally based on [anthropics/skills](https://github.com/anthropics/skills).

Each skill is a self-contained folder containing a `SKILL.md` file (and optionally scripts, references, and assets). Skills are loaded on-demand by the agent when the task matches the skill's description.

## Using as a Git Submodule

This repo is structured so that skill folders live at the root level, making it suitable for use as a git submodule mounted directly at a skills discovery path (e.g. `.github/skills` or `.claude/skills`):

```bash
git submodule add <this-repo-url> .github/skills/anthropic-base
```

## Skills

| Skill | Description |
|---|---|
| [canvas-design](./canvas-design/) | Design and layout for canvas-based artifacts |
| [doc-coauthoring](./doc-coauthoring/) | Structured workflow for co-authoring documents and specs |
| [docx](./docx/) | Create and edit Word documents |
| [frontend-design](./frontend-design/) | Production-grade frontend UI design |
| [internal-comms](./internal-comms/) | Internal communications templates and workflows |
| [mcp-builder](./mcp-builder/) | Build MCP servers in Python or TypeScript |
| [pdf](./pdf/) | Create and manipulate PDF files |
| [pptx](./pptx/) | Create and edit PowerPoint presentations |
| [skill-creator](./skill-creator/) | Create, test, and iterate on new skills |
| [slack-gif-creator](./slack-gif-creator/) | Generate animated GIFs for Slack |
| [theme-factory](./theme-factory/) | Generate design system themes |
| [web-artifacts-builder](./web-artifacts-builder/) | Build multi-component React/Tailwind HTML artifacts |
| [webapp-testing](./webapp-testing/) | Automated web application testing |
| [xlsx](./xlsx/) | Create and edit Excel spreadsheets |

## License

Most skills are Apache 2.0. The document skills (`docx`, `pdf`, `pptx`, `xlsx`) are source-available under Anthropic's terms — see the `LICENSE.txt` in each folder.

# Creating a Basic Skill

Skills are simple to create - just a folder with a `SKILL.md` file containing YAML frontmatter and instructions. You can use the **template-skill** in this repository as a starting point:

```markdown
---
name: my-skill-name
description: A clear description of what this skill does and when to use it
---

# My Skill Name

[Add your instructions here]

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

The frontmatter requires only two fields:
- `name` - A unique identifier for your skill (lowercase, hyphens for spaces)
- `description` - A complete description of what the skill does and when to use it
