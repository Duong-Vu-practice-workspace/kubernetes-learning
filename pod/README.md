# Create pod using .yml file

```bash
kubectl apply -f pod.yml
```

# Create pod
```bash
kubectl run my-pod --image=nginx
```

# Show all pods
```bash
kubectl get pods
```
# Delete pod
```bash
kubectl delete pod my-pod
```
# Show pod details
```bash
kubectl describe pod my-pod
```