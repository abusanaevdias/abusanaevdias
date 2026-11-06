# Engineering study notes: Open Notebook

> Study annotation for [lfnovo/open-notebook](https://github.com/lfnovo/open-notebook), maintained in the profile library. The application and historical commits belong to the upstream authors.

Reviewed on 2026-11-07. Catalog item 3; exact upstream URL supplied in the user's project guide, page 8.

Upstream: [lfnovo/open-notebook](https://github.com/lfnovo/open-notebook). Default branch at review: `main`.
Reviewed commit: [`5e285b7a2e435895c4ee99ad7e4b8d2af64c3239`](https://github.com/lfnovo/open-notebook/commit/5e285b7a2e435895c4ee99ad7e4b8d2af64c3239).

This is an attributed study-fork note. Upstream authors created the application and its historical commits. Our addition is this bounded analysis and proposed extension, not upstream authorship, maintainership, a completed implementation, deployment, client result or competition submission. Preserve the original README, licenses and history unchanged.

## Specific use case

Study a small permitted research notebook in which answers can be checked against its uploaded sources.

## What the inspected documentation shows

The README describes separate SurrealDB and application services and asks for language and embedding models explicitly. The encryption key protects stored provider credentials and must remain stable to read them later. A notebook UI alone does not establish that retrieval, embeddings or audio generation are configured.

## Setup and API boundaries

- Recommended setup uses Docker Desktop or Docker Engine with Compose, running SurrealDB plus the application/UI/API/background worker.
- Set and retain a unique OPEN_NOTEBOOK_ENCRYPTION_KEY, then configure at least one language model and one embedding model in the UI.
- Source installation documents Python >=3.11,<3.13, Node.js >=20.9 (22 LTS recommended), uv and Docker for SurrealDB.
- The example Compose publishes UI/API beyond loopback and has no password by default; its README gives loopback binding or OPEN_NOTEBOOK_PASSWORD options.

- Use an AI-provider API key or a local model service such as Ollama; providers without embeddings need a separate embedding provider.
- Cloud LLM, embedding, speech/transcription and podcast services may charge independently. Local operation requires downloaded models, storage and sufficient compute; self-hosted UI does not mean every provider call stays local.

## Possible extension — not implemented

Possible extension: a notebook evidence export that lists answer citations, resolved source identifiers and missing references for manual review. This proposed audit view has not been implemented or tested.

A later implementation would first check existing behavior, use permitted fixtures, and verify source links, failure handling and persistence. These are proposed checks, not test results.

## License and provenance

Root license: [`LICENSE`](https://github.com/lfnovo/open-notebook/blob/5e285b7a2e435895c4ee99ad7e4b8d2af64c3239/LICENSE), upstream identifier **MIT**; reviewed license blob `13f4e6550e06b98aa76a0af8cbb7de437de69e34`.

Preserve the upstream copyright and permission notice in copies or substantial portions; the software is provided without warranty.

Retain the MIT copyright and permission notice. Provider, model, media and uploaded-source rights are separate; the license is not a blanket data-permission grant.

## Evidence and verification status

- [Pinned upstream README](https://github.com/lfnovo/open-notebook/blob/5e285b7a2e435895c4ee99ad7e4b8d2af64c3239/README.md), blob `81db8ab78395d6ad7b613f96704741a6c3eb8f9c`.
- [docs/1-INSTALLATION/from-source.md](https://github.com/lfnovo/open-notebook/blob/5e285b7a2e435895c4ee99ad7e4b8d2af64c3239/docs/1-INSTALLATION/from-source.md)
- [Project or identity evidence](https://www.open-notebook.ai/).
- GitHub connector read-only repository metadata, commit and file reads established this snapshot. Branch heads and setup instructions can change after review.
- No packages were installed; the app, upstream test suite, model calls, deployment and proposed extension were not run. Repository appearance and documentation are not runtime verification or a security certification.

