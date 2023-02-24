## Replicasets

Replication controller helps us run multiple instances of the same controller/pod (HA) 
ensures the required number of pods are running always

```
k create -f rs.yaml
k get rs
k delete rs new-rs
k replace -f rs.yaml # - to update the replicaset
k scale -replicas=6 -f rs.yaml
kubectl scale rs new-replica-set --replicas=2
```
