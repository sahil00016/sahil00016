### Sahil Sonker

**SDE I · Optimo Capital**

Backend engineer at a fintech NBFC. I design and ship production systems across the full lending stack — REST APIs, async pipelines, internal tooling, and a borrower-facing mobile app. My work sits at the intersection of clean service architecture, operational reliability, and integrating LLMs into real financial workflows.

---

**What I'm shipping**

| Project | What it does | Stack |
|---|---|---|
| **Optimo App** | Borrower-facing mobile lending platform | Django · DRF · Flutter · PostgreSQL |
| **Co-lending Gateway** | Ops portal routing loan applications to partner lenders (BHN, GFL) | Django · React 19 · TypeScript · SQLAlchemy |
| **Email Intelligence Pipeline** | Event-driven pipeline extracting structured data from operational emails via LLMs | FastAPI · AWS Lambda · AWS Bedrock · Pydantic v2 |

---

**Stack**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)

![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white)

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![AWS Lambda](https://img.shields.io/badge/AWS_Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white)
![AWS Bedrock](https://img.shields.io/badge/AWS_Bedrock-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)

---

**Focus areas**

- Layered service architecture — routes → services → repositories, consistent across Django, FastAPI, and Go
- Resilience patterns — circuit breakers, retry with exponential backoff, Lua-atomic rate limiters, SSRF guards
- RBAC — resource-scoped roles and permissions with JWT-based auth
- LLM pipelines — HMAC-verified ingestion, Pydantic-validated structured output, DLQ fallback, PII scrubbing
- Observability — OpenTelemetry tracing, Prometheus metrics, structured JSON logging with request-id propagation

---

**Currently**

Building out the field-config system in the co-lending portal — a dynamic form engine where each field carries its own visibility conditions, validation rules, and edit permissions, driven by config rather than hardcoded UI logic. The goal is ops teams being able to reconfigure what loan data surfaces for a partner without a code deploy.

---

**System architecture**

The three systems I work on are interconnected — the email pipeline feeds structured events directly into the co-lending gateway.

```mermaid
flowchart TD
    subgraph Borrower["Borrower Platform"]
        direction LR
        FLUTTER[Flutter App] --> DJANGO_A[Django REST API]
        DJANGO_A --> PG_A[(PostgreSQL)]
        DJANGO_A --> CELERY[Celery · RabbitMQ]
        DJANGO_A --> VALKEY[(Valkey)]
    end

    subgraph CoLending["Co-lending Gateway"]
        direction LR
        REACT[React 19 Portal] --> DJANGO_B[Django API]
        DJANGO_B --> PG_B[(PostgreSQL)]
        DJANGO_B --> SYNORIQ[(Synoriq DB\nread-only)]
        DJANGO_B --> PARTNERS[BHN · GFL]
    end

    subgraph EmailPipeline["Email Intelligence Pipeline"]
        direction LR
        GMAIL[Gmail] --> SCRIPT[Apps Script\nHMAC sign]
        SCRIPT --> APIGW[API Gateway]
        APIGW --> LAMBDA[Lambda · FastAPI]
        LAMBDA --> BEDROCK[AWS Bedrock\nLLM extraction]
        LAMBDA --> DLQ[DLQ · SNS → S3]
    end

    BEDROCK -->|structured events| DJANGO_B
```

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sahil-sonker-1a5234259/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:sahil.s@optimoloan.com)
