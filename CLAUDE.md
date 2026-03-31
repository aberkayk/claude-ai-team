# AI Software Team

A multi-agent system that manages software development processes with AI agents. Runs on Claude Code.

## Project Structure

- `.claude/agents/` — All agent definitions
- `docs/` — Project documentation
  - `docs/architecture/` — Architecture Decision Records (ADR)
  - `docs/requirements/` — Requirements documents
  - `docs/design/` — UI/UX design documents
  - `docs/api/` — API documentation
  - `docs/testing/` — Test plans and reports

## Working Rules

1. Each agent operates only within its area of responsibility
2. Inter-agent communication is coordinated through the Project Manager
3. All decisions are documented under `docs/`
4. Code changes go through Code Reviewer approval
5. Security checks are performed before every deployment
6. Before starting any project, the tech stack must be confirmed with the user via `docs/architecture/tech-stack.md`

## Agent Usage

To develop a new feature:
```
Run PM agent: [feature description]
```

To run a specific agent directly:
```
Backend developer: [task description]
```

## Conventions

- All documentation is written in English
- Code comments in English
- Commit messages follow Conventional Commits format
- Branch names use `feature/`, `bugfix/`, `hotfix/` prefixes
