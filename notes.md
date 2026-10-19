
# Project initialisation
uv init
uv add --dev (add dependency here)

uv sync
uv run ruff check . [# ruff checks code style] 
uv run pyright [pyright checks types]
uv run pytest [pyright look for tests]

[uv sync reads the project’s pyproject.toml and uv.lock, then makes the project’s virtual environment match them: it installs missing packages, updates packages that are out of sync, and removes ones that aren’t needed. It doesn’t change your source code.]



uv add --dev pre-commit
nano .pre-commit-config.yaml

Paste this in:
repos:
  - repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.17.1
    hooks:
      - id: ruff-check
      - id: ruff-format

uv run pre-commit install
uv run pre-commit run --all-files


[https://github.com/astral-sh/ruff-pre-commit is Astral’s public GitHub repository for Ruff’s pre-commit hooks. Astral also makes Ruff.
The config tells pre-commit to fetch those hooks from that repository. It then runs two checks before a commit:
- ruff-check flags Python code issues, like unused imports.
- ruff-format checks whether the code follows Ruff’s formatting rules.]


[Ruff is a fast tool for checking and formatting Python code.]