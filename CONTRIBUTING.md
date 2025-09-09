# Contributing Guidelines

## Development Setup

1. Install development dependencies:
   ```bash
   pip install -e .[dev]
   ```

2. Install pre-commit hooks:
   ```bash
   pre-commit install
   ```

3. Install Commitizen (for conventional commits):
   ```bash
   pip install commitizen
   ```

## Code Style

This project uses:
- **Black** for code formatting
- **isort** for import sorting
- **flake8** for linting
- **mypy** for type checking

Run all checks:
```bash
pre-commit run --all-files
```

## Commit Messages

This project uses [Conventional Commits](https://conventionalcommits.org/). Use Commitizen to create proper commit messages:

```bash
cz commit
```

Or manually follow the format:
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

Types:
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes that affect the build system or external dependencies
- `ci`: Changes to our CI configuration files and scripts
- `chore`: Other changes that don't modify src or test files

## Pull Requests

1. Create a feature branch from `main`
2. Make your changes
3. Run tests and linting: `pre-commit run --all-files`
4. Commit with conventional commits
5. Push and create a pull request

## Version Bumping

Use Commitizen to bump versions:
```bash
cz bump
```

This will update the version, create a git tag, and update the changelog.
