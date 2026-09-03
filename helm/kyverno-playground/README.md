# kyverno-playground

Kyverno Playground Web Application

**Homepage:** <https://github.com/giantswarm/kyverno-playground>

## Source Code

* <https://github.com/some-org/some-repo>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
|  | kyverno-playground | 0.10.5 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| nameOverride | string | `""` | Name override |
| fullnameOverride | string | `""` | Full name override |
| kyverno-playground.image.registry | string | `"gsoci.azurecr.io"` | Image registry |
| kyverno-playground.image.repository | string | `"giantswarm/kyverno-playground"` | Image repository |
| kyverno-playground.image.pullPolicy | string | `"IfNotPresent"` | Image pull policy |
| kyverno-playground.image.tag | string | `nil` | Image tag (will default to app version if not set) |
| kyverno-playground.nameOverride | string | `""` | Name override |
| kyverno-playground.fullnameOverride | string | `""` | Full name override |
| kyverno-playground.replicaCount | int | `1` | Number of pod replicas |
| kyverno-playground.tufRootMountPath | string | `"/.sigstore"` | A writable volume to use for the TUF root initialization. |
| kyverno-playground.imagePullSecrets | list | `[]` | Image pull secrets |
| kyverno-playground.priorityClassName | string | `""` | Priority class name |
| kyverno-playground.serviceAccount.create | bool | `true` | Create service account |
| kyverno-playground.serviceAccount.annotations | object | `{}` | Service account annotations |
| kyverno-playground.serviceAccount.name | string | `""` | Service account name (required if `serviceAccount.create` is `false`) |
| kyverno-playground.podAnnotations | object | `{}` | Pod annotations |
| kyverno-playground.podLabels | object | `{}` | Additional labels to add to each pod |
| kyverno-playground.global.labels | object | `{"application.giantswarm.io/team":"shield","giantswarm.io/service-type":"managed"}` | additional labels added on each resource |
| kyverno-playground.podSecurityContext | object | `{"fsGroup":2000}` | Pod security context |
| kyverno-playground.securityContext | object | See [values.yaml](values.yaml) | Container security context |
| kyverno-playground.service.type | string | `"ClusterIP"` | Service type |
| kyverno-playground.service.port | int | `8080` | Service port |
| kyverno-playground.livenessProbe | object | `{"httpGet":{"path":"/","port":"http"}}` | Liveness probe |
| kyverno-playground.readinessProbe | object | `{"httpGet":{"path":"/","port":"http"}}` | Readiness probe |
| kyverno-playground.ingress.enabled | bool | `false` | Enable ingress |
| kyverno-playground.ingress.className | string | `""` | Ingress class name |
| kyverno-playground.ingress.annotations | object | `{}` | Ingress annotations |
| kyverno-playground.ingress.hosts | list | `[]` | Ingress hosts |
| kyverno-playground.ingress.tls | list | `[]` | Ingress tls |
| kyverno-playground.networkPolicy.enabled | bool | `false` | Enable egress restriction for the playground pods |
| kyverno-playground.networkPolicy.allowClusterDNS | bool | `true` | Allow DNS to in-cluster CoreDNS while keeping app egress internet-only |
| kyverno-playground.clusterRoles | list | `[]` | Cluster roles |
| kyverno-playground.roles | list | `[]` | Cluster roles |
| kyverno-playground.httproute.enabled | bool | `false` | Enable HTTPRoute resource (Gateway API alternative to Ingress) Requires Gateway API CRDs (v1) installed in cluster https://gateway-api.sigs.k8s.io/ |
| kyverno-playground.httproute.labels | object | `{}` | Additional HTTPRoute labels |
| kyverno-playground.httproute.annotations | object | `{}` | Additional HTTPRoute annotations |
| kyverno-playground.httproute.parentRefs | list | `[]` | Gateway API parentRefs (list of Gateway references) Must reference an existing Gateway resource |
| kyverno-playground.httproute.hostnames | list | `[]` | List of hostnames for HTTPRoute |
| kyverno-playground.httproute.rules | list | `[{"matches":[{"path":{"type":"PathPrefix","value":"/"}}]}]` | HTTPRoute rules configuration Allows advanced routing with matches and filters |
| kyverno-playground.resources.limits | string | `nil` | Container resource limits |
| kyverno-playground.resources.requests | string | `nil` | Container resource requests |
| kyverno-playground.autoscaling.enabled | bool | `false` | Enable autoscaling |
| kyverno-playground.autoscaling.minReplicas | int | `1` | Min number of replicas |
| kyverno-playground.autoscaling.maxReplicas | int | `100` | Max number of replicas |
| kyverno-playground.autoscaling.targetCPUUtilizationPercentage | int | `80` | Target CPU utilisation |
| kyverno-playground.autoscaling.targetMemoryUtilizationPercentage | string | `nil` | Target Memory utilisation |
| kyverno-playground.nodeSelector | object | `{}` | Node selector |
| kyverno-playground.tolerations | list | `[]` | Tolerations |
| kyverno-playground.affinity | object | `{}` | Affinity |
| kyverno-playground.config.gin.mode | string | `"release"` | Gin mode (`release` or `debug`) |
| kyverno-playground.config.gin.cors | bool | `false` | Gin cors middleware |
| kyverno-playground.config.gin.logger | bool | `false` | Gin logger middleware |
| kyverno-playground.config.gin.maxBodySize | int | `2097152` | Gin max body size |
| kyverno-playground.config.cluster.enabled | bool | `false` | Enable connected cluster mode |
| kyverno-playground.config.ui.sponsor | string | `""` | Sponsor name |
| kyverno-playground.config.server.host | string | `"0.0.0.0"` | Server host |
| kyverno-playground.config.server.port | int | `8080` | Server port |
| kyverno-playground.config.engine.builtinCrds | list | `[]` | Builtin CRDs enabled (`argocd`, `cert-manager`, `prometheus-operator`, `tekton-pipelines`) |
| kyverno-playground.config.engine.localCrds | list | `[]` | Paths to folders containing yaml definitions for CRDs |
| kyverno-playground.config.versions | list | `[]` | list of additional Kyverno Playground versions |
| kyverno-playground.extraArgs | object | `{}` | Additonal container arguments |
| kyverno-playground.sponsor | string | `""` | Optional sponsor text |
| kyverno-playground.mcp.enabled | bool | `false` | Enable the MCP server deployment |
| kyverno-playground.mcp.replicaCount | int | `1` | Number of MCP server pod replicas |
| kyverno-playground.mcp.port | int | `8080` | MCP server port |
| kyverno-playground.mcp.service.type | string | `"ClusterIP"` | MCP service type |
| kyverno-playground.mcp.service.port | int | `8080` | MCP service port |
| kyverno-playground.mcp.ingress.enabled | bool | `false` | Enable MCP ingress |
| kyverno-playground.mcp.ingress.className | string | `""` | Ingress class name |
| kyverno-playground.mcp.ingress.annotations | object | `{}` | Ingress annotations |
| kyverno-playground.mcp.ingress.hosts | list | `[]` | Ingress hosts |
| kyverno-playground.mcp.ingress.tls | list | `[]` | Ingress tls |
| kyverno-playground.mcp.httproute.enabled | bool | `false` | Enable HTTPRoute resource (Gateway API alternative to Ingress) Requires Gateway API CRDs (v1) installed in cluster https://gateway-api.sigs.k8s.io/ |
| kyverno-playground.mcp.httproute.labels | object | `{}` | Additional HTTPRoute labels |
| kyverno-playground.mcp.httproute.annotations | object | `{}` | Additional HTTPRoute annotations |
| kyverno-playground.mcp.httproute.parentRefs | list | `[]` | Gateway API parentRefs (list of Gateway references) Must reference an existing Gateway resource |
| kyverno-playground.mcp.httproute.hostnames | list | `[]` | List of hostnames for HTTPRoute |
| kyverno-playground.mcp.httproute.rules | list | `[{"matches":[{"path":{"type":"PathPrefix","value":"/"}}]}]` | HTTPRoute rules configuration Allows advanced routing with matches and filters |
| kyverno-playground.mcp.resources | object | `{"limits":{},"requests":{}}` | MCP container resource limits/requests |
