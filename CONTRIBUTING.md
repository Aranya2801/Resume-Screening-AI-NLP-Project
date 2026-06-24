# Contributing to Resume Screening AI

Thanks for considering a contribution. This project welcomes bug fixes, new
features, documentation improvements, and dataset/benchmark contributions.

## Getting started

1. Fork the repo and clone your fork.
2. Follow the [Quickstart](README.md#quickstart) to get the backend and frontend running locally.
3. Create a branch: `git checkout -b feat/short-description`.

## Development workflow

### Backend

```bash
cd backend
pip install -r requirements.txt
pip install ruff black pytest pytest-cov
ruff check app tests
black app tests
pytest --cov=app
```

### Frontend

```bash
cd frontend
npm install
npm run lint
npm run build
```

## Commit and PR guidelines

- Use clear, present-tense commit messages (`Add skill-gap caching`, not `Added`/`Adding`).
- Keep PRs focused on one change; large unrelated diffs are hard to review.
- Fill out the PR template, including the test checklist.
- New services in `backend/app/services/` should ship with unit tests in `backend/tests/`.
- New API routes should be documented in the README's API table.

## Where to contribute

- **Good first issues**: labeled `good-first-issue` in the issue tracker.
- **Models/ML**: the `training/` pipelines are scaffolded but not yet trained on a real
  labeled dataset — contributions of benchmark datasets (see `datasets/README.md`) or
  trained model weights (with provenance and license) are especially valuable.
- **Qdrant integration**: cross-candidate semantic search via Qdrant is wired at the
  client level but the ingestion job is a stub — see `ROADMAP.md`.
- **i18n / multilingual resumes**: the parser is English-first; multilingual section
  header detection is open for contribution.

## Code style

- Python: `black` formatting, `ruff` linting, type hints on public functions.
- TypeScript: the existing `eslint-config-next` rules; functional React components.

## Reporting bugs / requesting features

Use the issue templates in `.github/ISSUE_TEMPLATE/`.

## Code of Conduct

By participating, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).
