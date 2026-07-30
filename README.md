# Lightning AI

Lightning AI is an AI development platform from the team behind PyTorch Lightning. It provides cloud AI Studios (persistent GPU-backed development workspaces), ephemeral Sandboxes for running untrusted or agent-generated code, multi-node training and finetuning, batch and real-time inference deployments, and hosted Model APIs that expose frontier LLMs behind an API key.

The platform is driven programmatically through the `lightning-sdk` Python SDK, the `@lightningai/sdk` JavaScript Sandbox SDK, and the `lightning` CLI, and is backed by a family of widely adopted open-source libraries including PyTorch Lightning, Lightning Fabric, LitServe, LitData, TorchMetrics and Thunder. Lightning AI runs as a fully managed cloud or inside a customer VPC, and is SOC 2 Type II and HIPAA certified.

- Website: https://lightning.ai/
- Documentation: https://lightning.ai/docs/
- GitHub: https://github.com/Lightning-AI
- Status: https://status.lightning.ai/

Backed by: index-ventures, sv-angel

## Artifacts

| Artifact | Path | Method |
|---|---|---|
| llms.txt | `llms/lightning-ai-llms.txt` | searched (verbatim) |
| Packages / SDKs | `packages/lightning-ai-packages.yml` | searched |
| CLI | `cli/lightning-ai-cli.yml` | searched |
| Sandbox | `sandbox/lightning-ai-sandbox.yml` | searched |
| Authentication | `authentication/lightning-ai-authentication.yml` | searched |
| Conventions | `conventions/lightning-ai-conventions.yml` | searched |
| Error catalog | `errors/lightning-ai-error-codes.yml` | searched |
| Data model | `data-model/lightning-ai-data-model.yml` | derived |
| Lifecycle | `lifecycle/lightning-ai-lifecycle.yml` | searched |
| Conformance | `conformance/lightning-ai-conformance.yml` | searched |
| Rate limits | `rate-limits/lightning-ai-rate-limits.yml` | searched |
| Plans | `plans/lightning-ai-plans.yml` | searched |
| Changelog | `changelog/lightning-ai-changelog.yml` | searched |
| Well-known | `well-known/lightning-ai-well-known.yml` | searched (none published) |
| Domain security | `security/lightning-ai-domain-security.yml` | probed |

## Not published by this provider

Recorded as honest negatives, not fabricated:

- **No OpenAPI / Swagger definition.** The documented contract is the SDK and CLI surface. This is why there is no `openapi/`, `overlays/`, `skills/`, `agentic-access/` or `arazzo/`.
- **No `/.well-known/` surface.** `lightning.ai` is a single-page app that returns HTTP 200 with an identical shell for every unmatched path, so status codes are not meaningful there — every probe was content-checked. See `well-known/lightning-ai-well-known.yml`.
- **No OAuth 2.0 / OIDC**, so no `scopes/` artifact — the platform uses teamspace-scoped API keys.
- **No idempotency-key contract**, so no `Idempotency` pointer. Only `Sandbox.delete()` is documented as idempotent.
- **No event, streaming or webhook surface**, so no `asyncapi/`.
- **No vulnerability disclosure program or trust center** was found by probe.
- **No MCP server, deprecation policy, or public SLA** is documented.
