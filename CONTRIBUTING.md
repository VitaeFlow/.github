# Contributing to VitaeFlow

Thanks for your interest in contributing to VitaeFlow! Whether it's a bug report, a feature idea, or a pull request, every contribution helps.

## Reporting bugs

Open an issue using the **Bug report** template. Include:

- What you expected to happen
- What actually happened
- Steps to reproduce
- SDK/CLI version (`npm list @vitaeflow/sdk` or `vitaeflow --version`)
- Node.js version (`node -v`)

## Suggesting features

Open an issue using the **Feature request** template. Describe the use case — why you need it, not just what you want. This helps us understand the problem and find the best solution.

## Submitting a pull request

1. **Fork** the repo and create a branch from `main`
2. **Install** dependencies: `npm install`
3. **Make** your changes
4. **Test** your changes: `npm test`
5. **Commit** with a clear message describing what you changed and why
6. **Open** a pull request against `main`

### Guidelines

- Keep PRs focused — one concern per PR
- Follow the existing code style
- Add tests for new functionality
- Update the README if your change affects the public API
- Don't bump the version number — maintainers handle releases

### Commit messages

Keep them short and descriptive:

```
Add tolerant mode warning for version mismatch
Fix extract crash when XMP metadata is missing
```

## Project structure

| Repository | Description |
|---|---|
| [vitaeflow-spec](https://github.com/VitaeFlow/vitaeflow-spec) | JSON schema and PDF embedding standard |
| [vitaeflow-js](https://github.com/VitaeFlow/vitaeflow-js) | JavaScript/TypeScript SDK |
| [vitaeflow-cli](https://github.com/VitaeFlow/vitaeflow-cli) | Command-line tool |
| [vitaeflow-web](https://github.com/VitaeFlow/vitaeflow-web) | Website and interactive tools |

## Questions?

Open a discussion or an issue — there are no dumb questions.

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](https://opensource.org/licenses/MIT).
