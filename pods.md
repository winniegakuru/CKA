## POD
#### Set Alias:
`alias k=kubectl`

#### Create a pod using command:
`kubectl run nginx --image=nginx`

#### Create a pod using command dry run to a file:
```
kubectl run nginx --image=nginx --dry-run=client
kubectl run nginx --image=nginx --dry-run=client -o yaml
kubectl run nginx --image=nginx --dry-run=client -o yaml > nginx-po.yaml
kubectl create deployment --image=nginx nginx --dry-run=client -o yaml > nginx-deployment.yaml
```

#### List all Pods:
`k get po`

#### Get pod's Image names:
`kubectl get pods -o=name`

#### Get pod's running Image(grep)
`kubectl get po -o jsonpath="{.items[*].spec.containers[*].image}"`

#### The longer option:
`k describe po nginx | grep image`

#### Get Node where the Pod is running:
`k get po -o wide`

#### Get the state of a container:
`k describe po webapp | grep State`

#### Delete a Pod:
`k delete po webapp`
