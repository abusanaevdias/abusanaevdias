# 17 — Formbricks: engineering study notes

> Study annotation for [formbricks/formbricks](https://github.com/formbricks/formbricks), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study/library fork of [formbricks/formbricks](https://github.com/formbricks/formbricks). The application, existing commits and upstream documentation remain the work of their original authors and contributors. The local contribution prepared for this library is this engineering note; it is not a claim to have built, deployed or operated the upstream product. Preserve the upstream README and every license file unchanged.

Review date: 2026-11-07 (Asia/Almaty). Snapshot time: 2026-11-06T21:21:43Z. Default branch: `main`. Exact reviewed commit: [`19e87ea16c4445bc3108f845c88062211ffa43fc`](https://github.com/formbricks/formbricks/commit/19e87ea16c4445bc3108f845c88062211ffa43fc). Later upstream changes are outside this snapshot.

## Purpose and a specific study use case

Survey and experience-management platform supporting link, website, in-app and email feedback, with a separately licensed enterprise area.

A bounded study use case is to inspect the existing data flow and API boundaries with synthetic fixtures before deciding whether to attempt the extension below. This note does not establish feature correctness, production readiness or an implemented integration.

## Setup and API dependencies

- Source package.json requires Node >=24.0.0 <25 and pnpm 11.7.0.
- README's local route is pnpm install, then pnpm go; these were read, not executed.
- The current local Compose stack includes PostgreSQL/pgvector, SpiceDB/Authzed, MailHog, Valkey, RustFS, Hub and Cube. Environment setup generates/configures required auth/encryption/cron and service secrets.

- Use the versioned management/client APIs and authorized environment/API credentials from current docs; a local API endpoint is not anonymous administrative access.
- SMTP supports verification/reset email; object storage is needed for relevant upload configurations.
- Hub embeddings/enrichment/translation and other AI providers are optional and require their own credentials or local models; enterprise features require the applicable license key.

No deployment, Enterprise subscription, API key or provider call was made. Hosting and enabled SMTP/storage/LLM services may cost money; EE entitlement is separate from the AGPL core.

## License boundary

Primary license: [LICENSE](https://github.com/formbricks/formbricks/blob/19e87ea16c4445bc3108f845c88062211ffa43fc/LICENSE). Declared identifier: `NOASSERTION`. Mixed: AGPLv3 core, MIT for listed SDK/client packages, custom Enterprise license for EE.

- Preserve the root and directory-specific licenses and third-party notices; do not describe the entire tree as one unrestricted AGPL or MIT work.

- AGPL-covered modifications carry the applicable copyleft and remote-network source obligations.

- EE permits development/testing copying and modification without a subscription, but production requires valid Enterprise terms/license for the correct seats and other publication/distribution rights are restricted by its text.

- The EE license does not become AGPL merely because its code is in this public repository.

- Mixed license tree with explicit EE distribution/production limitations; no uniform open-source or white-label resale claim.
- README's older self-hosting URL now redirects to documentation introduction; use the current Self Hosting navigation.

## Possible extension — not implemented

An opt-in response-export redaction preview using synthetic feedback, implemented in an appropriately licensed core extension after a separate scope review.

This is a proposed next exercise only. No implementation, test result, user outcome or commercial permission is claimed.

## Verification actually performed

Read-only review of the official repository metadata, default-branch HEAD, pinned README/license/configuration files and linked primary documentation. No packages were installed, application commands executed, tests run, database initialized, account credentials created or deployment performed. The repository's presence and this note are not runtime verification.

## Primary sources

- [Official project site](https://formbricks.com/)
- [README.md](https://github.com/formbricks/formbricks/blob/19e87ea16c4445bc3108f845c88062211ffa43fc/README.md)
- [LICENSE](https://github.com/formbricks/formbricks/blob/19e87ea16c4445bc3108f845c88062211ffa43fc/LICENSE)
- [apps/web/modules/ee/LICENSE](https://github.com/formbricks/formbricks/blob/19e87ea16c4445bc3108f845c88062211ffa43fc/apps/web/modules/ee/LICENSE)
- [package.json](https://github.com/formbricks/formbricks/blob/19e87ea16c4445bc3108f845c88062211ffa43fc/package.json)
- [.env.example](https://github.com/formbricks/formbricks/blob/19e87ea16c4445bc3108f845c88062211ffa43fc/.env.example)
- [docker-compose.dev.yml](https://github.com/formbricks/formbricks/blob/19e87ea16c4445bc3108f845c88062211ffa43fc/docker-compose.dev.yml)


