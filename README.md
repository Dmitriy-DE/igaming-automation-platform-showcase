<p align="center"><img src="./assets/hero.svg" width="100%" alt="Automation Platform"/></p>

<p align="center">
  <img src="https://img.shields.io/badge/18-directions-8250DF?style=flat-square"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=000"/>
</p>

# Multi-service Automation Platform

A private monorepo I built as a home for **18 service/product directions**: messaging, bots, APIs, data processing, AI tooling, workers and infrastructure.

The public showcase strips out the sensitive mechanics and keeps the platform engineering.

<p align="center"><img src="./assets/product-mockup.svg" width="100%" alt="Automation Platform control plane mockup"/></p>

<p align="center"><sub>Illustrative records; screen hierarchy, labels and visual system are reconstructed from the private source.</sub></p>

## <code>01 / actual_surfaces</code>

<p align="center"><img src="./assets/actual-surfaces.svg" width="100%" alt="Actual product surfaces"/></p>

## <code>02 / platform_surface</code>

<p align="center"><img src="./assets/features.svg" width="100%" alt="Automation Platform features"/></p>

## <code>03 / core_model</code>

<p align="center"><img src="./assets/core-model.svg" width="100%" alt="Runtime model"/></p>

## <code>04 / architecture</code>

<p align="center"><img src="./assets/architecture-visual.svg" width="100%" alt="Automation Platform architecture"/></p>

<p align="center"><img src="./assets/overview.svg" width="100%" alt="Automation Platform system overview"/></p>

## <code>05 / service_onboarding</code>

<p align="center"><img src="./assets/flow-visual.svg" width="100%" alt="Automation Platform service flow"/></p>

## <code>06 / rules_that_keep_it_sane</code>

1. A project does not import another project's business logic.
2. Shared code is infrastructure, not a dumping ground.
3. Secrets belong to the owning runtime.
4. Scheduled work is versioned.
5. Admin is a control plane, not a god-process.
6. Runtime status is factual.
7. Repeated deployment work becomes automation.

## <code>07 / engineering_signature</code>

<p align="center">
  <img src="./assets/engineering-signature.svg" width="100%" alt="Engineering signature"/>
</p>

## <code>08 / inspect</code>

- [Architecture](docs/ARCHITECTURE.md)
- [Boundary rules](docs/BOUNDARIES.md)
- [Sanitised service manifest](examples/service-manifest.json)

<details><summary><b>Deliberately not public</b></summary>

Server IPs, real domains, credentials, payment mechanics, customer data, proprietary campaign logic and production runbooks.

</details>
