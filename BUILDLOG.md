# Build log — 2026-11-07

A dated snapshot of local validation for three original, AI-assisted portfolio demonstrators. All three use Python 3.11+ and the standard library, with synthetic fixtures and independently runnable examples.

## Local checks

The complete unittest suites were run locally on **2026-11-07** with Python 3.11. All **92 tests passed**:

| Project | Local source revision | Tests passed |
| --- | --- | ---: |
| [Flow Inbox](https://github.com/abusanaevdias/flow-inbox) | `ed91ca728b06c3f2834c42e98ee03fac3ad62588` | 23 |
| [Retrieval Bench](https://github.com/abusanaevdias/retrieval-bench) | `537f2cd17cc7fcc67e8948bb0fb95705cdd07b74` | 35 |
| [Yummy Operations API](https://github.com/abusanaevdias/yummy-operations-api) | `cb14be58428a87c5491c346fde978b1622e837fc` | 34 |
| **Total** | | **92** |

To repeat a suite, run this command from its repository directory:

```bash
python3.11 -B -m unittest -q
```

The revisions above identify the local sources checked. GitHub publication commits can have different identifiers. This log records local runs; it does not report automated CI results or a deployment.

## What each project demonstrates

**Flow Inbox** persists webhook-style JSON intake in SQLite, deduplicates matching requests, fences worker completion with lease tokens, and records retries and terminal states. Tests use temporary databases, competing threads, real loopback HTTP, and CLI subprocesses. Processing outcomes are simulated locally; no external job delivery is performed. Authentication, webhook signatures, heartbeat renewal, retention, and production operations remain outside its scope.

**Retrieval Bench** implements an inspectable BM25 lexical baseline, explicit relevance judgments, recall/MRR and no-answer accounting, configuration comparisons, and reproducible JSON/HTML reports. The tests check metric arithmetic, empty denominators, strict input handling, report escaping, and repeatability. The bundled corpus is synthetic. Scores describe retrieval against supplied exhaustive labels; they do not measure generated-answer correctness or establish model quality. BM25 is an established algorithm, not a new algorithm claimed by this project.

**Yummy Operations API** provides SQLite-backed templates, branches, employee state, and synthetic reservations with idempotent creation, immutable order snapshots, filters, and explicit state transitions. Tests cover restart persistence, concurrent duplicates, HTTP validation, malformed Unicode, and repeatable CLI fixtures. The existing [Yummy Admin](https://github.com/abusanaevdias/yummy) frontend remains a separate mock-data interface and is not connected. This API has no payment processing, authentication, dated inventory model, automatic expiry, or deployment.

## Review boundary

Independent local reviews examined transaction and idempotency behavior, invalid Unicode inputs, retrieval metric denominators, HTML escaping, and the accuracy of project documentation. Reproduced Unicode error paths in Flow Inbox and Yummy Operations API were fixed and covered by regression tests before the counts above were recorded.

The checks establish the tested local behavior. Production availability, load capacity, customer usage, employment experience, and commercial outcomes are not established by this snapshot. Each repository documents its own limitations and reproduction steps.
