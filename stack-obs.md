# STACK OBS

## ISNTALL LOKI + GRAFANA

```bash 
kubectl create namespace logging-demo

kubectl apply -f loki-config.yaml
kubectl apply -f loki-deployment-service.yaml
kubectl apply -f loki-ingress.yaml
kubectl apply -f alloy-config.yaml
kubectl apply -f alloy-rbac.yaml
kubectl apply -f alloy-daemonset.yaml
kubectl apply -f pod-logger-1.yaml
kubectl apply -f grafana-datasources.yaml
kubectl apply -f grafana-deployment-service.yaml
kubectl apply -f grafana-ingress.yaml

kubectl get pods -A
kubectl get ingress -A
```


## INSTALL PROMETHEUS + ALERTMANAGER + GRAFANA

```bash 
kubectl create namespace monitoring-demo

kubectl apply -f alert-webhook-receiver.yaml
kubectl apply -f alertmanager-config.yaml
kubectl apply -f alertmanager-deployment-service.yaml
kubectl apply -f alertmanager-ingress.yaml
kubectl apply -f prometheus-config.yaml
kubectl apply -f prometheus-rbac.yaml
kubectl apply -f prometheus-deployment-service.yaml
kubectl apply -f prometheus-ingress.yaml
kubectl apply -f node-exporter-daemonset.yaml
kubectl apply -f kube-state-metrics.yaml
kubectl apply -f prometheus-rules.yaml
kubectl apply -f grafana-datasources-v2.yaml
kubectl apply -f fake-target.yaml
kubectl apply -f crashloop-pod.yaml
kubectl apply -f disk-filler-pod.yaml

kubectl -n logging-demo delete pod -l app=grafana
kubectl -n monitoring-demo delete pod -l app=prometheus

kubectl get pods -A
kubectl get ingress -A
```


## INSTALL OPENTELEMETRY + TEMPO + GRAFANA

```bash 
kubectl create namespace tracing-demo
kubectl create namespace apps-demo

kubectl apply -f tempo-config.yaml
kubectl apply -f tempo-deployment-service.yaml
kubectl apply -f otel-collector-config.yaml
kubectl apply -f otel-collector-deployment-service.yaml
kubectl apply -f mongo-tracing.yaml
kubectl apply -f flask-tracing-app.yaml
kubectl apply -f flask-tracing-ingress.yaml
kubectl apply -f grafana-datasources-v3.yaml

kubectl -n logging-demo delete pod -l app=grafana

kubectl get pods -A
kubectl get ingress -A
```
