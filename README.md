<p align="center"><img src="./assets/hero.svg" width="100%" alt="Multi-service Automation Platform"/></p>

<table>
<tr>
<td width="20%" align="center"><b>18 directions</b><br/><sub>service / product portfolio</sub></td>
<td width="20%" align="center"><b>Node + Python</b><br/><sub>polyglot runtimes</sub></td>
<td width="20%" align="center"><b>PostgreSQL</b><br/><sub>owned data</sub></td>
<td width="20%" align="center"><b>Independent deploy</b><br/><sub>service boundaries</sub></td>
<td width="20%" align="center"><b>Control plane</b><br/><sub>read-only portfolio view</sub></td>
</tr>
</table>

<p align="center"><img src="./assets/actual-surfaces.svg" width="100%" alt="Control plane"/></p>

<table>
<tr>
<td width="50%" valign="top"><img src="./assets/features.svg" width="100%" alt="Platform surface"/></td>
<td width="50%" valign="top"><img src="./assets/core-model.svg" width="100%" alt="Boundary model"/></td>
</tr>
</table>

<table>
<tr>
<td width="48%" valign="top"><img src="./assets/overview.svg" width="100%" alt="Portfolio truth"/></td>
<td width="52%" valign="top"><img src="./assets/architecture-visual.svg" width="100%" alt="Architecture"/></td>
</tr>
</table>

<p align="center"><img src="./assets/flow-visual.svg" width="100%" alt="Service onboarding"/></p>
<p align="center"><img src="./assets/engineering-signature.svg" width="100%" alt="Engineering signature"/></p>

<details>
<summary><b>Boundary rules</b></summary>

- projects/A does not import projects/B business logic
- shared code is infrastructure, not a dumping ground
- each runtime owns its secrets and schema
- scheduler / deploy definitions stay versioned
- historical deployment notes do not masquerade as current production
- sensitive lifecycle / money paths use explicit change gates

</details>