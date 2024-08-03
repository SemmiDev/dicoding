```shell
kubectl scale deployment nginx-deployment --replicas=5
kubectl rollout undo deployment nginx-deployment
kubectl rollout history deployment nginx-deployment
kubectl rollout status deployment nginx-deployment

# history di detect ketika kita mengubah image
```
