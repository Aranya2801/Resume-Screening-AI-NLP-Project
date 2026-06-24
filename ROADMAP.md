# Roadmap

## Near-term (v0.2)
- [ ] Wire Qdrant ingestion: embed every parsed resume on upload, enable
      cross-candidate similarity search and the duplicate-content fraud check.
- [ ] Authentication (JWT) + role-based access (recruiter / candidate / admin).
- [ ] Redis-backed caching for embedding computations (currently recomputed per request).
- [ ] Resume upload batch mode (zip of resumes → bulk parse + rank).

## Mid-term (v0.3)
- [ ] LangChain-based multi-agent orchestration wiring the existing services
      (Resume Analyzer, ATS, Skill Gap, Recruiter Assistant, Candidate
      Recommendation, Interview Question Generator, Hiring Decision) into
      autonomous agents with tool-calling, rather than direct function calls.
- [ ] Interview Question Generator using the job description + skill gaps as context.
- [ ] Multilingual resume parsing (spaCy multilingual pipelines + section-header
      translation tables).
- [ ] Admin dashboard: usage analytics, model performance monitoring.

## Long-term (v1.0)
- [ ] Train a learned ranking model (e.g. gradient-boosted reranker) on real
      labeled hiring-outcome data, with SHAP-based explanations
      (`training/evaluation/shap_explain.py`), replacing/augmenting the current
      heuristic weighted-sum scorer.
- [ ] MLflow experiment tracking + model registry for the trained ranking model.
- [ ] DVC for dataset versioning once a labeled benchmark dataset is adopted.
- [ ] Terraform modules for AWS ECS, Azure Container Apps, and GCP Cloud Run.
- [ ] SOC 2-oriented audit logging for candidate-data access.

## Always open for contribution
- Expanding `KNOWN_SKILLS` taxonomy into a maintained, sourced `datasets/skills_taxonomy.csv`.
- More fraud-detection heuristics with documented false-positive analysis.
- Accessibility pass on the frontend (keyboard nav, screen-reader labels).
