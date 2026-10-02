<p align="center"><img src="./assets/hero.svg" width="100%" alt="Multi-service Automation Platform"/></p>

> **A monorepo portfolio containing 18 service / product directions.**  
> It is not one monolithic “iGaming automation app”. The engineering problem is keeping many different runtimes, data owners and operational paths inside one repository without letting them collapse into one god-process.

<table>
<tr>
<td align="center"><b>18 directions</b><br/><sub>services / products / patterns</sub></td>
<td align="center"><b>Node + Python</b><br/><sub>polyglot runtimes</sub></td>
<td align="center"><b>PostgreSQL</b><br/><sub>data services</sub></td>
<td align="center"><b>Admin SPA</b><br/><sub>portfolio control plane</sub></td>
<td align="center"><b>Versioned jobs</b><br/><sub>schedulers / deploy</sub></td>
<td align="center"><b>No live prod claim</b><br/><sub>current repo truth</sub></td>
</tr>
</table>

## Portfolio map

<p align="center"><img src="./assets/readme-portfolio.svg" width="100%" alt="Automation platform portfolio"/></p>

<table>
<tr>
<td width="33%" valign="top"><b>Not every direction is a separate server.</b><br/><sub>Some entries are full runtimes, some are code paths inside another runtime, and some are documentation/pattern references.</sub></td>
<td width="33%" valign="top"><b>Status is factual.</b><br/><sub>The repository currently does not claim a live production topology. Historical deployment material remains history, not present-state marketing.</sub></td>
<td width="33%" valign="top"><b>The control plane is observational.</b><br/><sub>Admin/portfolio views aggregate operational information but should not become the owner of every service’s business logic.</sub></td>
</tr>
</table>

## Main rule

<p align="center"><img src="./assets/readme-boundary-law.svg" width="100%" alt="Monorepo boundary rule"/></p>

> **Cross-project imports are forbidden except through shared infrastructure or explicitly documented offline/read-only/control-plane exceptions.**

## How a direction becomes operational

<p align="center"><img src="./assets/flow-visual.svg" width="100%" alt="Service onboarding"/></p>

<table>
<tr>
<td width="33%" valign="top"><b>Scope + README</b><br/><sub>Each direction must explain purpose, runtime, data ownership, environment and operational contract.</sub></td>
<td width="33%" valign="top"><b>Schema + runtime</b><br/><sub>Migrations, secrets, schedules and deploy recipes belong to the owning service boundary.</sub></td>
<td width="33%" valign="top"><b>Health + control plane</b><br/><sub>The service exposes enough operational state to be observed without giving the admin layer ownership of its internals.</sub></td>
</tr>
</table>

## Change-sensitive paths

<table>
<tr>
<td width="50%" valign="top"><b>Money/lifecycle path</b><br/><sub>Critical mailer lifecycle files are explicitly frozen behind owner approval. The repository treats this as a change-control boundary, not a suggestion.</sub></td>
<td width="50%" valign="top"><b>Versioned operations</b><br/><sub>Schedulers, deployment manifests and repeated operational work stay in Git so runtime behaviour can be reviewed instead of reconstructed from server folklore.</sub></td>
</tr>
</table>

## Architecture

<p align="center"><img src="./assets/architecture-visual.svg" width="100%" alt="Automation platform architecture"/></p>

<table>
<tr>
<td width="33%" valign="top"><b>Independent runtime target</b><br/><sub>Services are being prepared to deploy independently into cloud/runtime targets rather than depending on one historical host topology.</sub></td>
<td width="33%" valign="top"><b>Owned data / secrets</b><br/><sub>Each runtime owns the credentials and data paths required for its own contract.</sub></td>
<td width="33%" valign="top"><b>Shared infrastructure only where deliberate</b><br/><sub>Common DB config/adapters may be shared; product-specific business rules remain local.</sub></td>
</tr>
</table>

## Engineering signature

<p align="center"><img src="./assets/engineering-signature.svg" width="100%" alt="Engineering signature"/></p>

<details>
<summary><b>Current-state note</b></summary>

The source repository explicitly states that there is **no currently claimed live production fleet**. Historical server/topology documents describe prior or target states; the current engineering goal is independent cloud deployment with explicit ownership and versioned operations.

</details>