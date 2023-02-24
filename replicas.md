## Replicasets

Replication controller helps us run multiple instances of the same controller/pod (HA) 
ensures the required number of pods are running always

Sample RS manifest:
```
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: frontend
  labels:
    app: guestbook
    tier: frontend
spec:
  # modify replicas according to your case
  replicas: 3
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: php-redis
        image: gcr.io/google_samples/gb-frontend:v3
```

### commands
```
k create -f rs.yaml
k get rs
k delete rs new-rs
k replace -f rs.yaml # - to update the replicaset
k scale -replicas=6 -f rs.yaml
kubectl scale rs new-replica-set --replicas=2
```
