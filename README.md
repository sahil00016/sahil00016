<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:132f4c,100:0d1117&height=220&section=header&text=Sahil%20Sonker&fontSize=56&fontColor=58A6FF&fontAlign=50&fontAlignY=42&desc=Full-Stack%20Engineer%20%20%C2%B7%20%20Systems%20Thinker%20%20%C2%B7%20%20Optimo%20Capital&descAlign=50&descAlignY=62&descSize=17&descFontColor=8b949e&animation=fadeIn" />

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=2800&pause=900&color=58A6FF&center=true&vCenter=true&width=560&lines=Building+fintech+systems+end+to+end;REST+APIs+%E2%80%94+async+pipelines+%E2%80%94+mobile+apps;Service+design+%7C+resilience+%7C+LLM+pipelines;Django+%C2%B7+React+%C2%B7+Flutter+%C2%B7+Go+%C2%B7+FastAPI" alt="Typing SVG" />

<br/>

[![LinkedIn](https://img.shields.io/badge/Let's%20connect-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sahil-sonker-1a5234259/)
[![Gmail](https://img.shields.io/badge/sahilsonker2025%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sahilsonker2025@gmail.com)

</div>

<br/>

```python
class SahilSonker:
    role        = "SDE I  ·  Optimo Capital"
    type        = "Full-Stack Engineer  ·  Systems Thinker"

    languages   = ["Python", "Go", "TypeScript", "Dart"]
    frameworks  = ["Django", "FastAPI", "React 19", "Flutter"]
    infra       = ["PostgreSQL", "Redis", "Docker", "AWS Lambda", "RabbitMQ"]

    ships       = [
        "Borrower-facing mobile lending platform  (Django + Flutter)",
        "Co-lending ops portal with partner routing  (Django + React 19)",
        "Event-driven LLM email intelligence pipeline  (FastAPI + AWS Bedrock)",
    ]

    interests   = ["System design", "Event-driven architecture", "LLMs in production"]
    currently   = "Building a config-driven dynamic field engine for co-lending ops"
    ask_me_about = "How three production systems talk to each other"
```

<div align="center">

</div>

<br/>

---

### What I ship

**Optimo App** &nbsp;·&nbsp; *Borrower-facing mobile lending platform*  
Full-stack — Flutter mobile UI built to Figma spec, backed by a Django REST API with JWT auth, resource-scoped RBAC, encrypted field storage, and Celery async workers over RabbitMQ. Borrowers move through the full loan lifecycle on this.

**Co-lending Gateway** &nbsp;·&nbsp; *Internal ops portal for loan routing*  
React 19 + TypeScript (TanStack Query, Zustand, shadcn/ui) on the front, Django + SQLAlchemy on the back — reading live loan data from an external Synoriq PostgreSQL instance and pushing eligible applications to partner lenders. Includes a config-driven field engine where visibility rules, validation, and edit permissions are data, not code.

**Email Intelligence Pipeline** &nbsp;·&nbsp; *Event-driven LLM extraction on AWS*  
Gmail → HMAC-signed Apps Script → API Gateway → Lambda (FastAPI + Mangum) → AWS Bedrock → Pydantic-validated structured output → downstream Django API. Nonce replay detection, PII scrubbing, DLQ fallback to SNS/S3, and an LLM self-repair loop that re-prompts on schema validation failure.

---

### Stack

<div align="center">

**Languages**

<img src="https://skillicons.dev/icons?i=python,go,ts,dart&perline=8" />

**Frameworks & UI**

<img src="https://skillicons.dev/icons?i=django,fastapi,react,flutter&perline=8" />

**Data & Infra**

<img src="https://skillicons.dev/icons?i=postgres,redis,docker,nginx,aws,rabbitmq,vite,git&perline=8" />

</div>

---

### Engineering focus

- **System design first** — think in service boundaries, contracts, and failure modes before writing code
- **Full-stack ownership** — schema → API → UI, with consistent patterns (response envelopes, RBAC, layered services) across the whole surface
- **Resilience** — circuit breakers, retry with exponential backoff, Lua-atomic rate limiters, SSRF guards
- **LLM pipelines** — schema-validated structured output, self-repair loops, DLQ fallback, PII scrubbing
- **Observability** — OpenTelemetry tracing, Prometheus metrics, structured JSON logging with request-id propagation

<br/>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:132f4c,100:0d1117&height=120&section=footer&animation=fadeIn" />
