# Actual Budget — engineering study notes

> Study annotation for [actualbudget/actual](https://github.com/actualbudget/actual), maintained in the profile library. The application and historical commits belong to the upstream authors.

This is an attributed study-library entry for [actualbudget/actual](https://github.com/actualbudget/actual). The upstream project and its contributors retain their authorship. The work prepared in this review is this note only; it does not establish that the application was installed, tested, deployed or improved. Keep the upstream README, license files and history intact.

## Provenance reviewed

- Catalog position: 14; exact link supplied in the user's source guide, page 19.
- Canonical repository: [actualbudget/actual](https://github.com/actualbudget/actual).
- Default branch: `master`.
- Reviewed HEAD commit: [`c09b17bbccbe6a262f1eb3853cc5b61a77afba7f`](https://github.com/actualbudget/actual/commit/c09b17bbccbe6a262f1eb3853cc5b61a77afba7f).
- Documentation review date: 2026-11-07. These observations are pinned to that commit; later upstream changes require a fresh review.

## Specific study use case

Study local-first transaction import, reconciliation and synchronization using synthetic budgets only.

Local-first personal budgeting application with optional synchronization and bank-data integrations.

## Setup and service requirements

- Current package.json requires Node >= 22.18.0 and uses Yarn 4.17.1 (engine range ^4.9.1).
- Development: install from the repository root, then yarn start; Docker/Dev Container and packaged desktop alternatives are documented.
- Sync server is separate from local-only browser use; development server is documented on 3001, built sync server on 5006. Native dependencies can require platform build tools.

The following commands are documented upstream and were **not executed** in this review:

```sh
yarn install
yarn start
yarn build:server
yarn start:server
```

- No paid model API is required for core budgeting.
- Bank sync is optional, needs actual-server plus operator-owned provider credentials; service availability/charges and supported banks vary.
- Bank-sync tokens are stored on the server outside budget end-to-end encryption. No financial accounts were connected and no transactions were moved.

## One possible extension — not implemented

Add an import dry-run report for duplicate detection and reconciliation on a synthetic transaction fixture.

This is an idea for a future bounded change, not a completed feature, contribution, runtime result or user outcome.

## Verification status

Only read-only repository metadata, current documentation and license text were reviewed. No dependency installation, package execution, application build, automated tests, browser checks, provider requests or deployment was performed. Test result: **not run**. The upstream README, screenshots and CI claims are not our verification results.

## License boundary

Reviewed file: [LICENSE.txt](https://github.com/actualbudget/actual/blob/c09b17bbccbe6a262f1eb3853cc5b61a77afba7f/LICENSE.txt). SPDX: **MIT**.

Keep the upstream copyright and permission notice with copies or substantial portions. Preserve the license and warranty disclaimer. Dependencies, assets, model weights, provider terms and trademarks can have separate conditions. The code license does not grant bank/API access or replace provider terms; this library review is not financial advice.

Adding these notes does not relicense upstream code or third-party content. This entry does not claim affiliation, original authorship, production readiness or an official competition submission.

## Primary evidence

- [Canonical upstream](https://github.com/actualbudget/actual)
- [Reviewed commit](https://github.com/actualbudget/actual/commit/c09b17bbccbe6a262f1eb3853cc5b61a77afba7f)
- [README.md](https://github.com/actualbudget/actual/blob/c09b17bbccbe6a262f1eb3853cc5b61a77afba7f/README.md)
- [LICENSE.txt](https://github.com/actualbudget/actual/blob/c09b17bbccbe6a262f1eb3853cc5b61a77afba7f/LICENSE.txt)
- [package.json](https://github.com/actualbudget/actual/blob/c09b17bbccbe6a262f1eb3853cc5b61a77afba7f/package.json)
- [CONTRIBUTING.md](https://github.com/actualbudget/actual/blob/c09b17bbccbe6a262f1eb3853cc5b61a77afba7f/CONTRIBUTING.md)
- [Development setup](https://actualbudget.org/docs/contributing/development-setup/)
- [Build from source](https://actualbudget.org/docs/install/build-from-source/)
- [Bank sync](https://actualbudget.org/docs/advanced/bank-sync/)

