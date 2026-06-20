# Graphite (graphite-dev)

Graphite is a code review platform built on top of GitHub for stacking pull requests, AI code review, and merging at scale. The gt CLI creates and submits stacked PRs, Graphite Agent (Diamond) provides codebase-aware AI review and chat, and a merge queue batches and tests PRs in parallel. Graphite has no standalone public REST API - it integrates through a GitHub App that consumes GitHub webhooks, the gt CLI (authenticated with a Graphite token), the GT MCP server, and label / GitHub-mediated integrations (Slack, Linear, external merge queue).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/graphite-dev/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/graphite-dev/refs/heads/main/apis.yml)

## Tags

- Code Review
- Stacked PRs
- Merge Queue
- AI Code Review
- Developer Tools
- GitHub

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Graphite GitHub App

Graphite installs as a GitHub App (graphite-app) on an organization to receive GitHub webhooks for real-time updates on CI status, mergeability, and push events, and to call GitHub's APIs with fine-grained permissions and short-lived tokens. GitHub is the only git provider Graphite integrates with; there is no standalone Graphite-hosted REST API.

- **Human URL:** [https://graphite.com/docs/authenticate-with-github-app](https://graphite.com/docs/authenticate-with-github-app)
- **Base URL:** `https://github.com/apps/graphite-app`

#### Tags

- GitHub App
- Webhooks
- Authentication

#### Properties

- [Documentation](https://graphite.com/docs/authenticate-with-github-app)
- [API Reference](https://github.com/marketplace/graphite-dev)
- [OpenAPI](openapi/graphite-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/graphite-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/graphite-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Graphite CLI (gt)

The gt command-line interface creates, stacks, submits, syncs, restacks, and merges pull requests from the terminal. It authenticates with a Graphite auth token (gt auth) and drives Graphite's hosted platform plus GitHub on the user's behalf.

- **Human URL:** [https://graphite.com/docs/cli-overview](https://graphite.com/docs/cli-overview)
- **Base URL:** `https://app.graphite.dev`

#### Tags

- CLI
- Stacked PRs
- Stacking

#### Properties

- [Documentation](https://graphite.com/docs/cli-overview)
- [API Reference](https://graphite.com/docs/command-reference)
- [OpenAPI](openapi/graphite-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/graphite-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/graphite-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Graphite GT MCP Server

GT MCP is a Model Context Protocol server built into the Graphite CLI (gt mcp) that lets AI agents in tools like Cursor and Claude Code automatically break large changes into smaller, reviewable stacked pull requests. It is a local MCP server over the CLI, not a remote HTTP API.

- **Human URL:** [https://graphite.com/docs/gt-mcp](https://graphite.com/docs/gt-mcp)
- **Base URL:** `https://graphite.com/docs/gt-mcp`

#### Tags

- MCP
- Model Context Protocol
- AI Agents

#### Properties

- [Documentation](https://graphite.com/docs/gt-mcp)
- [OpenAPI](openapi/graphite-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/graphite-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/graphite-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Graphite Agent (Diamond) AI Code Review

Graphite Agent (formerly Diamond, now unified with Graphite Chat) is a codebase-aware AI code review agent that comments on pull requests, answers questions, and helps fix and iterate on code. It is triggered on PRs through the Graphite platform and configured via repository settings, not via a public API.

- **Human URL:** [https://graphite.com/docs/ai-reviews](https://graphite.com/docs/ai-reviews)
- **Base URL:** `https://app.graphite.dev`

#### Tags

- AI Code Review
- Diamond
- Code Review

#### Properties

- [Documentation](https://graphite.com/docs/ai-reviews)
- [Documentation](https://graphite.com/docs/ai-review-customization)
- [OpenAPI](openapi/graphite-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/graphite-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/graphite-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Graphite Merge Queue

The Graphite merge queue batches and tests multiple PRs in parallel once they are ready, reducing wait times and merge conflicts. Integration with an external merge queue is label-based and GitHub-mediated rather than exposed as an HTTP API.

- **Human URL:** [https://graphite.com/docs/graphite-merge-queue](https://graphite.com/docs/graphite-merge-queue)
- **Base URL:** `https://app.graphite.dev`

#### Tags

- Merge Queue
- CI
- Automation

#### Properties

- [Documentation](https://graphite.com/docs/graphite-merge-queue)
- [Documentation](https://graphite.com/docs/external-merge-queue-integration)
- [OpenAPI](openapi/graphite-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/graphite-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/graphite-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Graphite Insights

Graphite Insights tracks team engineering velocity (PR throughput, review latency, and related stats) over indexed repositories, surfaced in the Graphite web app. No public analytics API is documented.

- **Human URL:** [https://graphite.com/docs/insights](https://graphite.com/docs/insights)
- **Base URL:** `https://app.graphite.dev`

#### Tags

- Insights
- Analytics
- Engineering Velocity

#### Properties

- [Documentation](https://graphite.com/docs/insights)
- [Documentation](https://graphite.com/docs/insights-stats-definitions)
- [OpenAPI](openapi/graphite-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/graphite-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/graphite-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/withgraphite)
- [LinkedIn](https://www.linkedin.com/company/graphite-dev)
- [Website](https://graphite.dev)
- [Documentation](https://graphite.com/docs)
- [Plans](plans/graphite-dev-plans-pricing.yml)
- [Rate Limits](rate-limits/graphite-dev-rate-limits.yml)
- [Fin Ops](finops/graphite-dev-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
