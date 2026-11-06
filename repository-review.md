# Engineering library — 15 source reviews

Reviewed on 6 November 2026. Scope: current primary README, root structure, retained license and available root agent guidance. This is not a line-by-line source audit or a runtime benchmark. The account's existing application repositories and these upstream references are separate bodies of work.

## 1. [fastapi/full-stack-fastapi-template](https://github.com/fastapi/full-stack-fastapi-template)

**Application foundation.** FastAPI API, React interface, SQLModel data access and PostgreSQL, with Docker Compose and separate backend/frontend guidance.

**Application:** Useful when an AI feature needs a real application boundary: authentication, a database and a typed client around model calls.

**Trade-off:** The template supplies application infrastructure; retrieval, model quality and domain-specific permissions still need their own design.

**Verification plan:** Trace an authenticated request from UI to API; check a denied request; verify migrations on disposable data.

## 2. [pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai)

**Typed AI workflows.** Provider adapters, typed agent outputs, tools, dependency injection and evaluation packages are separated in the repository.

**Application:** A candidate for document extraction where a valid response must match an explicit schema and a failed tool call must be visible.

**Trade-off:** Schema-valid output can still be factually wrong. Business invariants and source verification belong outside the model response.

**Verification plan:** Use valid, missing-field and contradictory fixtures; assert the schema and factual constraints separately.

## 3. [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph)

**Stateful orchestration.** A low-level stateful workflow engine with persistence, interruption and resumption, plus separate libraries, examples and docs.

**Application:** A candidate for multi-step document workflows that must pause for human approval before an external action.

**Trade-off:** Durable state does not make side effects idempotent. Repeated external calls need a stable operation key and reconciliation.

**Verification plan:** Stop after a tool dispatch, resume the workflow, and verify that the external action is not repeated.

## 4. [run-llama/llama_index](https://github.com/run-llama/llama_index)

**Document retrieval.** Core and integration packages support document ingestion, indexing and retrieval; the current README distinguishes the OSS framework from the company's document-processing focus.

**Application:** A candidate for connecting a document collection to a cited answer workflow with inspectable retrieval inputs.

**Trade-off:** The current upstream focus has shifted toward parsing/extraction products. Select integrations explicitly instead of assuming a stable all-in-one roadmap.

**Verification plan:** Use a small labelled corpus; inspect retrieved chunks; include no-answer and conflicting-source queries.

## 5. [scikit-learn/scikit-learn](https://github.com/scikit-learn/scikit-learn)

**ML baselines.** Scientific Python estimators, examples, benchmarks and tests live in a mature library with a BSD 3-Clause license.

**Application:** A candidate for an interpretable baseline before adding an LLM to a classification or ranking problem.

**Trade-off:** Avoid data leakage: preprocessing and feature selection must be learned on training folds, not on the whole dataset.

**Verification plan:** Keep a held-out set; compare a dummy baseline; record the split seed and per-class metrics.

## 6. [promptfoo/promptfoo](https://github.com/promptfoo/promptfoo)

**LLM evaluation.** A TypeScript CLI/library with evaluation configs, providers, examples and a dedicated test suite.

**Application:** A candidate for repeatable quality checks on prompts and RAG answers before changing a model or prompt version.

**Trade-off:** Evaluation quality depends on the fixtures and assertions. A green result on a narrow dataset is not a production guarantee.

**Verification plan:** Include normal, unsupported, malformed and conflicting inputs; keep provider calls and costs explicit; run tests only on owned fixtures.

## 7. [qdrant/qdrant](https://github.com/qdrant/qdrant)

**Vector retrieval service.** A Rust vector database with payload filters, API specifications, server code, tests and configuration.

**Application:** A candidate when retrieval needs a dedicated service and explicit payload-based filtering.

**Trade-off:** A vector match is not an authorization decision. Tenant and document permissions must be enforced with the query and the application.

**Verification plan:** Test cross-tenant denial, filtered queries, deleted documents and a restore on disposable data.

## 8. [pgvector/pgvector](https://github.com/pgvector/pgvector)

**Vectors in PostgreSQL.** A PostgreSQL extension for exact and approximate vector similarity search; SQL, C source and tests are kept together.

**Application:** A candidate when business records and embeddings should share PostgreSQL transactions and relational filtering.

**Trade-off:** Choose distance and indexes to match the embedding model; approximate search needs recall/latency measurement on the actual corpus.

**Verification plan:** Compare approximate results against exact search; test filtered recall; verify an index migration on disposable data.

## 9. [ollama/ollama](https://github.com/ollama/ollama)

**Model runtime.** A model runtime with a local REST API, server code, model handling and platform-specific execution paths.

**Application:** A candidate for local inference experiments where the chosen model, runtime and hardware can be recorded.

**Trade-off:** The runtime's MIT license does not determine model-weight licenses. Local execution also does not automatically secure an exposed endpoint.

**Verification plan:** Bind the test service to the intended interface; record model identity and hardware; check timeout and resource-exhaustion behaviour.

## 10. [huggingface/transformers](https://github.com/huggingface/transformers)

**Model integration.** Shared model definitions, preprocessing and pipeline APIs support inference and training across text and multimodal tasks.

**Application:** A candidate when a product needs explicit control over a model checkpoint and preprocessing rather than only a hosted chat interface.

**Trade-off:** The library license and each model's license are separate. Record checkpoint revision, memory needs and any remote-code requirement.

**Verification plan:** Use a pinned checkpoint revision and a tiny non-sensitive fixture; inspect tokenization and model outputs separately.

## 11. [streamlit/streamlit](https://github.com/streamlit/streamlit)

**Data application UI.** Python application logic, frontend packages, protobuf definitions and end-to-end tests support interactive data applications.

**Application:** A candidate for an internal evaluation dashboard or a small inspectable data application.

**Trade-off:** Cache and session boundaries need review when documents are private. The current README says outside PR acceptance is paused; do not promise an upstream contribution.

**Verification plan:** Test two independent sessions, a cache invalidation and an empty/error state before sharing a dashboard.

## 12. [gradio-app/gradio](https://github.com/gradio-app/gradio)

**Model demo UI.** Python functions are exposed through interfaces/blocks, with separate client, frontend, backend, demo and test areas.

**Application:** A candidate for a clear model demonstration with controlled inputs and inspectable outputs.

**Trade-off:** A public share link can expose the application. Treat file handling, input limits and authenticated access as deliberate deployment choices.

**Verification plan:** Test empty and oversized inputs, file cleanup and an explicit error response; keep the initial demonstration local.

## 13. [donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer)

**Architecture reference.** An organized system-design reference with trade-offs, sample solutions and exercises; its license text states CC BY 4.0.

**Application:** A reference for writing short architecture decisions: requirements, alternatives, capacity assumptions and failure handling.

**Trade-off:** The examples are study resources, not proof that this account operated systems at their example scale.

**Verification plan:** Write one bounded design case, list assumptions, explain a rejected alternative and define a failure-recovery test.

## 14. [astral-sh/ruff](https://github.com/astral-sh/ruff)

**Python quality tooling.** A Rust workspace implements Python linting and formatting with configuration, rules and repository development guidance.

**Application:** A candidate for a fast, consistent quality gate alongside tests and type checks in an AI application repository.

**Trade-off:** Formatting and linting do not establish semantic correctness, security or model quality. Review automatic fixes before applying them.

**Verification plan:** Run lint and formatting checks on an owned small fixture; keep functional and model-quality tests as separate evidence.

## 15. [react/react](https://github.com/react/react)

**Product interface layer.** Declarative components and state-driven rendering, with core packages, fixtures, compiler work and contribution guidance.

**Application:** A reference for TypeScript product interfaces, particularly explicit loading, error and empty states around AI operations.

**Trade-off:** A React-core fork is a source-study reference; it is not an original UI framework or evidence of upstream maintainer status.

**Verification plan:** For an application change, verify keyboard interaction, cancellation, loading/error states and rendering of untrusted model text.

