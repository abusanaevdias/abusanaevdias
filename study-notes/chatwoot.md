# 20 — Chatwoot: engineering study notes

> Study annotation for [chatwoot/chatwoot](https://github.com/chatwoot/chatwoot), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study/library fork of [chatwoot/chatwoot](https://github.com/chatwoot/chatwoot). The application, existing commits and upstream documentation remain the work of their original authors and contributors. The local contribution prepared for this library is this engineering note; it is not a claim to have built, deployed or operated the upstream product. Preserve the upstream README and every license file unchanged.

Review date: 2026-11-07 (Asia/Almaty). Snapshot time: 2026-11-06T21:21:43Z. Default branch: `develop`. Exact reviewed commit: [`515f9e09b7a2160d99454b6852154509c1a2cf1a`](https://github.com/chatwoot/chatwoot/commit/515f9e09b7a2160d99454b6852154509c1a2cf1a). Later upstream changes are outside this snapshot.

## Purpose and a specific study use case

Customer-support platform with shared conversation inboxes, website chat, help-center features and optional channel/AI integrations.

A bounded study use case is to inspect the existing data flow and API boundaries with synthetic fixtures before deciding whether to attempt the extension below. This note does not establish feature correctness, production readiness or an implemented integration.

## Setup and API dependencies

- Default branch develop is the development base; README recommends master or release tags for stable use.
- Reviewed source pins Ruby 3.4.4, Node 24.x and pnpm 10.x (packageManager pnpm 10.2.0).
- Local Compose includes Rails, Sidekiq, Vite, pgvector/PostgreSQL 16, Redis and MailHog. Production Docker docs require configured secrets/URLs/services and explicit database preparation/migration.

- Use appropriately scoped Chatwoot API credentials and account/inbox permissions for protected endpoints; public widget APIs have a different scope.
- SMTP/inbound email and social/messaging providers need their own configuration; optional Captain AI keys are configured in Super Admin settings in this revision, not by assuming a universal .env key.
- No channel, contact, conversation, automatic reply or external provider was configured or invoked.

No Chatwoot Cloud/Enterprise plan, messaging provider, API key or AI usage was purchased or invoked. Hosting, storage, email, selected channels and enterprise/AI services are separate cost/entitlement boundaries.

## License boundary

Primary license: [LICENSE](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/LICENSE). Declared identifier: `NOASSERTION`. MIT Expat for code outside exceptions; custom Enterprise license for enterprise/.

- Preserve MIT copyright/permission notices, the enterprise license and third-party notices.

- The enterprise directory is excluded from the root MIT grant; do not describe the whole repository as MIT.

- Enterprise production use requires valid subscription/terms for the correct seats. Development/testing copying/modification is allowed by its text, while other distribution/exploitation rights are restricted.

- Do not infer that a public study fork authorizes enterprise production, unrestricted redistribution or white-label resale.

- Root/package metadata MIT labels do not cover enterprise/.
- Develop HEAD is not a verified stable deployment.

## Possible extension — not implemented

A fixture-based incoming-webhook deduplication diagnostic that verifies one synthetic event creates one local processing result, with no automatic external replies.

This is a proposed next exercise only. No implementation, test result, user outcome or commercial permission is claimed.

## Verification actually performed

Read-only review of the official repository metadata, default-branch HEAD, pinned README/license/configuration files and linked primary documentation. No packages were installed, application commands executed, tests run, database initialized, account credentials created or deployment performed. The repository's presence and this note are not runtime verification.

## Primary sources

- [Official project site](https://www.chatwoot.com/)
- [README.md](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/README.md)
- [LICENSE](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/LICENSE)
- [enterprise/LICENSE](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/enterprise/LICENSE)
- [.ruby-version](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/.ruby-version)
- [package.json](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/package.json)
- [docker-compose.yaml](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/docker-compose.yaml)
- [.env.example](https://github.com/chatwoot/chatwoot/blob/515f9e09b7a2160d99454b6852154509c1a2cf1a/.env.example)
- [Official documentation](https://developers.chatwoot.com/self-hosted/deployment/docker)

