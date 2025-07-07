# ReplicaSet in Kubernetes

A **ReplicaSet** ensures that a specified number of pod replicas are running at any given time. It is commonly used to maintain the desired state of application instances.

## Key Features

- Ensures high availability by maintaining pod replicas
- Supports scaling up and down
- Works with Deployments for rolling updates

## Example ReplicaSet YAML

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
    name: example-replicaset
spec:
    replicas: 3
    selector:
        matchLabels:
            app: my-app
    template:
        metadata:
            labels:
                app: my-app
        spec:
            containers:
            - name: my-container
              image: nginx
```

## Common Commands

- **Create a ReplicaSet:**
    ```sh
    kubectl apply -f replicaset.yaml
    ```
- **Get all ReplicaSets:**
    ```sh
    kubectl get replicasets
    ```
- **Get details of a specific ReplicaSet:**
    ```sh
    kubectl get replicaset <name> -o yaml
    ```
- **Delete a ReplicaSet:**
    ```sh
    kubectl delete replicaset <name>
    ```
- **Replace (update) a ReplicaSet:**
    ```sh
    kubectl replace -f replicaset.yaml
    ```
- **Scale a ReplicaSet:**
    ```sh
    kubectl scale replicaset <name> --replicas=<number>
    ```

## References

- [Kubernetes ReplicaSet Documentation](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/)