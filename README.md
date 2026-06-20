# Activeloop (activeloop)

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
