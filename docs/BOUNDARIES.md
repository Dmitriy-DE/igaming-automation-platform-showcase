# Service boundary rules

1. A service does not import another service's business logic.
2. Cross-service communication uses explicit contracts.
3. Shared code is infrastructure-oriented, not a dumping ground.
4. Secrets belong to the owning runtime.
5. Admin/control-plane access is explicit and auditable.
6. Scheduled jobs are versioned and reviewable.
7. Deployment state and product readiness are reported separately.
8. A disabled or incomplete capability must look disabled or incomplete.

These rules are more important in a multi-project monorepo than the choice of individual framework.
