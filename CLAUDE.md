# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working in this repository.

## Project Overview

**Repository**: `cloude`
**Owner**: sreekuttanmnj
**Status**: Early-stage / blank canvas — project initialization is not yet complete.

The repository currently contains only a `README.md` with a title. No source code, configuration, dependencies, tests, or CI/CD pipelines exist yet.

---

## Repository Structure

```
cloude/
├── .git/
├── README.md
└── CLAUDE.md   ← this file
```

As the project grows, update this section to reflect the actual directory layout.

---

## Development Workflow

### Branching Convention

- **Main branch**: `master`
- **Feature/task branches**: `claude/<description>-<session-id>` (e.g., `claude/claude-md-mmn04uc5lirikdr8-1cxpz`)
- Always develop on the designated branch — never push directly to `master` without a pull request.

### Committing

- Write clear, descriptive commit messages in the imperative mood (e.g., `Add authentication module`, not `Added auth`).
- Keep commits focused: one logical change per commit.
- Reference issue numbers where applicable (e.g., `Fix login bug (#42)`).

### Pushing

```bash
git push -u origin <branch-name>
```

- Branch names must start with `claude/` when working from a Claude-initiated session.
- Retry on network failures with exponential backoff (2 s → 4 s → 8 s → 16 s), up to 4 retries.

---

## Key Conventions (to be established)

The following sections should be populated as the project matures:

### Language & Framework
- [ ] Define primary language(s) and framework(s)
- [ ] Add language version requirements (e.g., Node 20+, Python 3.12+)

### Code Style
- [ ] Choose and configure a linter / formatter (e.g., ESLint + Prettier, Black + Ruff)
- [ ] Document naming conventions (camelCase, snake_case, PascalCase per context)

### Testing
- [ ] Select a test framework
- [ ] Establish coverage requirements
- [ ] Document how to run tests locally

### Environment Variables
- [ ] Create `.env.example` listing all required environment variables
- [ ] Never commit secrets or `.env` files; add them to `.gitignore`

### Build & Run
- [ ] Document how to install dependencies
- [ ] Document how to start a local development server
- [ ] Document how to build for production

---

## AI Assistant Guidelines

When working in this repository:

1. **Read before editing** — Always read a file in full before modifying it.
2. **Minimal changes** — Only make changes that are directly requested or clearly necessary. Do not refactor unrelated code.
3. **No speculative features** — Do not add features, error handling, or abstractions beyond what is asked.
4. **Security** — Never introduce command injection, SQL injection, XSS, hardcoded secrets, or other OWASP Top 10 vulnerabilities.
5. **No secrets in commits** — Check that `.env`, credential files, and private keys are excluded before committing.
6. **Update this file** — If you add a new language, framework, build tool, or major convention, update the relevant section of this `CLAUDE.md`.

---

## Updating This File

This file should be kept current. Whenever a significant change is made to the project (new tech stack, new tooling, new workflow), update the affected sections. Use the checklist items in "Key Conventions" as prompts for what still needs to be defined.
