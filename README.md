## minikube start

```
minikube start --driver=virtualbox
minikube status
```

## apply

```
kubectl apply -f deployment_vote.yaml
kubectl apply -f service_vote.yaml
kubectl apply -f deployment_result.yaml
kubectl apply -f service_result.yaml
kubectl apply -f deployment_db.yaml
kubectl apply -f service_db.yaml
kubectl apply -f deployment_redis.yaml
kubectl apply -f service_redis.yaml

kubectl apply -f deployment_worker.yaml

```

## confirmation 　

```
watch 'kubectl get pod,svc,ingress,replicaset,deployment -o wide'
```

## get IP from ingress

```
kubectl get ingress -o=jsonpath='{.items[0].status.loadBalancer.ingress[0].ip}'
```

## delete

```
kubectl delete --all deployments --namespace=default
kubectl delete --all services --namespace=default
kubectl delete --all ingress --namespace=default
```
