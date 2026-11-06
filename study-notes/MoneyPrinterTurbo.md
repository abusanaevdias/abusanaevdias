# MoneyPrinterTurbo — engineering study notes

> Study annotation for [harry0703/MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study-library entry for [harry0703/MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo). The upstream project and its contributors retain their authorship. The work prepared in this review is this note only; it does not establish that the application was installed, tested, deployed or improved. Keep the upstream README, license files and history intact.

## Provenance reviewed

- Catalog position: 9; exact link supplied in the user's source guide, page 14.
- Canonical repository: [harry0703/MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo).
- Default branch: `main`.
- Reviewed HEAD commit: [`842525d033b8f43e49d2ea8b0cff93f639d379b4`](https://github.com/harry0703/MoneyPrinterTurbo/commit/842525d033b8f43e49d2ea8b0cff93f639d379b4).
- Documentation review date: 2026-11-07. These observations are pinned to that commit; later upstream changes require a fresh review.

## Specific study use case

Study a media pipeline with explicit generation stages and editable configuration, using only assets the operator may use.

Python WebUI/API pipeline that combines script, footage, speech, subtitles and music into short videos.

## Setup and service requirements

- Python>=3.11; pyproject.toml and uv.lock define the source environment.
- Source route: uv sync --frozen, then sh webui.sh on macOS/Linux; README also documents the official mpt package and Docker release compose.
- FFmpeg is required for media rendering; it may be downloaded automatically, or configured explicitly. GPU is optional; local transcription/rendering needs compute and storage.

The following commands are documented upstream and were **not executed** in this review:

```sh
uv sync --frozen
sh webui.sh
docker compose -f docker-compose.release.yml up
```

- Online LLM, footage, video-generation and paid speech providers need their respective credentials.
- Local Ollama, user-provided clips and key-free Edge TTS are documented options; these do not establish an entirely offline pipeline.
- External generation services may charge; footage/music/voice rights are not granted by the code license. No paid services were activated.

## One possible extension — not implemented

Add a per-output asset provenance manifest recording source URLs, operator-supplied rights notes and rendering settings.

This is an idea for a future bounded change, not a completed feature, contribution, runtime result or user outcome.

## Verification status

Only read-only repository metadata, current documentation and license text were reviewed. No dependency installation, package execution, application build, automated tests, browser checks, provider requests or deployment was performed. Test result: **not run**. The upstream README, screenshots and CI claims are not our verification results.

## License boundary

Reviewed file: [LICENSE](https://github.com/harry0703/MoneyPrinterTurbo/blob/842525d033b8f43e49d2ea8b0cff93f639d379b4/LICENSE). SPDX: **MIT**.

Keep the upstream copyright and permission notice with copies or substantial portions. Preserve the license and warranty disclaimer. Dependencies, assets, model weights, provider terms and trademarks can have separate conditions. The README itself flags possible copyright issues in included default music; do not treat bundled music or third-party footage as cleared for commercial reuse.

Adding these notes does not relicense upstream code or third-party content. This entry does not claim affiliation, original authorship, production readiness or an official competition submission.

## Primary evidence

- [Canonical upstream](https://github.com/harry0703/MoneyPrinterTurbo)
- [Reviewed commit](https://github.com/harry0703/MoneyPrinterTurbo/commit/842525d033b8f43e49d2ea8b0cff93f639d379b4)
- [README-en.md](https://github.com/harry0703/MoneyPrinterTurbo/blob/842525d033b8f43e49d2ea8b0cff93f639d379b4/README-en.md)
- [LICENSE](https://github.com/harry0703/MoneyPrinterTurbo/blob/842525d033b8f43e49d2ea8b0cff93f639d379b4/LICENSE)
- [pyproject.toml](https://github.com/harry0703/MoneyPrinterTurbo/blob/842525d033b8f43e49d2ea8b0cff93f639d379b4/pyproject.toml)

