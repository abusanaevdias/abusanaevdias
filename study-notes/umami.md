# 18 — Umami: engineering study notes

> Study annotation for [umami-software/umami](https://github.com/umami-software/umami), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study/library fork of [umami-software/umami](https://github.com/umami-software/umami). The application, existing commits and upstream documentation remain the work of their original authors and contributors. The local contribution prepared for this library is this engineering note; it is not a claim to have built, deployed or operated the upstream product. Preserve the upstream README and every license file unchanged.

Review date: 2026-11-07 (Asia/Almaty). Snapshot time: 2026-11-06T21:21:43Z. Default branch: `master`. Exact reviewed commit: [`559e3c607c23d2c72d9bd4f6481bda428255323c`](https://github.com/umami-software/umami/commit/559e3c607c23d2c72d9bd4f6481bda428255323c). Later upstream changes are outside this snapshot.

## Purpose and a specific study use case

Self-hosted web/product analytics with event collection, reports and authenticated JSON APIs.

A bounded study use case is to inspect the existing data flow and API boundaries with synthetic fixtures before deciding whether to attempt the extension below. This note does not establish feature correctness, production readiness or an implemented integration.

## Setup and API dependencies

- README documents Node 18.18+ and PostgreSQL 12.14+, but the pinned Dockerfile selects Node 22.23.4-alpine and pnpm 12.3.4; the package also pins pnpm 12.3.4.
- The reviewed Compose example runs the app with PostgreSQL 15; configure DATABASE_URL, APP_SECRET and persistence.
- Source setup uses pnpm install/build/start; build/database preparation can create tables and the initial admin account. None was executed here.

- Self-hosted API is under the instance's /api and requires authentication; Umami Cloud uses its own endpoint/API key.
- MCP is disabled by default in the README; enabling it requires MCP_ENABLED=1 and an API key generated in the instance.
- TWO_FACTOR_ENCRYPTION_KEY is needed to enable 2FA. Event collection requires deliberate tracker integration with a website; no tracker was installed.

No paid analytics account or API call is required merely to inspect this fork. Self-hosting infrastructure and optional managed/cloud services have separate costs.

## License boundary

Primary license: [LICENSE](https://github.com/umami-software/umami/blob/559e3c607c23d2c72d9bd4f6481bda428255323c/LICENSE). Declared identifier: `MIT`. MIT License

- Retain the copyright and permission notice in copies or substantial portions.

- Preserve third-party dependency licenses. The MIT source license does not grant third-party branding rights or prove a deployed tracking configuration is legally compliant.

- README minimum Node version is not the same as the current pinned container toolchain; no runtime compatibility was tested.
- Website privacy/compliance claims are upstream marketing, not a conclusion about a future fork deployment.

## Possible extension — not implemented

A deterministic event-name/schema checker with synthetic requests that compares received events against an explicit local tracking plan.

This is a proposed next exercise only. No implementation, test result, user outcome or commercial permission is claimed.

## Verification actually performed

Read-only review of the official repository metadata, default-branch HEAD, pinned README/license/configuration files and linked primary documentation. No packages were installed, application commands executed, tests run, database initialized, account credentials created or deployment performed. The repository's presence and this note are not runtime verification.

## Primary sources

- [Official project site](https://umami.is/)
- [README.md](https://github.com/umami-software/umami/blob/559e3c607c23d2c72d9bd4f6481bda428255323c/README.md)
- [LICENSE](https://github.com/umami-software/umami/blob/559e3c607c23d2c72d9bd4f6481bda428255323c/LICENSE)
- [package.json](https://github.com/umami-software/umami/blob/559e3c607c23d2c72d9bd4f6481bda428255323c/package.json)
- [Dockerfile](https://github.com/umami-software/umami/blob/559e3c607c23d2c72d9bd4f6481bda428255323c/Dockerfile)
- [docker-compose.yml](https://github.com/umami-software/umami/blob/559e3c607c23d2c72d9bd4f6481bda428255323c/docker-compose.yml)
- [Official documentation](https://docs.umami.is/docs/api)

