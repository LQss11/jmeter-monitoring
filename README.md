# jmeter-monitoring
A set of tools (influxdb, telegraf, grafana) with jmeter to monitor resources usage within a test plan. (Kubernetes)

# Quick start
```sh
docker compose -f ./docker/docker-compose.yaml build
kubectl apply -f ./manifests/grafana
kubectl apply -f ./manifests/influxdb
kubectl apply -f ./manifests/telegraf
kubectl apply -f ./manifests/jmeter
```
Start test
```sh
kubectl exec -it deployment/jmeter -- sh -c "echo 'google' | /data/scripts/run.sh"
```
Copy data inside jmx
```sh
kubectl cp ./file.jmx podname:/data/jmx
```  
```sh
kubectl delete -f ./manifests/grafana
kubectl delete -f ./manifests/influxdb
kubectl delete -f ./manifests/telegraf
kubectl apply -f ./manifests/jmeter
```