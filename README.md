# Depot (depot-dev)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
