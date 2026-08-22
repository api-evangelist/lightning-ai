# Lightning AI

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
