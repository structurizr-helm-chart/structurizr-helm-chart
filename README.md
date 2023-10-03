# structurizr

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![AppVersion: 3077](https://img.shields.io/badge/AppVersion-3077-informational?style=flat-square)

The Structurizr Helm chart deploys Structurizr On premise flavor. Structurizr is a web-based rendering tool designed to help software development teams create software architecture diagrams and documentation.

## Values

| Key                                        | Type   | Default                                                                        | Description                                                          |
|--------------------------------------------|--------|--------------------------------------------------------------------------------|----------------------------------------------------------------------|
| affinity                                   | object | `{}`                                                                           |                                                                      |
| autoscaling.enabled                        | bool   | `false`                                                                        |                                                                      |
| autoscaling.maxReplicas                    | int    | `100`                                                                          |                                                                      |
| autoscaling.minReplicas                    | int    | `1`                                                                            |                                                                      |
| autoscaling.targetCPUUtilizationPercentage | int    | `80`                                                                           |                                                                      |
| fullnameOverride                           | string | `""`                                                                           |                                                                      |
| image.pullPolicy                           | string | `"IfNotPresent"`                                                               |                                                                      |
| image.repository                           | string | `"structurizr/onpremises"`                                                     |                                                                      |
| image.tag                                  | string | `""`                                                                           |                                                                      |
| imagePullSecrets                           | list   | `[]`                                                                           |                                                                      |
| ingress.annotations                        | object | `{}`                                                                           |                                                                      |
| ingress.className                          | string | `""`                                                                           |                                                                      |
| ingress.enabled                            | bool   | `false`                                                                        |                                                                      |
| ingress.hosts[0].host                      | string | `"structurizr.local"`                                                          |                                                                      |
| ingress.hosts[0].paths[0].path             | string | `"/"`                                                                          |                                                                      |
| ingress.hosts[0].paths[0].pathType         | string | `"ImplementationSpecific"`                                                     |                                                                      |
| ingress.tls                                | list   | `[]`                                                                           |                                                                      |
| nameOverride                               | string | `""`                                                                           |                                                                      |
| nodeSelector                               | object | `{}`                                                                           |                                                                      |
| persistence.VolumeName                     | string | `""`                                                                           |                                                                      |
| persistence.accessMode                     | string | `"ReadWriteOnce"`                                                              |                                                                      |
| persistence.annotations                    | object | `{}`                                                                           |                                                                      |
| persistence.enabled                        | bool   | `true`                                                                         | enable PVC mount/creation, required for the file storage             |
| persistence.existingClaim                  | string | `""`                                                                           | If defined, PVC must be created manually before volume will be bound |
| persistence.size                           | string | `"10Gi"`                                                                       | volume size                                                          |
| persistence.storageClass                   | string | `""`                                                                           | Storage class of PV to bind.                                         |
| persistence.subPath                        | string | `""`                                                                           |                                                                      |
| podAnnotations                             | object | `{}`                                                                           |                                                                      |
| podSecurityContext                         | object | `{}`                                                                           |                                                                      |
| replicaCount                               | int    | `1`                                                                            | Specify the number of replicas                                       |
| resources                                  | object | `{}`                                                                           |                                                                      |
| securityContext                            | object | `{}`                                                                           |                                                                      |
| service.port                               | int    | `8080`                                                                         |                                                                      |
| service.type                               | string | `"ClusterIP"`                                                                  |                                                                      |
| serviceAccount.annotations                 | object | `{}`                                                                           |                                                                      |
| serviceAccount.create                      | bool   | `true`                                                                         |                                                                      |
| serviceAccount.name                        | string | `""`                                                                           |                                                                      |
| structurizr_properties                     | string | `"# structurizr.url=https://localhost\n# structurizr.authentication=\"file\""` | content of the structurizr.properties file                           |
| tolerations                                | list   | `[]`                                                                           |                                                                      |
| volumeMounts                               | list   | `[]`                                                                           | Additional volumeMounts to the container                             |
| volumes                                    | list   | `[]`                                                                           | Additional volumes to the pod                                        |
| tomcat_server                              | string   | `""`                                                                            | Customize Tomcat Server configuration                                |
