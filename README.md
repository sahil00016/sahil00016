<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=26&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=620&lines=Hey%2C+I'm+Sahil+%F0%9F%91%8B;SDE+I+%C2%B7+Optimo+Capital;Building+fintech+infrastructure" alt="Typing SVG" />

<br/>

Backend engineer at a fintech NBFC. I design and ship production systems across the full lending stack — REST APIs, async pipelines, internal tooling, and a borrower-facing mobile app. My work sits at the intersection of clean architecture, operational reliability, and integrating LLMs into real financial workflows.

<br/><br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sahil-sonker-1a5234259/)
[![Email](https://img.shields.io/badge/sahil.s%40optimoloan.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:sahil.s@optimoloan.com)

</div>

<br/>

---

### What I ship

**Optimo App** &nbsp;·&nbsp; *Borrower-facing mobile lending platform*
Django REST backend with JWT auth, RBAC, encrypted field storage, Celery async workers, and a Flutter mobile frontend wired to Figma-spec UI. Serves borrowers through the full loan lifecycle.

**Co-lending Gateway** &nbsp;·&nbsp; *Internal ops portal for loan routing*
React 19 + TypeScript frontend backed by a Django API that reads live loan data from an external Synoriq PostgreSQL instance and pushes eligible applications to partner lenders (BHN, GFL). Includes a dynamic field-config engine — visibility rules, validation, and edit permissions driven by config, not hardcoded UI logic.

**Email Intelligence Pipeline** &nbsp;·&nbsp; *Event-driven LLM extraction on AWS*
Gmail → Apps Script (HMAC-signed) → API Gateway → Lambda (FastAPI + Mangum) → AWS Bedrock → structured Pydantic-validated output → downstream Django API. Handles nonce replay detection, PII scrubbing, DLQ fallback to SNS/S3, and an LLM error-repair loop that re-prompts on schema validation failure.

---

### Stack

<div align="center">
  <img src="https://skillicons.dev/icons?i=python,go,ts,dart&perline=4" />
  <br/>
  <img src="https://skillicons.dev/icons?i=django,fastapi,react,flutter&perline=4" />
  <br/>
  <img src="https://skillicons.dev/icons?i=postgres,redis,docker,nginx&perline=4" />
  <br/>
  <img src="https://skillicons.dev/icons?i=aws,rabbitmq,vite,git&perline=4" />
</div>

---

### Engineering focus

- **Layered architecture** — routes → services → repositories, applied consistently across Django, FastAPI, and Go
- **Resilience** — circuit breakers, retry with exponential backoff, Lua-atomic sliding-window rate limiters, SSRF guards
- **RBAC** — resource-scoped roles and permissions with JWT-based auth across all services
- **LLM pipelines** — schema-validated structured output, error-repair loops, DLQ fallback, PII scrubbing
- **Observability** — OpenTelemetry tracing, Prometheus metrics, structured JSON logging with request-id propagation
