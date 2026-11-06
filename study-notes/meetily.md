# Meetily — engineering study notes

> Study annotation for [Zackriya-Solutions/meetily](https://github.com/Zackriya-Solutions/meetily), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study-library entry for [Zackriya-Solutions/meetily](https://github.com/Zackriya-Solutions/meetily). The upstream project and its contributors retain their authorship. The work prepared in this review is this note only; it does not establish that the application was installed, tested, deployed or improved. Keep the upstream README, license files and history intact.

## Provenance reviewed

- Catalog position: 11; exact link supplied in the user's source guide, page 16.
- Canonical repository: [Zackriya-Solutions/meetily](https://github.com/Zackriya-Solutions/meetily).
- Default branch: `main`.
- Reviewed HEAD commit: [`07c4dfd45361bb6776916a0d46f493dda447f471`](https://github.com/Zackriya-Solutions/meetily/commit/07c4dfd45361bb6776916a0d46f493dda447f471).
- Documentation review date: 2026-11-07. These observations are pinned to that commit; later upstream changes require a fresh review.

## Specific study use case

Study local audio-to-transcript flow and editable meeting-summary handling on permitted sample recordings.

Tauri/Rust desktop meeting-note application with local transcription and configurable summary providers.

## Setup and service requirements

- Source builds need Rust, Node.js, pnpm 9.15.9 and CMake/platform build tools; install frontend dependencies with the committed lockfile.
- macOS/Windows packaged releases exist; Linux source-build instructions are provided.
- Windows installer requires AVX2-capable x64 CPU; GPU acceleration depends on platform/toolchain. Local model downloads and local compute are still required.

The following commands are documented upstream and were **not executed** in this review:

```sh
cd frontend
pnpm install --frozen-lockfile
pnpm tauri:dev
```

- Local transcription and local Ollama summaries can avoid a paid cloud-model API; model weights/downloads and compute are separate dependencies.
- Cloud Claude/Groq/OpenRouter/OpenAI-compatible summary providers need selected credentials and may charge.
- Community MIT code is distinct from separately offered Meetily Pro features/services; no Pro access was purchased.

## One possible extension — not implemented

Add an explicit transcript-to-summary trace view with timestamps and manual correction markers.

This is an idea for a future bounded change, not a completed feature, contribution, runtime result or user outcome.

## Verification status

Only read-only repository metadata, current documentation and license text were reviewed. No dependency installation, package execution, application build, automated tests, browser checks, provider requests or deployment was performed. Test result: **not run**. The upstream README, screenshots and CI claims are not our verification results.

## License boundary

Reviewed file: [LICENSE.md](https://github.com/Zackriya-Solutions/meetily/blob/07c4dfd45361bb6776916a0d46f493dda447f471/LICENSE.md). SPDX: **MIT**.

Keep the upstream copyright and permission notice with copies or substantial portions. Preserve the license and warranty disclaimer. Dependencies, assets, model weights, provider terms and trademarks can have separate conditions. This review concerns the public Community repository, not a license to Meetily Pro or to third-party recordings/model weights.

Adding these notes does not relicense upstream code or third-party content. This entry does not claim affiliation, original authorship, production readiness or an official competition submission.

## Primary evidence

- [Canonical upstream](https://github.com/Zackriya-Solutions/meetily)
- [Reviewed commit](https://github.com/Zackriya-Solutions/meetily/commit/07c4dfd45361bb6776916a0d46f493dda447f471)
- [README.md](https://github.com/Zackriya-Solutions/meetily/blob/07c4dfd45361bb6776916a0d46f493dda447f471/README.md)
- [LICENSE.md](https://github.com/Zackriya-Solutions/meetily/blob/07c4dfd45361bb6776916a0d46f493dda447f471/LICENSE.md)
- [BUILDING.md](https://github.com/Zackriya-Solutions/meetily/blob/07c4dfd45361bb6776916a0d46f493dda447f471/docs/BUILDING.md)
- [downloads](https://meetily.ai/downloads)

