# Activeloop (activeloop)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Activeloop builds Deep Lake, a database for AI that stores multimodal datasets (text, images, video, audio, embeddings) in a deep-learning-optimized format. The primary interface is the open-source Deep Lake Python SDK paired with the Tensor Query Language (TQL); datasets live locally, in your own cloud (S3, Azure, GCP), or in the managed Activeloop Cloud (app.activeloop.ai), which also exposes an alpha Managed Database REST query endpoint.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/activeloop/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/activeloop/refs/heads/main/apis.yml)

## Tags

- AI
- Vector Store
- Data Lake
- Multimodal
- Deep Learning
- Python SDK

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Deep Lake SDK (Python)

The open-source `deeplake` Python package (Apache-2.0) is the primary interface to Deep Lake. It creates, reads, writes, versions, and streams multimodal datasets and embeddings in the Deep Lake format against local, S3, Azure, GCP, or Activeloop-cloud storage, with NumPy-like indexing and PyTorch / TensorFlow dataloaders. This is an SDK / library interface, not a REST API.

- **Human URL:** [https://docs.deeplake.ai/](https://docs.deeplake.ai/)

#### Tags

- Python SDK
- Datasets
- Multimodal
- Data Versioning

#### Properties

- [Documentation](https://docs.deeplake.ai/)
- [API Reference](https://docs-v3.activeloop.ai/)
- [OpenAPI](openapi/activeloop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/activeloopai/deeplake)

### Tensor Query Language (TQL)

A high-performance, SQL-like query engine (implemented in C++ inside Deep Lake) for filtering datasets and running hybrid embedding-plus-attribute search. TQL queries are executed through the SDK via `ds.query(<query_string>)` or `vector_store.search(query=<query_string>)`, and require an authenticated Activeloop account (not available on purely local datasets). This is a query language surfaced through the SDK, not a standalone REST API.

- **Human URL:** [https://docs-v3.activeloop.ai/examples/tql](https://docs-v3.activeloop.ai/examples/tql)

#### Tags

- TQL
- Query Engine
- Search
- Filtering

#### Properties

- [Documentation](https://docs-v3.activeloop.ai/examples/tql)
- [OpenAPI](openapi/activeloop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/activeloopai/deeplake)

### Deep Lake Vector Store

A multimodal vector store, exposed through the Deep Lake Python SDK (`VectorStore`), that stores embeddings with their metadata and supports similarity and hybrid (TQL) search. Integrates with LangChain and LlamaIndex as a vector store for LLM / RAG applications. Accessed via the SDK, not a broad REST API.

- **Human URL:** [https://docs-v3.activeloop.ai/examples/rag/tutorials/vector-store-basics](https://docs-v3.activeloop.ai/examples/rag/tutorials/vector-store-basics)

#### Tags

- Vector Store
- Embeddings
- RAG
- Similarity Search

#### Properties

- [Documentation](https://docs-v3.activeloop.ai/examples/rag/tutorials/vector-store-basics)
- [OpenAPI](openapi/activeloop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/activeloopai/deeplake)

### Activeloop Managed Database REST API

An alpha REST endpoint for the Managed Tensor Database that accepts a TQL query string over HTTP POST and returns query results. Requires a Bearer `ACTIVELOOP_TOKEN` and a dataset hosted in the managed database (`tensor_db: True`). Documented as Alpha; syntax may change without notice. This is the only documented REST surface - the primary interface to Deep Lake remains the Python SDK plus TQL.

- **Human URL:** [https://docs-v3.activeloop.ai/examples/rag/tutorials/vector-search-options/rest-api](https://docs-v3.activeloop.ai/examples/rag/tutorials/vector-search-options/rest-api)
- **Base URL:** `https://app.activeloop.ai/api/query/v1`

#### Tags

- REST
- Managed Database
- Query
- Alpha

#### Properties

- [Documentation](https://docs-v3.activeloop.ai/examples/rag/tutorials/vector-search-options/rest-api)
- [OpenAPI](openapi/activeloop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [GitHub Organization](https://github.com/activeloopai)
- [LinkedIn](https://www.linkedin.com/company/activeloop)
- [Website](https://www.activeloop.ai)
- [Documentation](https://docs.deeplake.ai/)
- [Plans](plans/activeloop-plans-pricing.yml)
- [Rate Limits](rate-limits/activeloop-rate-limits.yml)
- [Fin Ops](finops/activeloop-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
