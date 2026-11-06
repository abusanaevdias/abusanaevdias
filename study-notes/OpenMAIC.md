# Engineering study notes: OpenMAIC

> Study annotation for [THU-MAIC/OpenMAIC](https://github.com/THU-MAIC/OpenMAIC), maintained in the profile library. The application and historical commits belong to the upstream authors.

Reviewed on 2026-11-07. Catalog item 1; exact upstream URL supplied in the user's project guide, page 6.

Upstream: [THU-MAIC/OpenMAIC](https://github.com/THU-MAIC/OpenMAIC). Default branch at review: `main`.
Reviewed commit: [`5bd8cc840ee6397d063e1fe6aba974b9f0401593`](https://github.com/THU-MAIC/OpenMAIC/commit/5bd8cc840ee6397d063e1fe6aba974b9f0401593).

This is an attributed study-fork note. Upstream authors created the application and its historical commits. Our addition is this bounded analysis and proposed extension, not upstream authorship, maintainership, a completed implementation, deployment, client result or competition submission. Preserve the original README, licenses and history unchanged.

## Specific use case

Study how a teacher could prepare an interactive lesson from permitted course materials while reviewing the generated scenes and questions.

## What the inspected documentation shows

The README separates server provider accounts from capability slots in openmaic.yml. Courses are persisted in PostgreSQL, and generation runs on a long-running server. This matters when studying a classroom workflow: a rendered lesson, a configured model and durable learner progress are separate concerns.

## Setup and API boundaries

- Source setup: Node.js >=22.19, pnpm >=10, PostgreSQL 16; local database helper uses Docker.
- Configure .env.local and openmaic.yml, including DATABASE_URL and a selected provider/model; the current long-running server requires PostgreSQL.
- Optional media, search, parsing and sandbox capabilities need their own service configuration and persistence.

- The example configuration uses an OpenAI API key; other supported providers and local Ollama/Lemonade are alternatives.
- Cloud text, image, speech, video, search and sandbox providers may bill separately; local models still require compute and downloaded assets. No cost or learning-outcome result was measured.

## Possible extension — not implemented

Possible extension: an optional lesson evidence sheet linking each generated quiz item to teacher-approved source passages and a review decision. This is a proposal, not implemented or validated here.

A later implementation would first check existing behavior, use permitted fixtures, and verify source links, failure handling and persistence. These are proposed checks, not test results.

## License and provenance

Root license: [`LICENSE`](https://github.com/THU-MAIC/OpenMAIC/blob/5bd8cc840ee6397d063e1fe6aba974b9f0401593/LICENSE), upstream identifier **MIT**; reviewed license blob `76abc5f13261e94fc0382b33ac8c101555288083`.

Preserve the upstream copyright and permission notice in copies or substantial portions; the software is provided without warranty.

The pinned source uses MIT; the README records a June 2026 relicensing. Earlier revisions and third-party models/assets can have different terms.

## Evidence and verification status

- [Pinned upstream README](https://github.com/THU-MAIC/OpenMAIC/blob/5bd8cc840ee6397d063e1fe6aba974b9f0401593/README.md), blob `528a1e4248671e26890effae6526042c35589d13`.
- [Project or identity evidence](https://open.maic.chat/).
- GitHub connector read-only repository metadata, commit and file reads established this snapshot. Branch heads and setup instructions can change after review.
- No packages were installed; the app, upstream test suite, model calls, deployment and proposed extension were not run. Repository appearance and documentation are not runtime verification or a security certification.

