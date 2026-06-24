# Changelog

All notable changes to this project are documented in this file.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [0.1.0] - 2026-06-19

### Added
- FastAPI backend with resume upload/parsing, job description ingestion, ranking,
  ATS analysis, skill-gap analysis, and recruiter-copilot chat endpoints.
- Resume parsing engine (PDF/DOCX/TXT) with section detection and skill extraction.
- Two-stage semantic matching (bi-encoder + cross-encoder).
- ATS scoring (keyword, formatting, readability sub-scores).
- Rule-based, explainable fraud-risk detection.
- Linear, auditable explainability for every ranking decision.
- SQLAlchemy/PostgreSQL data layer with Alembic migration scaffold.
- Next.js 14 dashboard: landing, upload, candidates, ranking, ATS, skill-gap, copilot chat.
- Docker Compose orchestration (Postgres, Redis, Qdrant, backend, frontend).
- GitHub Actions CI (backend lint/test, Trivy security scan, frontend build).
- Backend unit test suite (17 tests) for parsing, ATS scoring, skill-gap, fraud detection.
- Architecture documentation with Mermaid diagrams.

### Known limitations
- Qdrant is provisioned but not yet used for cross-candidate similarity search.
- No pre-trained ranking model yet — scoring is rule-based/heuristic, not learned.
- No authentication layer yet (single-tenant, trusted-network deployment assumed).

[0.1.0]: https://github.com/your-org/Resume-Screening-AI-NLP-Project/releases/tag/v0.1.0
