# Argo CD

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

Argo CD is a declarative GitOps continuous-delivery tool for Kubernetes, part of the CNCF Graduated Argo project. The argocd-server component exposes a gRPC and REST API used by the Web UI, the argocd CLI, and CI/CD systems. APIs cover applications, projects, clusters, repositories, accounts, certificates, GPG keys, sessions, settings, and notifications. Argo CD is also a Kubernetes operator that defines first-class CRDs (Application, ApplicationSet, AppProject) — those CRDs are themselves a Kubernetes-native API. Argo CD is open-source under the Apache 2.0 license; commercial offerings are provided by third parties (notably Akuity, founded by the Argo project's creators) rather than the Argo CD project itself.

**Areas:** ArgoCD · DevOps · GitOps · Kubernetes · Continuous Delivery · CNCF · Open Source · Operator · Cloud-Native · CI/CD

## Argo CD on APIs.io

Everything profiled for Argo CD is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/argocd/](https://apis.io/providers/argocd/)** — or go straight to one of the APIs or properties below.

### APIs (27)

- [Argo CD ApplicationSets API](https://apis.io/apis/argocd/argocd-applicationsets-api/) — The Argo CD ApplicationSets API (/api/v1/applicationsets) manages ApplicationSet resources — templated app generators (List, Cluster, Git, Matrix, Merge,…
- [Argo CD Projects API](https://apis.io/apis/argocd/argocd-projects-api/) — The Argo CD Projects API (/api/v1/projects) manages AppProject resources — multi-tenant boundaries that restrict the source repos, destination…
- [Argo CD Clusters API](https://apis.io/apis/argocd/argocd-clusters-api/) — The Argo CD Clusters API (/api/v1/clusters) registers, updates, lists, and removes target Kubernetes clusters that Argo CD deploys into, including cluster…
- [Argo CD Repositories API](https://apis.io/apis/argocd/argocd-repositories-api/) — The Argo CD Repositories API (/api/v1/repositories and /api/v1/repocreds) manages Git, Helm chart, and OCI-registry source repositories with credentials,…
- [Argo CD Accounts API](https://apis.io/apis/argocd/argocd-accounts-api/) — The Argo CD Accounts API (/api/v1/account) manages local accounts and their API tokens (capability for service accounts), including password rotation and…
- [Argo CD Sessions API](https://apis.io/apis/argocd/argocd-sessions-api/) — The Argo CD Sessions API (/api/v1/session) issues bearer tokens for username/password and OIDC-authenticated sessions used by all other API endpoints.
- [Argo CD Settings API](https://apis.io/apis/argocd/argocd-settings-api/) — The Argo CD Settings API (/api/v1/settings) returns the active server configuration — UI banner, OIDC config, Helm/Kustomize plugin defaults, resource…
- [Argo CD Certificates API](https://apis.io/apis/argocd/argocd-certificates-api/) — The Argo CD Certificates API (/api/v1/certificates) manages TLS certificates and SSH known_hosts entries used to securely connect to private Git, Helm, and…
- [Argo CD GPG Keys API](https://apis.io/apis/argocd/argocd-gpgkeys-api/) — The Argo CD GPG Keys API (/api/v1/gpgkeys) registers and removes GPG public keys used to verify signed commits before they are deployed.
- [Argo CD Notifications API](https://apis.io/apis/argocd/argocd-notifications-api/) — The Argo CD Notifications subsystem delivers app lifecycle events (sync, health, deploy) to webhooks, Slack, MS Teams, email, GitHub commit status, and…
- [Argo CD Version API](https://apis.io/apis/argocd/argocd-version-api/) — The Argo CD Version API (/api/version) returns the running argocd-server build version, Kustomize/Helm/Jsonnet versions, and Kubernetes server version.
- [Argo CD Application CRD](https://apis.io/apis/argocd/argocd-application-crd/) — Argo CD defines an Application Custom Resource Definition (argoproj.io/v1alpha1, kind=Application) describing a desired sync of a single source…
- [Argo CD ApplicationSet CRD](https://apis.io/apis/argocd/argocd-applicationset-crd/) — Argo CD defines an ApplicationSet Custom Resource Definition (argoproj.io/v1alpha1, kind=ApplicationSet) which templatizes Application creation across many…
- [Argo CD AppProject CRD](https://apis.io/apis/argocd/argocd-appproject-crd/) — Argo CD defines an AppProject Custom Resource Definition (argoproj.io/v1alpha1, kind=AppProject) which scopes which sources, destinations, and resource…
- [Argo CD AccountService API](https://apis.io/apis/argocd/argocd-accountservice-api/) — The AccountService API from Argo CD — 6 operation(s) for accountservice.
- [Argo CD ApplicationService API](https://apis.io/apis/argocd/argocd-applicationservice-api/) — The ApplicationService API from Argo CD — 26 operation(s) for applicationservice.
- [Argo CD ApplicationSetService API](https://apis.io/apis/argocd/argocd-applicationsetservice-api/) — The ApplicationSetService API from Argo CD — 6 operation(s) for applicationsetservice.
- [Argo CD CertificateService API](https://apis.io/apis/argocd/argocd-certificateservice-api/) — The CertificateService API from Argo CD — 1 operation(s) for certificateservice.
- [Argo CD ClusterService API](https://apis.io/apis/argocd/argocd-clusterservice-api/) — The ClusterService API from Argo CD — 4 operation(s) for clusterservice.
- [Argo CD GPGKeyService API](https://apis.io/apis/argocd/argocd-gpgkeyservice-api/) — The GPGKeyService API from Argo CD — 2 operation(s) for gpgkeyservice.
- [Argo CD ProjectService API](https://apis.io/apis/argocd/argocd-projectservice-api/) — The ProjectService API from Argo CD — 10 operation(s) for projectservice.
- [Argo CD RepoCredsService API](https://apis.io/apis/argocd/argocd-repocredsservice-api/) — The RepoCredsService API from Argo CD — 6 operation(s) for repocredsservice.
- [Argo CD RepositoryService API](https://apis.io/apis/argocd/argocd-repositoryservice-api/) — The RepositoryService API from Argo CD — 13 operation(s) for repositoryservice.
- [Argo CD SessionService API](https://apis.io/apis/argocd/argocd-sessionservice-api/) — The SessionService API from Argo CD — 2 operation(s) for sessionservice.
- [Argo CD SettingsService API](https://apis.io/apis/argocd/argocd-settingsservice-api/) — The SettingsService API from Argo CD — 2 operation(s) for settingsservice.
- [Argo CD VersionService API](https://apis.io/apis/argocd/argocd-versionservice-api/) — The VersionService API from Argo CD — 1 operation(s) for versionservice.
- [Argo CD Notification Service API](https://apis.io/apis/argocd/argocd-notification-service-api/) — The Notification Service API from Argo CD — 3 operation(s) for notification service.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Argocd Agentic Access](https://apis.io/agentic-access/argocd/argocd-agentic-access/)

#### Collections (14)

Postman and Open Collection request collections.

- [Consolidate Services AccountService API](https://apis.io/collections/argocd/open-argocd-accountservice-api/)
- [Consolidate Services AccountService ApplicationService API](https://apis.io/collections/argocd/open-argocd-applicationservice-api/)
- [Consolidate Services AccountService ApplicationSetService API](https://apis.io/collections/argocd/open-argocd-applicationsetservice-api/)
- [Consolidate Services AccountService CertificateService API](https://apis.io/collections/argocd/open-argocd-certificateservice-api/)
- [Consolidate Services AccountService ClusterService API](https://apis.io/collections/argocd/open-argocd-clusterservice-api/)
- [Consolidate Services AccountService GPGKeyService API](https://apis.io/collections/argocd/open-argocd-gpgkeyservice-api/)
- [Consolidate Services AccountService NotificationService API](https://apis.io/collections/argocd/open-argocd-notificationservice-api/)
- [Consolidate Services AccountService ProjectService API](https://apis.io/collections/argocd/open-argocd-projectservice-api/)
- [Consolidate Services AccountService RepoCredsService API](https://apis.io/collections/argocd/open-argocd-repocredsservice-api/)
- [Consolidate Services AccountService RepositoryService API](https://apis.io/collections/argocd/open-argocd-repositoryservice-api/)
- [Consolidate Services](https://apis.io/collections/argocd/open-argocd-server/)
- [Consolidate Services AccountService SessionService API](https://apis.io/collections/argocd/open-argocd-sessionservice-api/)
- [Consolidate Services AccountService SettingsService API](https://apis.io/collections/argocd/open-argocd-settingsservice-api/)
- [Consolidate Services AccountService VersionService API](https://apis.io/collections/argocd/open-argocd-versionservice-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Argo CD API Rules](https://apis.io/rules/argocd/argocd-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Argocd Authentication](https://apis.io/security/argocd/argocd-authentication/)
- [Argocd Domain Security](https://apis.io/security/argocd/argocd-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Argocd Plans Pricing](https://apis.io/plans/argocd/argocd-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Argocd Rate Limits](https://apis.io/rate-limits/argocd/argocd-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Argocd Finops](https://apis.io/finops/argocd/argocd-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://argo-cd.readthedocs.io/)
- [Documentation](https://argo-cd.readthedocs.io/en/stable/)
- [Getting started](https://argo-cd.readthedocs.io/en/stable/getting_started/)
- [API reference](https://argo-cd.readthedocs.io/en/stable/developer-guide/api-docs/)
- [Support](https://github.com/argoproj/argo-cd/issues)
- [Changelog](https://github.com/argoproj/argo-cd/blob/master/CHANGELOG.md)
- [Blog](https://blog.argoproj.io/)
- [GitHub](https://github.com/argoproj)

## API Evangelist rating

**Kin Score 36.6** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 48.2 |
| Contract quality | 35.7 |
| Contract governance | 27.3 |
| Operational transparency | 42.1 |
| Developer ergonomics | 61.9 |
| Access clarity | 5.3 |

**Agent readiness 22.5** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | yes |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 16.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/argocd/](https://apis.io/providers/argocd/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Argo CD: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/argocd/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
