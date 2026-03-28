# Contributing to ClawHub

Thanks for your interest in contributing to ClawHub — the public skill registry for OpenClaw AI agent tools.

## Ways to Contribute

### Publish a Skill
The most impactful contribution is publishing a new skill to clawhub.ai:
1. Create a `SKILL.md` describing your skill
2. Run `clawhub publish <path>` to submit
3. Skills are reviewed by moderators before appearing in search

See [docs/quickstart.md](docs/quickstart.md) for the full publishing workflow.

### Report Issues
- Use [GitHub Issues](https://github.com/tradesmantools/clawhub/issues) for bugs and feature requests
- Search existing issues before creating a new one
- Use the issue templates provided

### Submit Code
1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Make your changes
4. Run tests: `bun test`
5. Run E2E tests: `bun run e2e`
6. Submit a pull request

## Development Setup

```bash
# Prerequisites: bun, Node.js 18+

git clone https://github.com/tradesmantools/clawhub.git
cd clawhub
bun install
bun dev
```

The app runs on `http://localhost:3000`. Convex backend starts automatically.

## Code Standards

- **TypeScript** — strict mode, no `any` types
- **Formatting** — oxlint for linting (see `.oxlintrc.json`)
- **Testing** — vitest for unit tests, Playwright for E2E
- **Commits** — conventional commits: `feat:`, `fix:`, `chore:`, `docs:`
- **PRs** — one logical change per PR, descriptive title, reference issue if applicable

## PR Review Process

1. Automated checks must pass (lint, test, build)
2. One maintainer review required
3. No merge conflicts
4. gitleaks secret scan must pass (pre-commit hook)

## What We're Looking For

**Good first issues:**
- Skill search improvements
- CLI UX enhancements
- Documentation fixes
- Test coverage improvements

**We will NOT merge:**
- New core skills (publish to ClawHub instead)
- Commercial service integrations without clear product justification
- Dependencies that significantly increase bundle size

## Code of Conduct

Be respectful, constructive, and inclusive. We follow the [Contributor Covenant](https://www.contributor-covenant.org/version/2/1/code_of_conduct/).

## Questions?

- Open a [Discussion](https://github.com/tradesmantools/clawhub/discussions)
- Join [Discord](https://discord.gg/clawd)
- Email: info@lv8rlabs.com

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
