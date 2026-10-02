<p align="center"><img src="./assets/hero.svg" width="100%" alt="Multi-service Automation Platform"/></p>

<p align="center">
  <img src="https://img.shields.io/badge/18-directions-8250DF?style=flat-square"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=000"/>
</p>

# Multi-service Automation Platform

A private monorepo built as a home for **18 service and product directions** across messaging, Telegram tooling, APIs, data processing, AI tooling, content pipelines, workers and infrastructure.

The old showcase undersold the project by treating it as one automation product. It is closer to a **portfolio operating system**: many independent runtimes, shared infrastructure primitives, one administrative/control plane and strict ownership boundaries.

> **Current truth:** the repository is being prepared for independent cloud deployment. This showcase does **not** claim that the historical production topology is currently live.

## <code>01 / actual_surfaces</code>

<p align="center"><img src="./assets/actual-surfaces.svg" width="100%" alt="Automation Platform control plane"/></p>

The control plane aggregates status and metrics, but it is not allowed to become a god-process. Each project keeps its own runtime, schema ownership, secrets, README and operational recipe.

## <code>02 / platform_surface</code>

<p align="center"><img src="./assets/features.svg" width="100%" alt="Automation Platform surface"/></p>

The 18 directions span messaging, Telegram products, data/API services, AI/content tools, commerce/billing foundations, workers and infrastructure. Some are runnable services, some are currently inactive, and some are documentation/pattern references; those states are kept explicit.

## <code>03 / core_model</code>

<p align="center"><img src="./assets/core-model.svg" width="100%" alt="Automation Platform boundary model"/></p>

The central architectural law is simple:

> **projects/A does not import projects/B business logic.**

Shared code exists for infrastructure primitives and deliberately documented control-plane exceptions, not for accidental coupling.

## <code>04 / portfolio_truth</code>

<p align="center"><img src="./assets/overview.svg" width="100%" alt="Automation Platform status model"/></p>

Historical deployment notes remain useful evidence, but history is not presented as current runtime state. Status means what the codebase and current deployment preparation can actually prove.

## <code>05 / architecture</code>

<p align="center"><img src="./assets/architecture-visual.svg" width="100%" alt="Automation Platform architecture"/></p>

The target model is a common monorepo with independently deployable service runtimes, explicit data ownership, versioned scheduling, cloud-agnostic deployment and a read-only portfolio control plane.

## <code>06 / service_onboarding</code>

<p align="center"><img src="./assets/flow-visual.svg" width="100%" alt="Automation Platform service onboarding"/></p>

A new direction needs explicit scope, documentation, schema/runtime ownership, deployment, scheduling and health visibility before it becomes another operational dependency.

## <code>07 / rules_that_keep_it_sane</code>

1. Business logic stays inside the project that owns it.
2. Shared code is infrastructure, not a dumping ground.
3. Secrets belong to the owning runtime.
4. Scheduled work is versioned.
5. Admin is a control plane, not a god-process.
6. Runtime status is factual.
7. Repeated deployment work becomes automation.
8. Sensitive money/lifecycle paths use explicit owner-gated change control.

## <code>08 / engineering_signature</code>

<p align="center"><img src="./assets/engineering-signature.svg" width="100%" alt="Automation Platform engineering signature"/></p>

## <code>09 / inspect</code>

- [Architecture](docs/ARCHITECTURE.md)
- [Boundary rules](docs/BOUNDARIES.md)
- [Sanitised service manifest](examples/service-manifest.json)

<details>
<summary><b>Deliberately not public</b></summary>

Credentials, production hosts, customer data, private provider configuration, payment mechanics and production runbooks are excluded from this showcase.

</details>