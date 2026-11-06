# Engineering study notes: Presenton

> Study annotation for [presenton/presenton](https://github.com/presenton/presenton), maintained in the profile library. The application and historical commits belong to the upstream authors.

Reviewed on 2026-11-07. Catalog item 4; exact upstream URL supplied in the user's project guide, page 9.

Upstream: [presenton/presenton](https://github.com/presenton/presenton). Default branch at review: `main`.
Reviewed commit: [`9af2b47dda31060d3d5070e020a0825b15c94b32`](https://github.com/presenton/presenton/commit/9af2b47dda31060d3d5070e020a0825b15c94b32).

This is an attributed study-fork note. Upstream authors created the application and its historical commits. Our addition is this bounded analysis and proposed extension, not upstream authorship, maintainership, a completed implementation, deployment, client result or competition submission. Preserve the original README, licenses and history unchanged.

## Specific use case

Study a draft-to-editable-slide workflow for a short, permitted educational presentation, checking content and exported layout manually.

## What the inspected documentation shows

The repository documents a shared FastAPI backend and Next.js interface, with Electron packaging as another shell around that application. It also distinguishes local provider configuration from the cloud-backed Community gallery, so a desktop window is not evidence of an air-gapped deployment.

## Setup and API boundaries

- Docker is a documented full-app route with persistent app_data and a browser UI on the selected host port.
- Electron/source setup documents Node.js LTS, npm, Python 3.11 and uv for the shared FastAPI backend, plus the Next.js frontend.
- Configure the chosen text/image providers in settings or documented environment variables.
- The Community gallery uses a remote service by default; air-gapped configurations must explicitly disable PRESENTON_COMMUNITY_ENABLED.

- Cloud model and image providers require the corresponding accounts/keys and can incur usage charges; local Ollama or compatible endpoints are alternatives for supported capabilities.
- A ChatGPT sign-in route is documented, but account eligibility, limits and service terms are separate from this source license. No authentication or model call was attempted.
- Templates, stock images, fonts, hosted APIs and optional enterprise offerings can have separate terms and costs.

## Possible extension — not implemented

Possible extension: a source-review checklist attached to a generated deck, tracking each factual claim, reference and reviewer decision before export. This is only a proposed extension.

A later implementation would first check existing behavior, use permitted fixtures, and verify source links, failure handling and persistence. These are proposed checks, not test results.

## License and provenance

Root license: [`LICENSE`](https://github.com/presenton/presenton/blob/9af2b47dda31060d3d5070e020a0825b15c94b32/LICENSE), upstream identifier **Apache-2.0**; reviewed license blob `5566576249c0c99a84455b2fc8454e03a9b18e20`.

Preserve the Apache 2.0 license and attribution notices, mark modified files and retain applicable NOTICE material; patent, trademark and warranty limits remain in force.

Retain Apache license/attributions, include applicable NOTICE material, and mark modifications. The reviewed repository contains an empty root NOTICE file, which should remain untouched. The source license does not grant third-party image/font rights or hosted-service access.

## Evidence and verification status

- [Pinned upstream README](https://github.com/presenton/presenton/blob/9af2b47dda31060d3d5070e020a0825b15c94b32/README.md), blob `87f14e593a430dbde67a4999b3c70742e9b13917`.
- [NOTICE](https://github.com/presenton/presenton/blob/9af2b47dda31060d3d5070e020a0825b15c94b32/NOTICE)
- [Project or identity evidence](https://presenton.ai/about).
- GitHub connector read-only repository metadata, commit and file reads established this snapshot. Branch heads and setup instructions can change after review.
- No packages were installed; the app, upstream test suite, model calls, deployment and proposed extension were not run. Repository appearance and documentation are not runtime verification or a security certification.

