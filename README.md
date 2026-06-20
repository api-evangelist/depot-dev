# Depot (depot-dev)

Depot is a fast container-image build and remote cache service. It runs Docker builds and GitHub Actions jobs on managed, single-tenant cloud compute with persistent BuildKit cache, and exposes Depot Cache as a remote cache backend for tools like Bazel, Go, Turborepo, Gradle, and sccache. Depot is programmable through a public API at api.depot.dev built on Connect (multiprotocol gRPC, gRPC-Web, and HTTP/JSON) for managing projects, tokens, and builds, plus the depot CLI.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/depot-dev/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/depot-dev/refs/heads/main/apis.yml)

## Tags

- Container Builds
- Docker
- BuildKit
- Remote Cache
- CI/CD
- GitHub Actions

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Depot Project API

Connect/gRPC ProjectService in the depot.core.v1 package for managing projects (Depot's unit of cache isolation), including create, get, list, update, delete, and cache-policy/reset operations. Exposed over HTTP/JSON as POST calls to /depot.core.v1.ProjectService/{Method}.

- **Human URL:** [https://depot.dev/docs/api/overview](https://depot.dev/docs/api/overview)
- **Base URL:** `https://api.depot.dev`

#### Tags

- Projects
- Organizations
- Cache Policy

#### Properties

- [Documentation](https://depot.dev/docs/container-builds/reference/api-overview)
- [API Reference](https://buf.build/depot/api/docs/main:depot.core.v1)
- [OpenAPI](openapi/depot-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/depot-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/depot-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Depot Build API

Connect/gRPC BuildService in the depot.build.v1 package for registering a build (returns a build ID and one-time build token), finishing a build, getting a build, and listing builds for a project. Exposed over HTTP/JSON as POST calls to /depot.build.v1.BuildService/{Method}.

- **Human URL:** [https://depot.dev/docs/api/api-container-builds-tutorial](https://depot.dev/docs/api/api-container-builds-tutorial)
- **Base URL:** `https://api.depot.dev`

#### Tags

- Builds
- Docker
- BuildKit

#### Properties

- [Documentation](https://depot.dev/blog/docker-build-api)
- [API Reference](https://depot.dev/docs/api/api-container-builds-tutorial)
- [OpenAPI](openapi/depot-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/depot-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/depot-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Depot BuildKit API

Connect/gRPC BuildKitService in the depot.buildkit.v1 package that acquires a lower-level BuildKit machine connection (endpoint plus TLS material) for advanced use cases that drive BuildKit directly. Exposed over HTTP/JSON as POST calls to /depot.buildkit.v1.BuildKitService/{Method}.

- **Human URL:** [https://depot.dev/docs/api/api-container-builds-tutorial](https://depot.dev/docs/api/api-container-builds-tutorial)
- **Base URL:** `https://api.depot.dev`

#### Tags

- BuildKit
- Endpoint
- Machine

#### Properties

- [Documentation](https://depot.dev/blog/depot-api)
- [OpenAPI](openapi/depot-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/depot-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/depot-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Depot Tokens API

Project-token management on the depot.core.v1 ProjectService (list, create, and delete project-scoped tokens). Project tokens are scoped to a single project and are the recommended credential for authenticating CI builds. Exposed over HTTP/JSON as POST calls to /depot.core.v1.ProjectService/{Method}.

- **Human URL:** [https://depot.dev/docs/container-builds/reference/api-authentication](https://depot.dev/docs/container-builds/reference/api-authentication)
- **Base URL:** `https://api.depot.dev`

#### Tags

- Tokens
- Authentication
- Project Tokens

#### Properties

- [Documentation](https://depot.dev/docs/container-builds/reference/api-authentication)
- [Documentation](https://depot.dev/blog/project-tokens)
- [OpenAPI](openapi/depot-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/depot-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/depot-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Depot GitHub Actions Runners

Managed, single-tenant GitHub Actions runners selected via runner labels (e.g. depot-ubuntu-24.04, depot-ubuntu-24.04-arm) across Intel, Arm/Graviton4, macOS, Windows, and GPU sizes. Runners are provisioned through a GitHub webhook integration rather than direct API calls; usage is billed per second at roughly half the cost of GitHub-hosted runners.

- **Human URL:** [https://depot.dev/docs/github-actions/overview](https://depot.dev/docs/github-actions/overview)
- **Base URL:** `https://api.depot.dev`

#### Tags

- GitHub Actions
- Runners
- CI/CD

#### Properties

- [Documentation](https://depot.dev/docs/github-actions/overview)
- [Documentation](https://depot.dev/products/github-actions)

### Depot Cache

Depot Cache is a remote build cache backend that plugs into tools supporting remote caching (GitHub Actions, Bazel, Go, Turborepo, Gradle, Pants, sccache). It is consumed through each tool's native remote-cache protocol authenticated with a Depot token, not through a separate REST API.

- **Human URL:** [https://depot.dev/docs/cache/overview](https://depot.dev/docs/cache/overview)
- **Base URL:** `https://api.depot.dev`

#### Tags

- Remote Cache
- Bazel
- Turborepo
- sccache

#### Properties

- [Documentation](https://depot.dev/docs/cache/overview)

## Common Properties

- [GitHub Organization](https://github.com/depot)
- [LinkedIn](https://www.linkedin.com/company/depot-dev)
- [Website](https://depot.dev/)
- [Documentation](https://depot.dev/docs)
- [Plans](plans/depot-dev-plans-pricing.yml)
- [Rate Limits](rate-limits/depot-dev-rate-limits.yml)
- [Fin Ops](finops/depot-dev-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
