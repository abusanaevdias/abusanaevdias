# Open Lovable — engineering study notes

> Study annotation for [firecrawl/open-lovable](https://github.com/firecrawl/open-lovable), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study-library entry for [firecrawl/open-lovable](https://github.com/firecrawl/open-lovable). The upstream project and its contributors retain their authorship. The work prepared in this review is this note only; it does not establish that the application was installed, tested, deployed or improved. Keep the upstream README, license files and history intact.

## Provenance reviewed

- Catalog position: 10; exact link supplied in the user's source guide, page 15.
- Canonical repository: [firecrawl/open-lovable](https://github.com/firecrawl/open-lovable).
- Default branch: `main`.
- Reviewed HEAD commit: [`806b8072f28afea11fa2b028cac1449eff74c511`](https://github.com/firecrawl/open-lovable/commit/806b8072f28afea11fa2b028cac1449eff74c511).
- Documentation review date: 2026-11-07. These observations are pinned to that commit; later upstream changes require a fresh review.

## Specific study use case

Study the handoff between web extraction, model-driven code edits and a remote execution sandbox.

Firecrawl team's example application for conversing with a model to generate and edit React applications.

## Setup and service requirements

- Node.js-compatible Next.js environment and pnpm, npm or Yarn; reviewed package.json does not pin a Node engine.
- Install dependencies, create .env.local and run the documented development command; UI is documented at localhost:3000.
- Choose Vercel Sandbox (default) or E2B; this is not a dependency-free or purely local execution path.

The following commands are documented upstream and were **not executed** in this review:

```sh
pnpm install
pnpm dev
```

- FIRECRAWL_API_KEY is required by the README; configure a selected model provider such as Gemini, Anthropic, OpenAI or Groq.
- Vercel Sandbox requires Vercel OIDC or token/team/project configuration; E2B alternative requires E2B_API_KEY.
- MORPH_API_KEY is optional for faster edits. Crawl/model/sandbox/hosting usage may incur charges; no accounts were linked.

## One possible extension — not implemented

Add a human-review checkpoint that lists changed files and source attribution before applying a generated patch.

This is an idea for a future bounded change, not a completed feature, contribution, runtime result or user outcome.

## Verification status

Only read-only repository metadata, current documentation and license text were reviewed. No dependency installation, package execution, application build, automated tests, browser checks, provider requests or deployment was performed. Test result: **not run**. The upstream README, screenshots and CI claims are not our verification results.

## License boundary

Reviewed file: [LICENSE](https://github.com/firecrawl/open-lovable/blob/806b8072f28afea11fa2b028cac1449eff74c511/LICENSE). SPDX: **MIT**.

Keep the upstream copyright and permission notice with copies or substantial portions. Preserve the license and warranty disclaimer. Dependencies, assets, model weights, provider terms and trademarks can have separate conditions. MIT covers this example's code; it does not transfer rights to websites supplied for extraction or to the Lovable/Firecrawl marks.

Adding these notes does not relicense upstream code or third-party content. This entry does not claim affiliation, original authorship, production readiness or an official competition submission.

## Primary evidence

- [Canonical upstream](https://github.com/firecrawl/open-lovable)
- [Reviewed commit](https://github.com/firecrawl/open-lovable/commit/806b8072f28afea11fa2b028cac1449eff74c511)
- [README.md](https://github.com/firecrawl/open-lovable/blob/806b8072f28afea11fa2b028cac1449eff74c511/README.md)
- [LICENSE](https://github.com/firecrawl/open-lovable/blob/806b8072f28afea11fa2b028cac1449eff74c511/LICENSE)
- [package.json](https://github.com/firecrawl/open-lovable/blob/806b8072f28afea11fa2b028cac1449eff74c511/package.json)

