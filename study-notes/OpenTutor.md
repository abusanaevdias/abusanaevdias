# Engineering study notes: OpenTutor

> Study annotation for [zijinz456/OpenTutor](https://github.com/zijinz456/OpenTutor), maintained in the profile library. The application and historical commits belong to the upstream authors.

Reviewed on 2026-11-07. Catalog item 6; exact upstream URL supplied in the user's project guide, page 11.

Upstream: [zijinz456/OpenTutor](https://github.com/zijinz456/OpenTutor). Default branch at review: `main`.
Reviewed commit: [`153bac7d419b801d94fa3aef57d0f4e43fe286a5`](https://github.com/zijinz456/OpenTutor/commit/153bac7d419b801d94fa3aef57d0f4e43fe286a5).

This is an attributed study-fork note. Upstream authors created the application and its historical commits. Our addition is this bounded analysis and proposed extension, not upstream authorship, maintainership, a completed implementation, deployment, client result or competition submission. Preserve the original README, licenses and history unchanged.

## Specific use case

Study how a learner can upload permitted course material, inspect cited explanations and complete one quiz/review task while retaining local progress.

## What the inspected documentation shows

The README combines a FastAPI backend, an asynchronous SQLAlchemy data layer and SQLite with a separate web frontend. It explicitly scopes the current release to local single-user use, while describing local and cloud model choices separately. Local storage does not make a classroom or multi-user deployment a verified capability.

## Setup and API boundaries

- The exact user-provided PDF URL selects zijinz456/OpenTutor; similarly named projects were not substituted.
- README manual setup: Python 3.11+, Node.js 20+, backend requirements-core.txt and the apps/web frontend; Docker Compose is an alternative.
- A local model service such as Ollama is the default documented route; cloud model provider settings are optional.
- The current channel targets a local single-user beta. Authentication is disabled by default; README requires explicit AUTH_ENABLED and JWT_SECRET_KEY configuration for network-accessible use.

- Local models require model downloads and sufficient compute; optional cloud providers require keys and may charge for usage.
- macOS and Linux are first-class beta targets. Separate Windows-native source instructions require CPython 3.12 and Node.js 24; Windows support is described separately.
- Experimental knowledge-graph or autonomous flows and generated study quality were not runtime-verified.

## Possible extension — not implemented

Possible extension: a teacher-reviewed bilingual glossary workflow tied to source passages and quiz mistakes, with explicit accept/reject review. This proposal has not been implemented or evaluated.

A later implementation would first check existing behavior, use permitted fixtures, and verify source links, failure handling and persistence. These are proposed checks, not test results.

## License and provenance

Root license: [`LICENSE`](https://github.com/zijinz456/OpenTutor/blob/153bac7d419b801d94fa3aef57d0f4e43fe286a5/LICENSE), upstream identifier **MIT**; reviewed license blob `2c7493ad525b2b5ee698f8586134feebdb0293df`.

Preserve the upstream copyright and permission notice in copies or substantial portions; the software is provided without warranty.

Retain the MIT notice and upstream attribution. Uploaded course material, local model weights and provider services retain their own conditions.

## Evidence and verification status

- [Pinned upstream README](https://github.com/zijinz456/OpenTutor/blob/153bac7d419b801d94fa3aef57d0f4e43fe286a5/README.md), blob `8582d0b75877589f99cb3908a19fade605b90e51`.
- [Project or identity evidence](https://github.com/zijinz456/OpenTutor).
- GitHub connector read-only repository metadata, commit and file reads established this snapshot. Branch heads and setup instructions can change after review.
- No packages were installed; the app, upstream test suite, model calls, deployment and proposed extension were not run. Repository appearance and documentation are not runtime verification or a security certification.

