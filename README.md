# AI Software Team

A multi-agent system that manages software development processes with AI agents. Runs on Claude Code.

## What Does It Do?

This project defines a complete software development team as AI agents. Each agent works within its area of expertise and is coordinated by the Project Manager agent.

**Key feature:** Before starting any project, the system asks you which technologies you want to use and configures all agents accordingly.

## Agents

| Agent | Role | Model |
|-------|------|-------|
| **Project Manager** | Orchestrator — manages all other agents | Opus |
| **Product Owner** | User stories and prioritization | Sonnet |
| **Business Analyst** | Requirements analysis and documentation | Sonnet |
| **System Architect** | Architecture design and technology decisions | Opus |
| **UI Designer** | Interface design and user experience | Sonnet |
| **Frontend Developer** | Frontend development | Sonnet |
| **Backend Developer** | Server-side development | Sonnet |
| **DBA** | Database design and optimization | Sonnet |
| **DevOps Engineer** | CI/CD, infrastructure, and deployment | Sonnet |
| **Security Engineer** | Security analysis and auditing | Sonnet |
| **QA Tester** | Test planning and automation | Sonnet |
| **Code Reviewer** | Code quality control | Opus |
| **Technical Writer** | Documentation | Sonnet |

## Setup

### Prerequisites
- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed
- Anthropic API key configured

### Usage

1. Clone this repo:
```bash
git clone https://github.com/[username]/ai-software-team.git
cd ai-software-team
```

2. Start Claude Code:
```bash
claude
```

3. Give a task:
```
Run PM agent: Build a user registration system
```

The PM agent will first ask you about your preferred tech stack, then orchestrate the entire development process.

You can also run a specific agent directly:
```
System architect: Design architecture for an e-commerce app
```

## Workflow

```
You ──► Project Manager
              │
              ├─0─► Asks YOU for tech stack preferences
              ├─1─► Product Owner ──► User stories
              ├─2─► Business Analyst ──► Requirements
              ├─3─► System Architect ──► Architecture
              ├─4─► UI Designer ──► Design
              ├─5─► DBA ──► Database schema
              ├─6─► Backend Developer ──► API code
              ├─6─► Frontend Developer ──► UI code (parallel)
              ├─7─► Code Reviewer ──► Code review
              ├─8─► QA Tester ──► Tests
              ├─9─► Security Engineer ──► Security report
              ├─10► DevOps Engineer ──► CI/CD & deploy
              └─11► Technical Writer ──► Documentation
```

## Project Structure

```
.claude/
└── agents/                          # Agent definitions
    ├── project-manager.md
    ├── product-owner.md
    ├── business-analyst.md
    ├── system-architect.md
    ├── ui-designer.md
    ├── frontend-developer.md
    ├── backend-developer.md
    ├── dba.md
    ├── devops-engineer.md
    ├── security-engineer.md
    ├── qa-tester.md
    ├── code-reviewer.md
    └── technical-writer.md
docs/
├── architecture/
│   └── tech-stack.md                # Technology choices (filled with user)
├── requirements/                    # Requirements documents
├── design/                          # UI/UX design documents
├── api/                             # API documentation
└── testing/                         # Test plans and reports
```

## Customization

- **Change tech stack:** Edit `docs/architecture/tech-stack.md` or let the PM agent ask you
- **Add a new agent:** Create a new `.md` file under `.claude/agents/`
- **Change model:** Update the `model` field in agent frontmatter (opus/sonnet/haiku)
- **Restrict tools:** Add/remove tools from the `tools` list in agent frontmatter

## License

MIT
