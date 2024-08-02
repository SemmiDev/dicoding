```
kubectl apply -f pod.yaml
kubectl apply -f service.yaml
kubectl run -it --rm --image=busybox temp -- sh
wget -qO- http://nginx-service
```
