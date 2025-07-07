# Create replication controller using .yml file

```bash
kubectl create -f replication-controller.yml
```

```bash
kubectl apply -f replication-controller.yml
```

### Get replication controller

```bash
kubectl get replicationcontroller
```

### Delete replicaset and delete all underlying PODS

```bash
kubectl delete replicationcontroller <replication-controller-name>
```

### Scale replication controller

```bash
kubectl scale replicationcontroller <replication-controller-name> --replicas=<number-of-replic