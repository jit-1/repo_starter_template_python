# Python Project Starter Template

A comprehensive starter template for Python projects with modern development tools, best practices, and automated quality checks.

## 🚀 Feat### Dependencies

Add your dependencies using Poetry:

```bash
# Add runtime dependency
poetry add requests

# Add development dependency
poetry add --group dev pytest

# Add dependency with specific version
poetry add "numpy>=1.20.0"
```

Update `pyproject.toml` Poetry section:

```toml
[tool.poetry.dependencies]
python = "^3.12"
requests = "^2.31.0"
numpy = "^1.24.0"
# Add your dependencies here

[tool.poetry.group.dev.dependencies]
black = "^23.12.0"
# Add your dev dependencies here
```ern Python Setup**: Configured for Python 3.12+
- **Code Quality Tools**: Black, isort, flake8, mypy, bandit
- **Testing Framework**: pytest with coverage reporting
- **Git Hooks**: Pre-commit hooks for automated code quality
- **Conventional Commits**: Commitizen for standardized commit messages
- **Development Dependencies**: Organized in pyproject.toml
- **Project Structure**: Well-organized directory layout
- **Documentation**: Contributing guidelines and development setup

## 📁 Project Structure

```
├── src/                    # Source code
│   ├── __init__.py
│   └── main.py
├── tests/                  # Test files
│   ├── __init__.py
│   └── test_main.py
├── docs/                   # Documentation
├── .github/               # GitHub configuration
│   └── ISSUE_TEMPLATES/   # Issue templates
├── .pre-commit-config.yaml # Pre-commit hooks configuration
├── pyproject.toml         # Poetry project configuration
├── poetry.lock            # Poetry lock file (generated)
├── .gitignore            # Git ignore rules
├── CONTRIBUTING.md       # Contributing guidelines
├── LICENSE               # License file
└── README.md             # This file
```

## 🛠️ Quick Start

### Prerequisites

- Python 3.12 or higher
- Poetry (Python dependency management)

### Install Poetry

```bash
# Install Poetry (if not already installed)
curl -sSL https://install.python-poetry.org | python3 -

# Or using pip
pip install poetry

# Verify installation
poetry --version
```

### 1. Clone and Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

# Install dependencies (this creates a virtual environment automatically)
poetry install
```

### 2. Setup Development Environment

```bash
# Activate the Poetry shell
poetry shell

# Install pre-commit hooks
pre-commit install

# Install Commitizen (already included in dev dependencies)
# No additional installation needed
```

### 3. Verify Setup

```bash
# Run all pre-commit hooks
pre-commit run --all-files

# Run tests
poetry run pytest tests/

# Run the main script
poetry run python src/main.py
```

## 📝 Usage

### Running the Application

```bash
poetry run python src/main.py
```

### Development Commands

```bash
# Activate Poetry shell
poetry shell

# Format code
poetry run black src/ tests/

# Sort imports
poetry run isort src/ tests/

# Lint code
poetry run flake8 src/ tests/

# Type check
poetry run mypy src/

# Run all quality checks
pre-commit run --all-files

# Run tests with coverage
poetry run pytest tests/ --cov=src --cov-report=html
```

### Poetry Commands

```bash
# Add a new dependency
poetry add package-name

# Add a development dependency
poetry add --group dev package-name

# Update dependencies
poetry update

# Show current environment info
poetry env info

# Remove virtual environment
poetry env remove python

# Export requirements (if needed)
poetry export -f requirements.txt --output requirements.txt
```

### Commitizen Commands

```bash
# Create conventional commit
poetry run cz commit

# Bump version and create tag
poetry run cz bump

# Check current version
poetry run cz version
```

## 🔧 Customization

### 1. Project Information

Update `pyproject.toml`:

```toml
[project]
name = "your-project-name"
version = "0.1.0"
description = "Your project description"
authors = [
    {name = "Your Name", email = "your.email@example.com"},
]
```

### 2. Dependencies

Add your dependencies to `pyproject.toml`:

```toml
dependencies = [
    "requests",
    "numpy",
    # Add your dependencies here
]
```

Or to `requirements.txt` for simple projects.

### 3. Source Code

Replace `src/main.py` with your application code:

```python
def main():
    print("Your application logic here")

if __name__ == "__main__":
    main()
```

### 4. Tests

Add tests to `tests/test_main.py`:

```python
import pytest
from src.main import main

def test_main():
    # Your test logic
    pass
```

### 5. Configuration Files

- **`.pre-commit-config.yaml`**: Customize pre-commit hooks
- **`.flake8`**: Adjust linting rules
- **`.bandit`**: Configure security checks
- **`.markdownlint.json`**: Markdown linting rules

## 🧪 Testing

### Running Tests

```bash
# Run all tests
poetry run pytest

# Run with coverage
poetry run pytest --cov=src --cov-report=html

# Run specific test file
poetry run pytest tests/test_main.py

# Run tests in verbose mode
poetry run pytest -v
```

### Writing Tests

- Tests are located in the `tests/` directory
- Use `pytest` framework
- Follow naming convention: `test_*.py`
- Use descriptive test function names

## 🚀 Deployment

### Building the Package

```bash
# Build distribution
poetry build

# Publish to PyPI (configure credentials first)
poetry publish
```

### Version Management

```bash
# Check current version
poetry run cz version

# Bump patch version
poetry run cz bump --increment patch

# Bump minor version
poetry run cz bump --increment minor

# Bump major version
poetry run cz bump --increment major

# Or use Poetry's version command
poetry version patch
poetry version minor
poetry version major
```

## 🤝 Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on:

- Code of conduct
- Development setup
- Commit message conventions
- Pull request process
- Version bumping

## 📋 Development Workflow

1. **Fork** the repository
2. **Clone** your fork: `git clone https://github.com/yourusername/your-repo-name.git`
3. **Setup** with Poetry: `poetry install && poetry shell`
4. **Install** pre-commit: `pre-commit install`
5. **Create** feature branch: `git checkout -b feature/your-feature-name`
6. **Make** your changes
7. **Run** quality checks: `pre-commit run --all-files`
8. **Write** tests for your changes
9. **Commit** using conventional commits: `poetry run cz commit`
10. **Push** your changes: `git push origin feature/your-feature-name`
11. **Create** a Pull Request

## 🔧 Troubleshooting

### Common Issues

**Pre-commit hooks not running:**
```bash
pre-commit install
pre-commit run --all-files
```

**Poetry environment issues:**
```bash
# Remove and recreate environment
poetry env remove python
poetry install

# Check Poetry configuration
poetry config --list
```

**Import errors:**
```bash
poetry install
poetry run python -c "import src.main"
```

**Python version issues:**
```bash
python --version  # Should be 3.12+
poetry env use python3.12
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙋 Support

If you have any questions or need help:

1. Check the [Contributing Guidelines](CONTRIBUTING.md)
2. Search existing issues
3. Create a new issue using one of our [issue templates](.github/ISSUE_TEMPLATES/)
4. For bugs: Use the **Bug Report** template
5. For features: Use the **Feature Request** template
6. For questions: Use the **Question** template
7. For documentation: Use the **Documentation Update** template

---

**Happy coding! 🎉**
