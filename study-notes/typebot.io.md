# 16 — Typebot: engineering study notes

> Study annotation for [baptisteArno/typebot.io](https://github.com/baptisteArno/typebot.io), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study/library fork of [baptisteArno/typebot.io](https://github.com/baptisteArno/typebot.io). The application, existing commits and upstream documentation remain the work of their original authors and contributors. The local contribution prepared for this library is this engineering note; it is not a claim to have built, deployed or operated the upstream product. Preserve the upstream README and every license file unchanged.

Review date: 2026-11-07 (Asia/Almaty). Snapshot time: 2026-11-06T21:21:43Z. Default branch: `main`. Exact reviewed commit: [`fd1dc34e0acdeca99d204fde6e692fed1879d9f5`](https://github.com/baptisteArno/typebot.io/commit/fd1dc34e0acdeca99d204fde6e692fed1879d9f5). Later upstream changes are outside this snapshot.

## Purpose and a specific study use case

Visual builder and runtime for conversational forms/chatbots, with result collection, embeds and optional external integrations.

A bounded study use case is to inspect the existing data flow and API boundaries with synthetic fixtures before deciding whether to attempt the extension below. This note does not establish feature correctness, production readiness or an implemented integration.

## Setup and API dependencies

- Source package.json requires Node 24.x and Bun 1.3.9; .node-version pins 24.22.1.
- Docker Compose defines separate builder/viewer services, PostgreSQL 16 and Redis; local developer Compose also supplies MinIO for uploads.
- Configure encryption secret, database URL, builder/viewer URLs and authentication; local docs use localhost for builder and 127.0.0.1 for viewer to isolate cookies.

- HTTP execution and result APIs require the authentication/configuration described by the official API documentation.
- Email/OAuth, S3-compatible uploads, OpenAI and other integration blocks need their own configured services and credentials when selected.
- Basic visual flows do not imply a requirement to buy an LLM API subscription; integrations may generate provider charges.

No cloud subscription, hosting, API key or external integration was created. Infrastructure and selected email/storage/AI/payment providers are separate dependencies and costs.

## License boundary

Primary license: [LICENSE](https://github.com/baptisteArno/typebot.io/blob/fd1dc34e0acdeca99d204fde6e692fed1879d9f5/LICENSE). Declared identifier: `FSL-1.1-ALv2`. Functional Source License 1.1, Apache 2.0 Future License; upstream abbreviation FSL-1.1-Apache-2.0

FSL-1.1-ALv2 is the current SPDX identifier for this Apache-future-license variant. The source file uses a different abbreviation; this mapping is documented rather than copied from GitHub autodetection.

- Current source is fair source under the FSL, not unrestricted AGPL or already blanket Apache-2.0.

- Internal use and noncommercial education/research are among the permitted purposes; competing commercial products/services are restricted by the actual license.

- Redistribution must retain the terms/link and copyright notices. Trademark use is limited to origin/license identification.

- Each software version receives the Apache-2.0 future license on its own second anniversary; the current reviewed HEAD is not relabelled Apache-2.0.

- README still contains an AGPLv3 badge, but its license section and actual LICENSE state FSL. Use the actual license.
- typebot.io and docs.typebot.io currently redirect to the .com domains; official site links back to the same repository.

## Possible extension — not implemented

A deterministic webhook-payload preview that checks required result fields against a local schema before an operator publishes a bot.

This is a proposed next exercise only. No implementation, test result, user outcome or commercial permission is claimed.

## Verification actually performed

Read-only review of the official repository metadata, default-branch HEAD, pinned README/license/configuration files and linked primary documentation. No packages were installed, application commands executed, tests run, database initialized, account credentials created or deployment performed. The repository's presence and this note are not runtime verification.

## Primary sources

- [Official project site](https://typebot.com/)
- [README.md](https://github.com/baptisteArno/typebot.io/blob/fd1dc34e0acdeca99d204fde6e692fed1879d9f5/README.md)
- [LICENSE](https://github.com/baptisteArno/typebot.io/blob/fd1dc34e0acdeca99d204fde6e692fed1879d9f5/LICENSE)
- [package.json](https://github.com/baptisteArno/typebot.io/blob/fd1dc34e0acdeca99d204fde6e692fed1879d9f5/package.json)
- [.node-version](https://github.com/baptisteArno/typebot.io/blob/fd1dc34e0acdeca99d204fde6e692fed1879d9f5/.node-version)
- [docker-compose.yml](https://github.com/baptisteArno/typebot.io/blob/fd1dc34e0acdeca99d204fde6e692fed1879d9f5/docker-compose.yml)
- [.env.example](https://github.com/baptisteArno/typebot.io/blob/fd1dc34e0acdeca99d204fde6e692fed1879d9f5/.env.example)
- [Official documentation](https://docs.typebot.com/self-hosting/get-started)
- [Official documentation](https://docs.typebot.com/contribute/guides/local-installation)
- [SPDX identifier reference](https://spdx.org/licenses/FSL-1.1-ALv2.html)

