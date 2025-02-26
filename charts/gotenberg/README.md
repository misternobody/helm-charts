# gotenberg

Gotenberg is a Docker-powered stateless API for converting HTML, Markdown and Office documents to PDF.
5.0.0
[![Artifact HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/kurt108)](https://artifacthub.io/packages/search?repo=kurt108)

=======

## Versions

* 2.x: Gotenberg 6
* 3.x: Gotenberg 7, K8s Version >=1.19
* 4.x: Gotenberg 7, Fixed Ingress Warnings
* 5.x: Gotenberg 7, PDB and VPA

## Installing the Chart

```console
$ helm repo add kurt108 https://kurt108.github.io/helm-charts
"kurt108" has been added to your repositories
$ helm repo update
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "kurt108" chart repository
...
Update Complete. ⎈ Happy Helming!⎈
$ helm install my-release kurt108/gotenberg
NAME: my-release
...
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| annotations | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `1` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| basicAuth.enabled | bool | `false` |  |
| basicAuth.passwordMD5 | string | `"$apr1$zQ7F0fKS$X3aXkUCufHQlVe51VWUKu1"` |  |
| basicAuth.username | string | `"convert"` |  |
| env.open.GOTENBERG_VERSION | string | `"7.0.3"` |  |
| env.open.LOG_FORMAT | string | `"TEXT"` |  |
| env.open.LOG_LEVEL | string | `"DEBUG"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"gotenberg/gotenberg"` |  |
| image.tag | string | `"7.0.3"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0].host | string | `"gotenberg.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
| nodeSelector | object | `{}` |  |
| podDisruptionBudget.enabled | bool | `false` |  |
| podDisruptionBudget.maxUnavailable | int | `1` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| service.port | int | `3000` |  |
| service.type | string | `"ClusterIP"` |  |
| tolerations | list | `[]` |  |
| verticalAutoscaling.enabled | bool | `false` |  |
| verticalAutoscaling.minAllowed | string | `"50m"` |  |
