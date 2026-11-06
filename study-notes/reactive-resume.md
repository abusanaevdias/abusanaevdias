# Reactive Resume — engineering study notes

> Study annotation for [reactive-resume/reactive-resume](https://github.com/reactive-resume/reactive-resume), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study-library entry for [reactive-resume/reactive-resume](https://github.com/reactive-resume/reactive-resume). The upstream project and its contributors retain their authorship. The work prepared in this review is this note only; it does not establish that the application was installed, tested, deployed or improved. Keep the upstream README, license files and history intact.

## Provenance reviewed

- Catalog position: 13; exact link supplied in the user's source guide, page 18.
- Canonical repository: [reactive-resume/reactive-resume](https://github.com/reactive-resume/reactive-resume).
- Default branch: `main`.
- Reviewed HEAD commit: [`ced8d2500e082cceb5837d59defbf9e2ca422c1a`](https://github.com/reactive-resume/reactive-resume/commit/ced8d2500e082cceb5837d59defbf9e2ca422c1a).
- Documentation review date: 2026-11-07. These observations are pinned to that commit; later upstream changes require a fresh review.
- The guide's older AmruthPillai URL redirects to reactive-resume/reactive-resume; GitHub metadata confirms the same repository identity.

## Specific study use case

Study structured resume editing, import/export round trips and self-hosted document storage using synthetic personal data.

Resume/document editor and self-hostable career workspace with JSON import/export and PDF generation.

## Setup and service requirements

- Canonical repository moved from AmruthPillai/Reactive-Resume to reactive-resume/reactive-resume; GitHub metadata resolves the same repository ID 249995750.
- Current package.json pins Node.js 24.x and pnpm 12.16.1.
- Docker quick start builds this checkout with PostgreSQL, Redis and SeaweedFS; development docs also allow local upload storage and describe Redis as optional.
- Current v6 PDF generation uses Forme; Browserless/Chromium/external print services are not required. Configure AUTH_SECRET and a separate ENCRYPTION_SECRET for saved AI-provider/assistant use.

The following commands are documented upstream and were **not executed** in this review:

```sh
docker compose up -d --build
pnpm install --frozen-lockfile
pnpm dev
```

- Core editing/export does not require a paid AI provider; optional assistant, search, SMTP/OAuth or managed storage/hosting introduce their own credentials and costs.
- No personal resumes, account registrations or external providers were configured during this review.

## One possible extension — not implemented

Add a synthetic JSON import/export regression corpus for multilingual resume sections and PDF text preservation.

This is an idea for a future bounded change, not a completed feature, contribution, runtime result or user outcome.

## Verification status

Only read-only repository metadata, current documentation and license text were reviewed. No dependency installation, package execution, application build, automated tests, browser checks, provider requests or deployment was performed. Test result: **not run**. The upstream README, screenshots and CI claims are not our verification results.

## License boundary

Reviewed file: [LICENSE](https://github.com/reactive-resume/reactive-resume/blob/ced8d2500e082cceb5837d59defbf9e2ca422c1a/LICENSE). SPDX: **MIT**.

Keep the upstream copyright and permission notice with copies or substantial portions. Preserve the license and warranty disclaimer. Dependencies, assets, model weights, provider terms and trademarks can have separate conditions.

Adding these notes does not relicense upstream code or third-party content. This entry does not claim affiliation, original authorship, production readiness or an official competition submission.

## Primary evidence

- [Canonical upstream](https://github.com/reactive-resume/reactive-resume)
- [Reviewed commit](https://github.com/reactive-resume/reactive-resume/commit/ced8d2500e082cceb5837d59defbf9e2ca422c1a)
- [README.md](https://github.com/reactive-resume/reactive-resume/blob/ced8d2500e082cceb5837d59defbf9e2ca422c1a/README.md)
- [LICENSE](https://github.com/reactive-resume/reactive-resume/blob/ced8d2500e082cceb5837d59defbf9e2ca422c1a/LICENSE)
- [package.json](https://github.com/reactive-resume/reactive-resume/blob/ced8d2500e082cceb5837d59defbf9e2ca422c1a/package.json)
- [development](https://docs.rxresu.me/contributing/development)

