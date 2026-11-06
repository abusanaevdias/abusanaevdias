# Engineering study notes: Vane / Perplexica

> Study annotation for [ItzCrazyKns/Vane](https://github.com/ItzCrazyKns/Vane), maintained in the profile library. The application and historical commits belong to the upstream authors.

Reviewed on 2026-11-07. Catalog item 5; exact upstream URL supplied in the user's project guide, page 10.

Upstream: [ItzCrazyKns/Vane](https://github.com/ItzCrazyKns/Vane). Default branch at review: `master`.
Reviewed commit: [`348feca3e378fb4157b217724ed508dc707f853f`](https://github.com/ItzCrazyKns/Vane/commit/348feca3e378fb4157b217724ed508dc707f853f).

This is an attributed study-fork note. Upstream authors created the application and its historical commits. Our addition is this bounded analysis and proposed extension, not upstream authorship, maintainership, a completed implementation, deployment, client result or competition submission. Preserve the original README, licenses and history unchanged.

## Specific use case

Study an answer engine against a small set of permitted research questions, inspecting the retrieved citations rather than assuming answer correctness.

## What the inspected documentation shows

The installation instructions distinguish the bundled search image from a slim image that delegates retrieval to an existing SearXNG service. Model selection and retrieval availability are separate setup dependencies. The old Perplexica name should not be counted as another project.

## Setup and API boundaries

- Canonical current repository is ItzCrazyKns/Vane; the former ItzCrazyKns/Perplexica URL redirects there. This is one catalog item.
- The recommended Docker image bundles SearXNG; the slim image requires a separate SearXNG endpoint.
- Non-Docker setup requires SearXNG with JSON output and the documented search-engine configuration, plus npm install/build/start for the application.
- Configure a supported cloud provider or a reachable local model endpoint, and retain the persistent data volume.

- Local Ollama/compatible models avoid a cloud model API charge but still need hardware and model downloads; cloud providers charge under their own plans.
- SearXNG retrieves from external search engines, and a cloud model can receive query/context data. A self-hosted application is not automatically offline or fully private.
- The reviewed README lists authentication as upcoming; no public-hosting readiness or security certification is claimed.

## Possible extension — not implemented

Possible extension: a local citation-check report that records source URL reachability and whether a quoted passage is present in the retrieved text. No citation checker has been implemented or run here.

A later implementation would first check existing behavior, use permitted fixtures, and verify source links, failure handling and persistence. These are proposed checks, not test results.

## License and provenance

Root license: [`LICENSE`](https://github.com/ItzCrazyKns/Vane/blob/348feca3e378fb4157b217724ed508dc707f853f/LICENSE), upstream identifier **MIT**; reviewed license blob `f94c7b0dabce11a8f6c98749125b15a9ced41137`.

Preserve the upstream copyright and permission notice in copies or substantial portions; the software is provided without warranty.

Retain the MIT copyright and permission notice. Search-engine, model-provider and retrieved-content terms remain separate from the repository license.

## Evidence and verification status

- [Pinned upstream README](https://github.com/ItzCrazyKns/Vane/blob/348feca3e378fb4157b217724ed508dc707f853f/README.md), blob `28e62ba4ef3f22ec825ef4e320b351af7fbfd36b`.
- [package.json](https://github.com/ItzCrazyKns/Vane/blob/348feca3e378fb4157b217724ed508dc707f853f/package.json)
- [Project or identity evidence](https://github.com/ItzCrazyKns/Perplexica).
- GitHub connector read-only repository metadata, commit and file reads established this snapshot. Branch heads and setup instructions can change after review.
- No packages were installed; the app, upstream test suite, model calls, deployment and proposed extension were not run. Repository appearance and documentation are not runtime verification or a security certification.

