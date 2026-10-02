<p align="center"><img src="./assets/hero.svg" width="100%" alt="Multi-service Automation Platform"/></p>

<table>
<tr>
<td width="50%" valign="top">

### What it is

A private monorepo for **18 service and product directions** across:

- messaging
- Telegram tooling
- APIs
- data processing
- AI/content tooling
- workers
- control-plane services
- deployment/infrastructure

</td>
<td width="50%" valign="top">

### The architectural rule

> **A project owns its own business logic.**

Shared code exists for infrastructure primitives, not as a shortcut for cross-project coupling.

Runtime status is also explicit: some directions are active code, some are inactive, some are patterns/docs.

</td>
</tr>
</table>

<img src="./assets/actual-surfaces.svg" width="100%" alt="Control plane"/>

<br/>

<table>
<tr>
<td width="52%" valign="top">
<img src="./assets/features.svg" width="100%" alt="Platform surface"/>
</td>
<td width="48%" valign="top">

### Portfolio, not a god-process

The control plane aggregates status and operational visibility but does not become the owner of every service.

Each direction keeps its own runtime, schema, secrets, documentation and deployment recipe.

</td>
</tr>
</table>

<img src="./assets/core-model.svg" width="100%" alt="Boundary model"/>

<br/>

<table>
<tr>
<td width="48%" valign="top">

### Current truth

The repository is being prepared for independent cloud deployment.

Historical infrastructure remains documented as history and is not presented as current production state.

</td>
<td width="52%" valign="top">
<img src="./assets/overview.svg" width="100%" alt="Portfolio truth"/>
</td>
</tr>
</table>

<img src="./assets/architecture-visual.svg" width="100%" alt="Architecture"/>

<br/>

<img src="./assets/flow-visual.svg" width="100%" alt="Service onboarding"/>

<br/>

<img src="./assets/engineering-signature.svg" width="100%" alt="Engineering signature"/>

<p align="center"><sub>Private source · public engineering showcase</sub></p>