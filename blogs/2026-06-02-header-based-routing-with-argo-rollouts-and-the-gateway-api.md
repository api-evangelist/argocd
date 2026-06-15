---
title: "Header based routing with Argo Rollouts and the Gateway API"
url: "https://blog.argoproj.io/header-based-routing-with-argo-rollouts-and-the-gateway-api-777f9a1f614d"
date: "2026-06-02"
author: "Kostis Kapelonis"
feed_url: "https://medium.com/feed/argo-project"
---
A new Gateway API plugin release for Argo Rollouts adds header-based routing capabilities, enabling traffic to be routed to specific users or groups during canary deployments by matching HTTP headers rather than using random request-based traffic splitting. This supports scenarios where organizations want granular control over which users see new versions first, such as geographic targeting or QA-only preview access. The plugin uses the newly added "name" property in Gateway API 1.2 to manage routing rules more reliably, eliminating previous race conditions caused by ConfigMap-based tracking.
