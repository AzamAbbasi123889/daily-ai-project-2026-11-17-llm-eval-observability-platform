# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] POST /ingest returns 201 and stores record in DB
- [ ] All required fields validated
- [ ] Response includes generated UUID
- [ ] Metrics appear within 30 s of ingestion
- [ ] Metric rows linked to original call via foreign key
- [ ] No failed jobs in Celery dashboard
- [ ] POST /synthetic returns 202 and creates N synthetic calls
- [ ] Generated prompts are stored and can be re‑run via /run-synthetic
- [ ] /calls supports pagination and filtering
- [ ] /metrics/summary returns per‑model average latency, toxicity score, and factuality rate
- [ ] All endpoints return OpenAPI schema
- [ ] Initialize repo, CI pipeline, Docker Compose
- [ ] Create PostgreSQL schema and pgvector extension
- [ ] Implement FastAPI /ingest endpoint
- [ ] Write unit tests for validation
- [ ] Set up Redis & Celery workers
- [ ] Integrate LangChain for factuality check
- [ ] Add Detoxify toxicity scorer
- [ ] Persist MetricResult rows
- [ ] Expose /metrics/summary
- [ ] Build /synthetic endpoint using LLM prompt generation
- [ ] Store generated prompts as SyntheticTest
- [ ] Add /run-synthetic flow
- [ ] Instrument services with OpenTelemetry and verify traces in Jaeger
- [ ] Unit tests for each FastAPI route (pytest)
- [ ] Integration tests exercising full pipeline with a local Llama‑2 judge model
- [ ] Load test using Locust simulating 100 concurrent ingest requests
- [ ] Security test ensuring no raw PII is stored (regex scan)
- [ ] Docker Compose for local dev (fastapi, postgres, redis, celery, jaeger)
- [ ] GitHub Actions builds multi‑arch images and pushes to Docker Hub
- [ ] Deploy to Railway or Render using the same compose file
- [ ] Enable HTTPS via automatic Let's Encrypt

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
