# Scira — engineering study notes

> Study annotation for [zaidmukaddam/scira](https://github.com/zaidmukaddam/scira), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study-library entry for [zaidmukaddam/scira](https://github.com/zaidmukaddam/scira). The upstream project and its contributors retain their authorship. The work prepared in this review is this note only; it does not establish that the application was installed, tested, deployed or improved. Keep the upstream README, license files and history intact.

## Provenance reviewed

- Catalog position: 8; exact link supplied in the user's source guide, page 13.
- Canonical repository: [zaidmukaddam/scira](https://github.com/zaidmukaddam/scira).
- Default branch: `main`.
- Reviewed HEAD commit: [`e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9`](https://github.com/zaidmukaddam/scira/commit/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9).
- Documentation review date: 2026-11-07. These observations are pinned to that commit; later upstream changes require a fresh review.

## Specific study use case

Study how a search application separates retrieval, model calls and cited source presentation.

Agentic web research and search interface with cited answers, built with Next.js and Vercel AI SDK.

## Setup and service requirements

- Docker and Docker Compose; reviewed Dockerfile uses Node.js 22 Alpine.
- Alternative documented local route uses Bun: copy .env.example to .env.local, install dependencies and run bun dev.
- Database/auth and optional integrations require configuration; .env.example includes DATABASE_URL, REDIS_URL, BETTER_AUTH_SECRET and OAuth settings.

The following commands are documented upstream and were **not executed** in this review:

```sh
docker compose up
bun install
bun dev
```

- README local setup lists OpenAI and Anthropic credentials plus Exa for web search.
- Additional search/media/sandbox/voice/connectors require their own selected service keys; not every optional integration is needed for every mode.
- Model, search, sandbox, database and hosting usage may incur provider charges. No price or free-quota claim was verified.

## One possible extension — not implemented

Add a source-quality inspection view that shows retrieval timestamps and lets the reader flag a citation without changing the cited source.

This is an idea for a future bounded change, not a completed feature, contribution, runtime result or user outcome.

## Verification status

Only read-only repository metadata, current documentation and license text were reviewed. No dependency installation, package execution, application build, automated tests, browser checks, provider requests or deployment was performed. Test result: **not run**. The upstream README, screenshots and CI claims are not our verification results.

## License boundary

Reviewed file: [LICENSE](https://github.com/zaidmukaddam/scira/blob/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9/LICENSE). SPDX: **AGPL-3.0-or-later**.

Preserve AGPL notices and license, mark modified versions, and satisfy corresponding-source requirements when conveying covered work. A modified network-served version must offer its corresponding source to remote users under section 13. The project-specific notice grants version 3 or later; GitHub reports the legacy SPDX label AGPL-3.0. Dependencies, provider terms and trademarks remain separate.

Adding these notes does not relicense upstream code or third-party content. This entry does not claim affiliation, original authorship, production readiness or an official competition submission.

## Primary evidence

- [Canonical upstream](https://github.com/zaidmukaddam/scira)
- [Reviewed commit](https://github.com/zaidmukaddam/scira/commit/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9)
- [README.md](https://github.com/zaidmukaddam/scira/blob/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9/README.md)
- [LICENSE](https://github.com/zaidmukaddam/scira/blob/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9/LICENSE)
- [.env.example](https://github.com/zaidmukaddam/scira/blob/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9/.env.example)
- [Dockerfile](https://github.com/zaidmukaddam/scira/blob/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9/Dockerfile)
- [package.json](https://github.com/zaidmukaddam/scira/blob/e1692f5bdec7ec3f6482a24e0c6cf9b483d810f9/package.json)

