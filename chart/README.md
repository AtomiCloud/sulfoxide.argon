# atomi-kyverno

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.7.5](https://img.shields.io/badge/AppVersion-2.7.5-informational?style=flat-square)

AtomiCloud's Wrapper chart to deploy Kyverno

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://kyverno.github.io/kyverno/ | kyverno | 2.7.5 |
| https://kyverno.github.io/policy-reporter | policy-reporter | 2.19.4 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| kyverno.config.webhooks[0].namespaceSelector.matchExpressions[0].key | string | `"kubernetes.io/metadata.name"` |  |
| kyverno.config.webhooks[0].namespaceSelector.matchExpressions[0].operator | string | `"NotIn"` |  |
| kyverno.config.webhooks[0].namespaceSelector.matchExpressions[0].values[0] | string | `"kube-system"` |  |
| kyverno.config.webhooks[0].namespaceSelector.matchExpressions[0].values[1] | string | `"kube-node-lease"` |  |
| kyverno.config.webhooks[0].namespaceSelector.matchExpressions[0].values[2] | string | `"kube-public"` |  |
| kyverno.config.webhooks[0].namespaceSelector.matchExpressions[0].values[3] | string | `"kyverno"` |  |
| kyverno.customLabels."atomi.cloud/landscape" | string | `"pichu"` |  |
| kyverno.customLabels."atomi.cloud/layer" | string | `"1"` |  |
| kyverno.customLabels."atomi.cloud/module" | string | `"operator"` |  |
| kyverno.customLabels."atomi.cloud/platform" | string | `"systems"` |  |
| kyverno.customLabels."atomi.cloud/service" | string | `"policy-engine"` |  |
| kyverno.podAnnotations."atomi.cloud/landscape" | string | `"pichu"` |  |
| kyverno.podAnnotations."atomi.cloud/layer" | string | `"1"` |  |
| kyverno.podAnnotations."atomi.cloud/module" | string | `"operator"` |  |
| kyverno.podAnnotations."atomi.cloud/platform" | string | `"systems"` |  |
| kyverno.podAnnotations."atomi.cloud/service" | string | `"policy-engine"` |  |
| kyverno.replicaCount | int | `3` |  |
| kyverno.resources.limits.cpu | int | `1` |  |
| kyverno.resources.limits.memory | string | `"1Gi"` |  |
| kyverno.resources.requests.cpu | string | `"100m"` |  |
| kyverno.resources.requests.memory | string | `"128Mi"` |  |
| kyverno.templating.enabled | bool | `false` |  |
| kyverno.topologySpreadConstraints[0].labelSelector.matchLabels."atomi.cloud/module" | string | `"operator"` |  |
| kyverno.topologySpreadConstraints[0].labelSelector.matchLabels."atomi.cloud/service" | string | `"policy-engine"` |  |
| kyverno.topologySpreadConstraints[0].maxSkew | int | `1` |  |
| kyverno.topologySpreadConstraints[0].topologyKey | string | `"topology.kubernetes.io/zone"` |  |
| kyverno.topologySpreadConstraints[0].whenUnsatisfiable | string | `"ScheduleAnyway"` |  |
| policy-reporter.podAnnotations."atomi.cloud/landscape" | string | `"pichu"` |  |
| policy-reporter.podAnnotations."atomi.cloud/layer" | string | `"1"` |  |
| policy-reporter.podAnnotations."atomi.cloud/module" | string | `"reporter"` |  |
| policy-reporter.podAnnotations."atomi.cloud/platform" | string | `"systems"` |  |
| policy-reporter.podAnnotations."atomi.cloud/service" | string | `"policy-engine"` |  |
| policy-reporter.podLabels."atomi.cloud/landscape" | string | `"pichu"` |  |
| policy-reporter.podLabels."atomi.cloud/layer" | string | `"1"` |  |
| policy-reporter.podLabels."atomi.cloud/module" | string | `"reporter"` |  |
| policy-reporter.podLabels."atomi.cloud/platform" | string | `"systems"` |  |
| policy-reporter.podLabels."atomi.cloud/service" | string | `"policy-engine"` |  |
| policy-reporter.resources.limits.cpu | int | `1` |  |
| policy-reporter.resources.limits.memory | string | `"1Gi"` |  |
| policy-reporter.resources.requests.cpu | string | `"100m"` |  |
| policy-reporter.resources.requests.memory | string | `"128Mi"` |  |
| policy-reporter.topologySpreadConstraints[0].labelSelector.matchLabels."atomi.cloud/module" | string | `"reporter"` |  |
| policy-reporter.topologySpreadConstraints[0].labelSelector.matchLabels."atomi.cloud/service" | string | `"policy-engine"` |  |
| policy-reporter.topologySpreadConstraints[0].maxSkew | int | `1` |  |
| policy-reporter.topologySpreadConstraints[0].topologyKey | string | `"topology.kubernetes.io/zone"` |  |
| policy-reporter.topologySpreadConstraints[0].whenUnsatisfiable | string | `"ScheduleAnyway"` |  |
| policy-reporter.ui.enabled | bool | `true` |  |
| policy-reporter.ui.podAnnotations."atomi.cloud/landscape" | string | `"pichu"` |  |
| policy-reporter.ui.podAnnotations."atomi.cloud/layer" | string | `"1"` |  |
| policy-reporter.ui.podAnnotations."atomi.cloud/module" | string | `"ui"` |  |
| policy-reporter.ui.podAnnotations."atomi.cloud/platform" | string | `"systems"` |  |
| policy-reporter.ui.podAnnotations."atomi.cloud/service" | string | `"policy-engine"` |  |
| policy-reporter.ui.podLabels."atomi.cloud/landscape" | string | `"pichu"` |  |
| policy-reporter.ui.podLabels."atomi.cloud/layer" | string | `"1"` |  |
| policy-reporter.ui.podLabels."atomi.cloud/module" | string | `"ui"` |  |
| policy-reporter.ui.podLabels."atomi.cloud/platform" | string | `"systems"` |  |
| policy-reporter.ui.podLabels."atomi.cloud/service" | string | `"policy-engine"` |  |
| policy-reporter.ui.resources.limits.cpu | int | `1` |  |
| policy-reporter.ui.resources.limits.memory | string | `"1Gi"` |  |
| policy-reporter.ui.resources.requests.cpu | string | `"100m"` |  |
| policy-reporter.ui.resources.requests.memory | string | `"128Mi"` |  |
| serviceTree.cluster | string | `"opal"` |  |
| serviceTree.landscape | string | `"pichu"` |  |
| serviceTree.layer | string | `"1"` |  |
| serviceTree.module | string | `"operator"` |  |
| serviceTree.platform | string | `"systems"` |  |
| serviceTree.service | string | `"policy-engine"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.1](https://github.com/norwoodj/helm-docs/releases/v1.11.1)