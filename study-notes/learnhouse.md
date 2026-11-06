# Engineering study notes: LearnHouse

> Study annotation for [learnhouse/learnhouse](https://github.com/learnhouse/learnhouse), maintained in the profile library. The application and historical commits belong to the upstream authors.

Reviewed on 2026-11-07. Catalog item 7; exact upstream URL supplied in the user's project guide, page 12.

Upstream: [learnhouse/learnhouse](https://github.com/learnhouse/learnhouse). Default branch at review: `dev`.
Reviewed commit: [`f6eb3ae9dd92535da4528a3758c780378698aec4`](https://github.com/learnhouse/learnhouse/commit/f6eb3ae9dd92535da4528a3758c780378698aec4).

This is an attributed study-fork note. Upstream authors created the application and its historical commits. Our addition is this bounded analysis and proposed extension, not upstream authorship, maintainership, a completed implementation, deployment, client result or competition submission. Preserve the original README, licenses and history unchanged.

## Specific use case

Study a permitted course-authoring and assignment workflow in the community scope, keeping commercial feature entitlements separate.

## What the inspected documentation shows

The README separates Web, API, collaboration and CLI applications. Course content, live editing and infrastructure management therefore cross different service boundaries. Its default dev branch and precisely pinned native Python version matter when preparing reproducible setup notes.

## Setup and API boundaries

- The repository default branch is dev. The official CLI documents Node.js >=22 and Docker with Compose v2 for self-hosting.
- Setup manages PostgreSQL, Redis, an admin account and optional features; source development runs the API, Web and Collab services.
- The pinned native API pyproject.toml requires Python >=3.14.7,<3.14.8; do not reuse a generic Python 3.11 setup assumption.
- Email, S3, AI, OAuth and enterprise components require their corresponding configuration; a fork alone configures none of them.

- The community source license does not supply server resources, domains, email delivery, object storage or model API usage.
- Optional AI services can bill for model usage. Payments, SSO and multi-organization features are labelled Enterprise and may require separate licensing.
- No enterprise license was accepted, license key entered, payment provider connected or service deployed.

## Possible extension — not implemented

Possible extension: an assignment evidence export containing rubric decisions and source references for teacher review. It remains a proposal; no grading or learner-outcome claim is made.

A later implementation would first check existing behavior, use permitted fixtures, and verify source links, failure handling and persistence. These are proposed checks, not test results.

## License and provenance

Root license: [`LICENSE`](https://github.com/learnhouse/learnhouse/blob/f6eb3ae9dd92535da4528a3758c780378698aec4/LICENSE), upstream identifier **AGPL-3.0**; reviewed license blob `0ad25db4bd1d86c452db3f9602ccdbe172438f52`.

Preserve the GNU AGPL v3 license and notices and meet applicable corresponding-source obligations, including modified network use; enterprise terms remain separate.

Upstream labels the community code AGPL-3.0 and carries the GNU AGPL v3 text. Keep notices and license; covered distribution and modified network use carry corresponding-source duties. No -only versus -or-later election was established beyond that upstream label. Enterprise features are separately licensed; the community license does not grant their commercial entitlement. docs/LICENSE is a separate MIT document license.

## Evidence and verification status

- [Pinned upstream README](https://github.com/learnhouse/learnhouse/blob/f6eb3ae9dd92535da4528a3758c780378698aec4/README.md), blob `32103b179de72619d6660a8d4fade984097b6407`.
- [apps/cli/README.md](https://github.com/learnhouse/learnhouse/blob/f6eb3ae9dd92535da4528a3758c780378698aec4/apps/cli/README.md)
- [apps/api/pyproject.toml](https://github.com/learnhouse/learnhouse/blob/f6eb3ae9dd92535da4528a3758c780378698aec4/apps/api/pyproject.toml)
- [docs/LICENSE](https://github.com/learnhouse/learnhouse/blob/f6eb3ae9dd92535da4528a3758c780378698aec4/docs/LICENSE)
- [Project or identity evidence](https://learnhouse.app/).
- GitHub connector read-only repository metadata, commit and file reads established this snapshot. Branch heads and setup instructions can change after review.
- No packages were installed; the app, upstream test suite, model calls, deployment and proposed extension were not run. Repository appearance and documentation are not runtime verification or a security certification.

