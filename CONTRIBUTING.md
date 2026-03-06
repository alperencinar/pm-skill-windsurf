# Contributing

This is a Windsurf adaptation of the [PM Skills Marketplace](https://github.com/phuryn/pm-skills) originally created by [Paweł Huryn](https://www.productcompass.pm). Contributions are welcome — whether it's a bug fix, a typo, or a new skill idea.

## How to Contribute

- **Bugs and small fixes** — open a PR directly.
- **New skills, workflows, or larger changes** — open an issue first so we can discuss the approach.

## Guidelines

- Keep PRs focused — one change per PR.
- **Skills** live in `skills/<domain>/` as markdown files with `name` and `description` frontmatter.
- **Workflows** live in `.windsurf/workflows/` as markdown files with `description` frontmatter. They are invoked via `/slash-command` in Windsurf Cascade.
- Workflows reference skills via file paths (e.g., `read skills/pm-execution/create-prd.md`).
- Suggest follow-up workflows in natural language only.

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](LICENSE).
