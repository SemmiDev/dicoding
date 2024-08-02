```
kubectl apply -f pod.yaml
kubectl get pods
kubectl port-forward pod/hello-kubernetes 8080:8080
curl localhost:8080
```

```
kubectl create configmap nginx-config --from-file=nginx.conf
kubectl port-forward multi-container-pod 8080:80
```
