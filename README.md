<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=190&color=0:0D1117,50:8250DF,100:F0883E&text=Automation%20Platform&fontSize=42&fontColor=FFFFFF&fontAlignY=38&desc=Monorepo%20%E2%80%A2%20Services%20%E2%80%A2%20Control%20Plane%20%E2%80%A2%20Operations&descSize=16&descAlignY=60" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=000" />
  <img src="https://img.shields.io/badge/Monorepo-181717?style=for-the-badge&logo=github&logoColor=white" />
</p>

# Multi-service Automation Platform — public showcase

A sanitised view of a private **18-direction automation monorepo** used to explore and operate multiple service ideas from one engineering foundation.

The original domain includes iGaming-adjacent campaign operations, but this showcase focuses on the **platform engineering**: service boundaries, shared infrastructure, deployment, scheduling, admin tooling and operational controls.

## Portfolio architecture

```mermaid
flowchart TB
    ADMIN[Admin control plane]

    subgraph Product services
      MSG[Messaging / campaign services]
      TG[Telegram services]
      DATA[Data APIs / ingestion]
      AI[AI / content services]
      JOBS[Workers / scheduled jobs]
    end

    subgraph Shared platform
      LIB[Shared libraries]
      DB[(PostgreSQL)]
      SCHED[Scheduler manifest]
      DEPLOY[Deployment tooling]
      OBS[Health / metrics / watchdogs]
    end

    ADMIN --> MSG
    ADMIN --> TG
    ADMIN --> DATA
    ADMIN --> AI

    MSG --> LIB
    TG --> LIB
    DATA --> LIB
    AI --> LIB

    MSG --> DB
    TG --> DB
    DATA --> DB
    AI --> DB
    JOBS --> DB

    SCHED --> JOBS
    DEPLOY --> Product services
    OBS --- Product services
```

## Engineering problems this platform addresses

- Keeping many experiments/services deployable without turning them into one coupled application.
- Shared infrastructure without cross-project business-code imports.
- Service-specific configuration and secret isolation.
- Repeatable migrations and scheduled jobs.
- A single operator control plane without destroying runtime isolation.
- Audit-friendly runbooks and operational documentation.
- Making incomplete/unavailable services explicit instead of pretending the whole portfolio is live.

## Monorepo rules

- Business logic stays inside the owning service.
- Shared modules contain infrastructure-level concerns only.
- Scheduled workloads are versioned.
- Configuration comes from environment/secrets, not committed credentials.
- Production-affecting paths require explicit review boundaries.
- Operational state is documented separately from aspirational architecture.

## Public abstraction of the 18 directions

Instead of publishing the private project names and commercial mechanics, the portfolio is grouped as:

| Group | Examples of engineering work |
|---|---|
| Messaging | email/SMS workflows, scheduling, tracking |
| Telegram | bots, account/session infrastructure, webhook services |
| Data | ingestion, APIs, scraping/processing jobs |
| AI/content | LLM gateway, batch processing, content workflows |
| Infrastructure | provisioning, workers, deployment automation |
| Control plane | admin SPA, portfolio status, operational commands |

## Repository map

- [Architecture](docs/ARCHITECTURE.md)
- [Service boundary rules](docs/BOUNDARIES.md)
- [Sanitised service manifest](examples/service-manifest.json)

## What is deliberately not public

No server IPs, real domains, credentials, payment mechanics, customer data, proprietary campaign logic or production runbooks are included here.
