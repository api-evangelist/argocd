# Argo CD (argocd)

Argo CD is a declarative GitOps continuous-delivery tool for Kubernetes, part of the CNCF Graduated Argo project. The argocd-server component exposes a gRPC and REST API used by the Web UI, the argocd CLI, and CI/CD systems, and Argo CD also defines first-class Kubernetes CRDs (Application, ApplicationSet, AppProject) that constitute its Kubernetes-native API.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/argocd/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=argocd-api-evangelist&utm_content=repo)

## Type

- **x-type:** opensource (CNCF Graduated, Apache License 2.0)

## Tags

 - DevOps, GitOps, Kubernetes, Continuous Delivery, CNCF, Open Source, Operator

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

| API | Description |
|---|---|
| Argo CD Applications API | `/api/v1/applications` — manage Applications, sync, refresh, rollback |
| Argo CD ApplicationSets API | `/api/v1/applicationsets` — templated Application generators |
| Argo CD Projects API | `/api/v1/projects` — multi-tenant AppProject scopes + RBAC |
| Argo CD Clusters API | `/api/v1/clusters` — register target Kubernetes clusters |
| Argo CD Repositories API | `/api/v1/repositories` and `/api/v1/repocreds` |
| Argo CD Accounts API | `/api/v1/account` — local accounts, tokens |
| Argo CD Sessions API | `/api/v1/session` — bearer-token issuance |
| Argo CD Settings API | `/api/v1/settings` — runtime config |
| Argo CD Certificates API | `/api/v1/certificates` — TLS / SSH known_hosts |
| Argo CD GPG Keys API | `/api/v1/gpgkeys` — verify signed commits |
| Argo CD Notifications | Lifecycle event delivery to Slack/email/webhook |
| Argo CD Version API | `/api/version` — running build info |
| Argo CD Application CRD | argoproj.io/v1alpha1 kind=Application |
| Argo CD ApplicationSet CRD | argoproj.io/v1alpha1 kind=ApplicationSet |
| Argo CD AppProject CRD | argoproj.io/v1alpha1 kind=AppProject |

## Common Properties

- [Website](https://argo-cd.readthedocs.io/)
- [Documentation](https://argo-cd.readthedocs.io/en/stable/)
- [API Reference](https://argo-cd.readthedocs.io/en/stable/developer-guide/api-docs/)
- [GitHub Organization](https://github.com/argoproj)
- [Source](https://github.com/argoproj/argo-cd)
- [License (Apache 2.0)](https://github.com/argoproj/argo-cd/blob/master/LICENSE)
- [CNCF Project](https://www.cncf.io/projects/argo/)
- [Plans](plans/argocd-plans-pricing.yml) — API Commons Plans 0.1 (FOSS — no commercial billing)
- [RateLimits](rate-limits/argocd-rate-limits.yml) — API Commons Rate Limits 0.1 (operator-tuned)
- [FinOps](finops/argocd-finops.yml) — FOCUS-aligned (FOSS — no commercial billing)

## Plans Summary

- **Open Source (Apache 2.0)** — free, CNCF Graduated, all features included
- **Third-Party Managed** — Akuity, Codefresh (Octopus Deploy), Kubernetes distribution vendors (out of scope of this profile)

## Rate Limits Summary

- **Failed login attempts:** default 5 / window (account locking)
- **Repo Server parallelism, kubectl parallelism, status-refresh** — operator-tuned via cluster config
- **External rate limits** — should be enforced via ingress / API gateway in front of argocd-server

## Artifacts

| Artifact | Path |
|---|---|
| Plans | `plans/argocd-plans-pricing.yml` |
| Rate Limits | `rate-limits/argocd-rate-limits.yml` |
| FinOps | `finops/argocd-finops.yml` |

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
