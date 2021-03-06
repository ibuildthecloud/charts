## Configuration

Parameter | Description | Default
--- | --- | ---
`routePrefix` | Prefix used to register routes | `"/"`
`auth.anonymous.enabled` | If true, enable anonymous authentication | `true`
`adminUser` | Grafana admin user name | `admin`
`adminPassword` | Grafana admin user password | `admin`
`image.repository` | Image | `grafana/grafana`
`image.tag` | Image tag | `4.4.1`
`extraVars` | Pass extra environment variables to the Grafana container. | `{}`
`grafanaWatcher.repository` | Image | `quay.io/coreos/grafana-watcher`
`grafanaWatcher.tag` | Image tag | `v0.0.8`
`ingress.enabled` | If true, Grafana Ingress will be created | `false`
`ingress.annotations` | Annotations for Grafana Ingress | `{}`
`ingress.labels` | Labels for Grafana Ingress | `{}`
`ingress.hosts` | Grafana Ingress fully-qualified domain names | `[]`
`ingress.tls` | TLS configuration for Grafana Ingress | `[]`
`nodeSelector` | Node labels for pod assignment | `{}`
`resources` | Pod resource requests & limits | `{}`
`service.annotations` | Annotations to be added to the Grafana Service | `{}`
`service.clusterIP` | Cluster-internal IP address for Grafana Service | `""`
`service.externalIPs` | List of external IP addresses at which the Grafana Service will be available | `[]`
`service.loadBalancerIP` | External IP address to assign to Grafana Service | `""`
`service.loadBalancerSourceRanges` | List of client IPs allowed to access Grafana Service | `[]`
`service.nodePort` | Port to expose Grafana Service on each node | `30902`
`service.type` | Grafana Service type | `ClusterIP`
`storageSpec` | Grafana StorageSpec for persistent data | `{}`

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart. For example,

> **Tip**: You can use the default [values.yaml](values.yaml)

> **Tip**: On GCE If you want to  use  `Ingress.enabled=true`, you must put `service.type=NodePort`
