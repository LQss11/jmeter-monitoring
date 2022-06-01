# jmeter-monitoring
A set of tools (influxdb, telegraf, grafana) with jmeter to monitor resources usage within a test plan. (Kubernetes)

# Quick start
```sh
docker compose -f ./docker/docker-compose.yaml build
kubectl apply -f ./grafana
kubectl apply -f ./influxdb
kubectl apply -f ./telegraf
```

```sh
kubectl delete -f ./grafana
kubectl delete -f ./influxdb
kubectl delete -f ./telegraf
```