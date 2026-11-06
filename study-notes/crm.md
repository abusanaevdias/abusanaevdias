# 19 — Frappe CRM: engineering study notes

> Study annotation for [frappe/crm](https://github.com/frappe/crm), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study/library fork of [frappe/crm](https://github.com/frappe/crm). The application, existing commits and upstream documentation remain the work of their original authors and contributors. The local contribution prepared for this library is this engineering note; it is not a claim to have built, deployed or operated the upstream product. Preserve the upstream README and every license file unchanged.

Review date: 2026-11-07 (Asia/Almaty). Snapshot time: 2026-11-06T21:21:43Z. Default branch: `develop`. Exact reviewed commit: [`986fea3e525a42ecab034b4e16ef784041552f78`](https://github.com/frappe/crm/commit/986fea3e525a42ecab034b4e16ef784041552f78). Later upstream changes are outside this snapshot.

## Purpose and a specific study use case

CRM application built on Frappe Framework and a Vue-based frontend, for leads, deals, activities and configurable sales workflows.

A bounded study use case is to inspect the existing data flow and API boundaries with synthetic fixtures before deciding whether to attempt the extension below. This note does not establish feature correctness, production readiness or an implemented integration.

## Setup and API dependencies

- Default branch develop is explicitly unstable/future v2; README points stable v1.x deployments to main and matching Frappe/ERPNext branches.
- Source app metadata requires Python >=3.10, but the full runtime requires a compatible Frappe Bench environment and framework dependencies, not standalone pip installation.
- Current pyproject lists Frappe and WhatsApp Bench dependencies. Development uses Bench/site setup and Yarn frontend tooling; the supplied Docker example includes MariaDB 10.8, Redis and a Bench container.

- Frappe REST APIs use the permissions of an authenticated user, through token key/secret or another supported auth method.
- Twilio, Exotel, WhatsApp and ERPNext integrations require their own compatible apps/accounts/credentials when enabled; no integration or outbound messaging was configured.

No hosted site, telephony/WhatsApp account, API token or paid service was created. Basic self-hosting has infrastructure costs; optional communication providers and Frappe Cloud have separate terms/billing.

## License boundary

Primary license: [LICENSE](https://github.com/frappe/crm/blob/986fea3e525a42ecab034b4e16ef784041552f78/LICENSE). Declared identifier: `AGPL-3.0`. Root LICENSE and official product site state AGPLv3; root package.json declares GPL-3.0.

GitHub uses legacy AGPL-3.0. The root package metadata conflict is recorded; no only-versus-or-later variant or uniform resolution is asserted.

- Preserve LICENSE, notices and upstream history, and meet applicable AGPL source and remote-network source-offer obligations for covered modifications.

- Do not silently replace the root AGPL license with the GPL string from package metadata; resolve the discrepancy before broader redistribution/licensing integration.

- Frappe, ERPNext and optional integrations remain separate upstream projects with their own licenses and services.

- Default develop branch is not the stable deployment branch.
- Root LICENSE is AGPLv3 while package.json says GPL-3.0; this discrepancy is unresolved and explicitly retained.

## Possible extension — not implemented

A synthetic lead-import dry-run that previews duplicate candidates and required-field failures without creating leads until an operator confirms.

This is a proposed next exercise only. No implementation, test result, user outcome or commercial permission is claimed.

## Verification actually performed

Read-only review of the official repository metadata, default-branch HEAD, pinned README/license/configuration files and linked primary documentation. No packages were installed, application commands executed, tests run, database initialized, account credentials created or deployment performed. The repository's presence and this note are not runtime verification.

## Primary sources

- [Official project site](https://frappe.io/crm)
- [README.md](https://github.com/frappe/crm/blob/986fea3e525a42ecab034b4e16ef784041552f78/README.md)
- [LICENSE](https://github.com/frappe/crm/blob/986fea3e525a42ecab034b4e16ef784041552f78/LICENSE)
- [pyproject.toml](https://github.com/frappe/crm/blob/986fea3e525a42ecab034b4e16ef784041552f78/pyproject.toml)
- [package.json](https://github.com/frappe/crm/blob/986fea3e525a42ecab034b4e16ef784041552f78/package.json)
- [docker/docker-compose.yml](https://github.com/frappe/crm/blob/986fea3e525a42ecab034b4e16ef784041552f78/docker/docker-compose.yml)
- [Official documentation](https://docs.frappe.io/framework/user/en/api/rest)

