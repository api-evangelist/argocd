# Argo CD (argocd)

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
