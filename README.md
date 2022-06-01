# jmeter-monitoring
A set of tools (influxdb, telegraf, grafana) with jmeter to monitor resources usage within a test plan. (Kubernetes)

# Quick start
```sh
docker compose -f ./docker/docker-compose.yaml build
kubectl apply -f ./manifests/grafana
kubectl apply -f ./manifests/influxdb
kubectl apply -f ./manifests/telegraf
```

```sh
kubectl delete -f ./manifests/grafana
kubectl delete -f ./manifests/influxdb
kubectl delete -f ./manifests/telegraf
```