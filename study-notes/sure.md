# 15 — Sure: engineering study notes

> Study annotation for [we-promise/sure](https://github.com/we-promise/sure), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study/library fork of [we-promise/sure](https://github.com/we-promise/sure). The application, existing commits and upstream documentation remain the work of their original authors and contributors. The local contribution prepared for this library is this engineering note; it is not a claim to have built, deployed or operated the upstream product. Preserve the upstream README and every license file unchanged.

This is also based on the earlier Maybe Finance project. This study/library fork is not affiliated with or endorsed by Maybe Finance Inc. The upstream code and Maybe/Sure history are retained for attribution; no ownership of the Maybe name or logo is claimed.

Review date: 2026-11-07 (Asia/Almaty). Snapshot time: 2026-11-06T21:21:43Z. Default branch: `main`. Exact reviewed commit: [`c032bf4d1b503e6d9178717f8f6decf7203391d0`](https://github.com/we-promise/sure/commit/c032bf4d1b503e6d9178717f8f6decf7203391d0). Later upstream changes are outside this snapshot.

## Purpose and a specific study use case

Community-maintained personal finance application descended from Maybe Finance, with manual accounts, transactions, budgets and optional data-provider/AI integrations.

A bounded study use case is to inspect the existing data flow and API boundaries with synthetic fixtures before deciding whether to attempt the extension below. This note does not establish feature correctness, production readiness or an implemented integration.

## Setup and API dependencies

- Docker and Compose are the recommended self-hosting route; pinned compose uses Sure web + worker, PostgreSQL 16 and Redis.
- Source development pins Ruby 3.4.9; README documents PostgreSQL >9.3 and Redis >5.4, while the actual Compose stack is the more concrete reviewed configuration.
- Configure SECRET_KEY_BASE, database/Redis connection, persistent volumes and relevant hostname/SMTP settings; upstream setup scripts perform installation and database setup.

- Manual finance workflows do not require an LLM API key. Optional bank/data providers and OpenAI-compatible/Anthropic integrations require their own credentials and may incur provider charges.
- The environment example includes MCP_API_TOKEN plus an existing MCP_USER_EMAIL for the optional MCP endpoint; its external access is not enabled or tested here.
- Yahoo Finance is a default optional market-data provider in the sample environment, so lack of a paid key does not imply no outbound network activity.

No service was purchased or invoked. Self-hosting infrastructure, SMTP, bank/data providers and optional LLM usage have their own costs and terms; no free-provider availability or bank coverage is promised.

## License boundary

Primary license: [LICENSE](https://github.com/we-promise/sure/blob/c032bf4d1b503e6d9178717f8f6decf7203391d0/LICENSE). Declared identifier: `AGPL-3.0`. GNU Affero General Public License version 3

GitHub reports the legacy AGPL-3.0 identifier. No project-specific only-versus-or-later grant is asserted here.

- Preserve the AGPL license, copyright notices, attribution and upstream history.

- For covered modifications, satisfy AGPL source-distribution and remote-network source-offer requirements as applicable.

- Upstream identifies Maybe as a trademark, requests non-affiliation attribution, and does not grant use of the Maybe name/logo as a fork brand.

- Sure is itself a community fork of the archived Maybe Finance codebase, not an original product authored by the study-fork owner.

## Possible extension — not implemented

A synthetic CSV import dry-run that highlights possible duplicate transactions before a user confirms import.

This is a proposed next exercise only. No implementation, test result, user outcome or commercial permission is claimed.

## Verification actually performed

Read-only review of the official repository metadata, default-branch HEAD, pinned README/license/configuration files and linked primary documentation. No packages were installed, application commands executed, tests run, database initialized, account credentials created or deployment performed. The repository's presence and this note are not runtime verification.

## Primary sources

- [Official project site](https://sure.am/)
- [README.md](https://github.com/we-promise/sure/blob/c032bf4d1b503e6d9178717f8f6decf7203391d0/README.md)
- [LICENSE](https://github.com/we-promise/sure/blob/c032bf4d1b503e6d9178717f8f6decf7203391d0/LICENSE)
- [.ruby-version](https://github.com/we-promise/sure/blob/c032bf4d1b503e6d9178717f8f6decf7203391d0/.ruby-version)
- [compose.example.yml](https://github.com/we-promise/sure/blob/c032bf4d1b503e6d9178717f8f6decf7203391d0/compose.example.yml)
- [.env.example](https://github.com/we-promise/sure/blob/c032bf4d1b503e6d9178717f8f6decf7203391d0/.env.example)
- [docs/hosting/docker.md](https://github.com/we-promise/sure/blob/c032bf4d1b503e6d9178717f8f6decf7203391d0/docs/hosting/docker.md)


