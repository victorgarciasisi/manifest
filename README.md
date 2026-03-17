## Catálogo de manifests 


### Workloads básicos
- Pods: `pod-example.yml`
- Deployments: `deployment-example.yml`,  `deployment-nodeselector.yaml`, `deployment-healthcheck.yaml`

### Services e Ingress
- Services: `service-example.yml`, `service-ingress-example.yml`, `hpa-service.yaml`
- Ingress: `web-ingress-example.yaml`

### Batch
- `job-example.yaml`, `cronjob-example.yaml`

### Autoscaling
- `hpa-deployment.yaml`, `hpa.yaml`

### Storage
- PVC demo: `pvc-demo.yaml`, `pvc-pod-demo.yaml`

### Observabilidad 
- Prometheus/Alertmanager: `prometheus-*.yaml`, `alertmanager-*.yaml`, `alert-webhook-receiver.yaml`
- Grafana: `grafana-*.yaml`
- Loki/Promtail: `loki-*.yaml`, `promtail-*.yaml`
- Tempo/OTel: `tempo-*.yaml`, `otel-collector-*.yaml`, `otel-demo-values.yaml`
- ELK: `elastic-*.yaml`, `kibana-*.yaml`, `logstash-*.yaml`, `filebeat-sidecar-config.yaml`
