# Architecture

## Control plane vs runtimes

The platform treats the administrative UI as a **control plane**, not as a place to import every project's business code.

```mermaid
flowchart LR
    A[Admin UI] --> G[Control-plane APIs]
    G --> M1[Service A metrics/commands]
    G --> M2[Service B metrics/commands]
    G --> M3[Service C metrics/commands]

    M1 --> D1[(Service-owned data)]
    M2 --> D2[(Service-owned data)]
    M3 --> D3[(Service-owned data)]

    S[Shared infrastructure libs] -.-> M1
    S -.-> M2
    S -.-> M3
```

## Shared concerns

Safe shared modules include:

- database connection/config helpers;
- common payment/integration clients where appropriate;
- structured logging;
- deployment helpers;
- scheduler definitions;
- health/metrics contracts.

Domain decisions stay local to the owning service.

## Deployment concept

Services may share a repository while remaining independently runnable. Deployment automation maps repository components to runtime targets and keeps periodic work in versioned manifests rather than undocumented host cron state.

The public repository intentionally omits real infrastructure inventory.
