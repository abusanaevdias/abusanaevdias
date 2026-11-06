# Engineering study notes: DeepTutor

> Study annotation for [HKUDS/DeepTutor](https://github.com/HKUDS/DeepTutor), maintained in the profile library. The application and historical commits belong to the upstream authors.

Reviewed on 2026-11-07. Catalog item 2; exact upstream URL supplied in the user's project guide, page 7.

Upstream: [HKUDS/DeepTutor](https://github.com/HKUDS/DeepTutor). Default branch at review: `main`.
Reviewed commit: [`60fb3bdfddb30b7740c7ce3bd9b28d908f2af6db`](https://github.com/HKUDS/DeepTutor/commit/60fb3bdfddb30b7740c7ce3bd9b28d908f2af6db).

This is an attributed study-fork note. Upstream authors created the application and its historical commits. Our addition is this bounded analysis and proposed extension, not upstream authorship, maintainership, a completed implementation, deployment, client result or competition submission. Preserve the original README, licenses and history unchanged.

## Specific use case

Study a permitted document-based tutoring flow with inspectable citations and a bounded practice task.

## What the inspected documentation shows

The current README distinguishes the core wheel from the full Web/CLI distribution and separates provider configuration from language-model selection. A source contributor setup is described on dev, even though the repository default branch is main. Notes about installation must keep those channels distinct.

## Setup and API boundaries

- Full PyPI app: Python 3.11–3.14 and Node.js >=20.9; install the full feature distribution rather than assuming the bare core wheel includes the Web app.
- Source contributor instructions use the dev branch with Python 3.11–3.14 and Node.js 22 LTS; the default branch reviewed here is main.
- Docker is an alternative full-app route; provider/model settings and runtime data persist in the selected runtime home or volume.

- Configure a language-model provider and model; retrieval, embeddings, search, speech and media capabilities can require additional providers or optional dependencies.
- Cloud providers can charge for model and service usage; a free source license does not supply an API balance, credential, storage or compute. No provider call was made.

## Possible extension — not implemented

Possible extension: a small source-grounding evaluation fixture that compares a fixed set of tutor answers and cited passages across configured models. No evaluator or comparison has been implemented or run here.

A later implementation would first check existing behavior, use permitted fixtures, and verify source links, failure handling and persistence. These are proposed checks, not test results.

## License and provenance

Root license: [`LICENSE`](https://github.com/HKUDS/DeepTutor/blob/60fb3bdfddb30b7740c7ce3bd9b28d908f2af6db/LICENSE), upstream identifier **Apache-2.0**; reviewed license blob `ae1dbfc5e74c6c9ebb3e46ea9ea8dde8a4a04ed8`.

Preserve the Apache 2.0 license and attribution notices, mark modified files and retain applicable NOTICE material; patent, trademark and warranty limits remain in force.

Retain Apache license and attribution notices, mark modified files, and preserve any applicable NOTICE material. Patent and trademark terms remain those of the upstream license; models and optional services have their own terms.

## Evidence and verification status

- [Pinned upstream README](https://github.com/HKUDS/DeepTutor/blob/60fb3bdfddb30b7740c7ce3bd9b28d908f2af6db/README.md), blob `8808e1dbfdc7a311e580a97cfbc5265c7369eb1c`.
- [Project or identity evidence](https://deeptutor.info/).
- GitHub connector read-only repository metadata, commit and file reads established this snapshot. Branch heads and setup instructions can change after review.
- No packages were installed; the app, upstream test suite, model calls, deployment and proposed extension were not run. Repository appearance and documentation are not runtime verification or a security certification.

