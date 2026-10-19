# Stellenagent

Stellenagent is a job-search assistant that helps people find and prepare applications for roles that fit them. It is for job seekers who want practical support organizing their search while staying in control of what gets sent in their name.

## The approval rule

Stellenagent may help research opportunities and prepare application materials, but it must never submit or send an application on its own. The applicant must review and explicitly approve every application before it is sent. This rule applies every time, without exception.

## Development

This project uses [uv](https://docs.astral.sh/uv/) to manage its Python environment and dependencies.

```bash
uv sync --dev
uv run ruff check .
uv run pyright
uv run pytest
```
