# Argo CD (argocd)

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

Argo CD is a declarative GitOps continuous-delivery tool for Kubernetes, part of the CNCF Graduated Argo project. The argocd-server component exposes a gRPC and REST API used by the Web UI, the argocd CLI, and CI/CD systems. APIs cover applications, projects, clusters, repositories, accounts, certificates, GPG keys, sessions, settings, and notifications. Argo CD is also a Kubernetes operator that defines first-class CRDs (Application, ApplicationSet, AppProject) — those CRDs are themselves a Kubernetes-native API. Argo CD is open-source under the Apache 2.0 license; commercial offerings are provided by third parties (notably Akuity, founded by the Argo project's creators) rather than the Argo CD project itself.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/argocd/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/argocd/refs/heads/main/apis.yml)

## Tags

- DevOps
- GitOps
- Kubernetes
- Continuous Delivery
- CNCF
- Open Source
- Operator

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-19

## APIs

### Argo CD Applications API

The Argo CD Applications API (/api/v1/applications) creates, updates, deletes, syncs, refreshes, and rolls back applications, surfaces application resource trees, manifests, events, logs, and pod terminal access. All endpoints accept an optional `project` query parameter to scope by AppProject.

#### Tags

- Applications
- Sync
- GitOps
- Lifecycle

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/developer-guide/api-docs/)
- [API Reference](https://argo-cd.readthedocs.io/en/stable/operator-manual/server-commands/argocd-server/)
- [OpenAPI](openapi/argocd-server-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD ApplicationSets API

The Argo CD ApplicationSets API (/api/v1/applicationsets) manages ApplicationSet resources — templated app generators (List, Cluster, Git, Matrix, Merge, Pull Request, SCM Provider) used to programmatically scale Argo CD across many clusters and tenants.

#### Tags

- ApplicationSets
- Generators
- GitOps

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/applicationset/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Projects API

The Argo CD Projects API (/api/v1/projects) manages AppProject resources — multi-tenant boundaries that restrict the source repos, destination clusters/namespaces, and resource kinds available to a group of applications, plus per-project RBAC and JWT tokens.

#### Tags

- Projects
- AppProjects
- RBAC

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/user-guide/projects/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Clusters API

The Argo CD Clusters API (/api/v1/clusters) registers, updates, lists, and removes target Kubernetes clusters that Argo CD deploys into, including cluster credentials, sharding hints, and namespace scoping.

#### Tags

- Clusters
- Targets
- Kubernetes

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Repositories API

The Argo CD Repositories API (/api/v1/repositories and /api/v1/repocreds) manages Git, Helm chart, and OCI-registry source repositories with credentials, certificates, and per-repo settings used by the Application controller.

#### Tags

- Repositories
- Git
- Helm
- OCI

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/user-guide/private-repositories/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Accounts API

The Argo CD Accounts API (/api/v1/account) manages local accounts and their API tokens (capability for service accounts), including password rotation and token issuance/revocation.

#### Tags

- Accounts
- Authentication
- Tokens

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/user-management/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Sessions API

The Argo CD Sessions API (/api/v1/session) issues bearer tokens for username/password and OIDC-authenticated sessions used by all other API endpoints.

#### Tags

- Sessions
- Authentication
- JWT

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/developer-guide/api-docs/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Settings API

The Argo CD Settings API (/api/v1/settings) returns the active server configuration — UI banner, OIDC config, Helm/Kustomize plugin defaults, resource exclusions, application instance label key, and similar runtime settings.

#### Tags

- Settings
- Configuration
- Plugins

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/argocd-cm-yaml/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Certificates API

The Argo CD Certificates API (/api/v1/certificates) manages TLS certificates and SSH known_hosts entries used to securely connect to private Git, Helm, and OCI repositories.

#### Tags

- Certificates
- TLS
- SSH

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD GPG Keys API

The Argo CD GPG Keys API (/api/v1/gpgkeys) registers and removes GPG public keys used to verify signed commits before they are deployed.

#### Tags

- GPG
- Signed Commits
- Security

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/user-guide/gpg-verification/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Notifications API

The Argo CD Notifications subsystem delivers app lifecycle events (sync, health, deploy) to webhooks, Slack, MS Teams, email, GitHub commit status, and other channels via templated triggers.

#### Tags

- Notifications
- Webhooks
- Slack
- Email

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/notifications/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Version API

The Argo CD Version API (/api/version) returns the running argocd-server build version, Kustomize/Helm/Jsonnet versions, and Kubernetes server version.

#### Tags

- Version
- Build Info

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/developer-guide/api-docs/)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD Application CRD

Argo CD defines an Application Custom Resource Definition (argoproj.io/v1alpha1, kind=Application) describing a desired sync of a single source (Git/Helm/OCI) to a destination cluster/namespace, with sync policy, automated/manual sync, and ignore/diff rules.

#### Tags

- CRD
- Kubernetes
- Application
- GitOps

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/application.yaml/)
- [Source](https://github.com/argoproj/argo-cd/blob/master/manifests/crds/application-crd.yaml)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD ApplicationSet CRD

Argo CD defines an ApplicationSet Custom Resource Definition (argoproj.io/v1alpha1, kind=ApplicationSet) which templatizes Application creation across many targets via pluggable generators.

#### Tags

- CRD
- Kubernetes
- ApplicationSet
- Generators

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/applicationset/)
- [Source](https://github.com/argoproj/argo-cd/blob/master/manifests/crds/applicationset-crd.yaml)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Argo CD AppProject CRD

Argo CD defines an AppProject Custom Resource Definition (argoproj.io/v1alpha1, kind=AppProject) which scopes which sources, destinations, and resource kinds Applications inside the project may use, plus per-project RBAC.

#### Tags

- CRD
- Kubernetes
- AppProject
- RBAC

#### Properties

- [Documentation](https://argo-cd.readthedocs.io/en/stable/user-guide/projects/)
- [Source](https://github.com/argoproj/argo-cd/blob/master/manifests/crds/appproject-crd.yaml)
- [Postman Collection](collections/argocd-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/argocd-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/argoproj)
- [Website](https://argo-cd.readthedocs.io/)
- [Documentation](https://argo-cd.readthedocs.io/en/stable/)
- [API Reference](https://argo-cd.readthedocs.io/en/stable/developer-guide/api-docs/)
- [Getting Started](https://argo-cd.readthedocs.io/en/stable/getting_started/)
- [GitHub Organization](https://github.com/argoproj)
- [Source](https://github.com/argoproj/argo-cd)
- [License](https://github.com/argoproj/argo-cd/blob/master/LICENSE)
- [C N C F  Project](https://www.cncf.io/projects/argo/)
- [Helm  Chart](https://github.com/argoproj/argo-helm/tree/main/charts/argo-cd)
- [Slack  Community](https://argoproj.github.io/community/join-slack/)
- [Blog](https://blog.argoproj.io/)
- [X ( Twitter)](https://x.com/argoproj)
- [YouTube](https://www.youtube.com/@ArgoProj)
- [Releases](https://github.com/argoproj/argo-cd/releases)
- [Roadmap](https://github.com/argoproj/argo-cd/blob/master/docs/roadmap.md)
- [Contribution  Guide](https://argo-cd.readthedocs.io/en/stable/developer-guide/contributors-quickstart-guide/)
- [Operator  Manual](https://argo-cd.readthedocs.io/en/stable/operator-manual/)
- [User  Guide](https://argo-cd.readthedocs.io/en/stable/user-guide/)
- [Plans](plans/argocd-plans-pricing.yml)
- [Rate Limits](rate-limits/argocd-rate-limits.yml)
- [Fin Ops](finops/argocd-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
