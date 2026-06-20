# Beam (beam-cloud)

Beam (beam.cloud) is a serverless GPU and Python cloud-runtime platform. You write ordinary Python, decorate it, and Beam deploys it as a web endpoint, a task queue, a scheduled job, or a secure sandbox running on on-demand CPU and GPU containers with per-second billing, rapid cold starts, and automatic scaling.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/beam-cloud/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/beam-cloud/refs/heads/main/apis.yml)

## Tags

- Serverless
- GPU
- Python
- Inference
- Containers

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Beam Web Endpoints API

Synchronous invocation of deployed Python functions exposed as REST web endpoints. Each deployment is reachable both by a versioned app subdomain (https://{name}-{id}-v{n}.app.beam.cloud) and by a named or id path on the shared host (https://app.beam.cloud/endpoint/{name} or /endpoint/id/{id}). Endpoints are for synchronous work completing within ~180 seconds; Bearer token auth.

- **Human URL:** [https://docs.beam.cloud/v2/endpoint/overview](https://docs.beam.cloud/v2/endpoint/overview)
- **Base URL:** `https://app.beam.cloud`

#### Tags

- Web Endpoints
- Function Invocation
- Serverless

#### Properties

- [Documentation](https://docs.beam.cloud/v2/endpoint/overview)
- [API Reference](https://docs.beam.cloud/v2/getting-started/quickstart)
- [OpenAPI](openapi/beam-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beam-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beam-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/beam-cloud-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [GitHub](https://github.com/beam-cloud/beta9)

### Beam Task Queues API

Asynchronous task submission for long-running work. POST to a deployed task-queue app returns a task_id; results and state are then polled from the control-plane Tasks API (GET https://api.beam.cloud/v2/task/{task_id}/) or delivered to a configured callback_url webhook.

- **Human URL:** [https://docs.beam.cloud/v2/task-queue/running-tasks](https://docs.beam.cloud/v2/task-queue/running-tasks)
- **Base URL:** `https://api.beam.cloud`

#### Tags

- Task Queues
- Async
- Background Jobs

#### Properties

- [Documentation](https://docs.beam.cloud/v2/task-queue/running-tasks)
- [API Reference](https://docs.beam.cloud/v2/task-queue/query-status)
- [OpenAPI](openapi/beam-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beam-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beam-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [GitHub](https://github.com/beam-cloud/beta9)

### Beam Tasks Management API

Control-plane REST API on api.beam.cloud for retrieving task status and metadata (GET /v2/task/{task_id}/) and cancelling one or more running tasks (DELETE /v2/task/cancel/). Bearer token auth; used to manage deployments and the lifecycle of async invocations.

- **Human URL:** [https://docs.beam.cloud/v2/reference/api-docs/tasks/tasks-status](https://docs.beam.cloud/v2/reference/api-docs/tasks/tasks-status)
- **Base URL:** `https://api.beam.cloud`

#### Tags

- Tasks
- Management
- Deployments

#### Properties

- [Documentation](https://docs.beam.cloud/v2/reference/api-docs/tasks/tasks-status)
- [API Reference](https://docs.beam.cloud/v2/reference/api-docs/tasks/tasks-cancel)
- [OpenAPI](openapi/beam-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beam-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beam-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [GitHub](https://github.com/beam-cloud/beta9)

### Beam Sandboxes and Volumes API

Secure, programmable sandbox containers for arbitrary code execution (filesystem and process operations) plus distributed storage Volumes and mounted external S3 buckets. Driven primarily through the Beam Python/TypeScript SDK and CLI on top of the same container runtime that powers endpoints and task queues.

- **Human URL:** [https://docs.beam.cloud/v2/sandbox/overview](https://docs.beam.cloud/v2/sandbox/overview)
- **Base URL:** `https://app.beam.cloud`

#### Tags

- Sandboxes
- Volumes
- Code Execution

#### Properties

- [Documentation](https://docs.beam.cloud/v2/sandbox/overview)
- [API Reference](https://docs.beam.cloud/v2/data/volume)
- [OpenAPI](openapi/beam-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beam-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beam-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [GitHub](https://github.com/beam-cloud/beta9)

## Common Properties

- [GitHub Organization](https://github.com/beam-cloud)
- [LinkedIn](https://www.linkedin.com/company/beam-cloud)
- [Website](https://www.beam.cloud)
- [Documentation](https://docs.beam.cloud)
- [Plans](plans/beam-cloud-plans-pricing.yml)
- [Rate Limits](rate-limits/beam-cloud-rate-limits.yml)
- [Fin Ops](finops/beam-cloud-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
