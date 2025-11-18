# namespace.yaml

```
  kubectl apply -f namespace.yaml
  kubectl get ns
  kubectl delete -f namespace.yaml
```

# pod.yaml

```
  kubectl apply -f pod.yaml
  kubectl get pods -n nginx
  kubectl delete -f pod.yaml
```

# kubernetes debug command

```
  kubectl exec -it pod/nginx-pod -n nginx -- bash
  kubectl describe pod/nginx-pod -n nginx
```

# deployment.yaml

```
  kubectl apply -f deployment.yaml
  kubectl get deployment -n nginx
  kubectl get pods -n nginx -o wide
  kubectl delete -f deployment.yaml
```

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/f246c960-8d1e-4121-9f37-ec2242ac6736" />

## Create the replicas of the deployment

```
  kubectl scale deployment/nginx-deployment -n nginx --replicas=3
  kubectl get pods -n nginx -o wide
```

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/49026e92-d1ee-4e2d-98be-e0500ce46d74" />

# replicasets.yaml

```
  kubectl apply -f replicasets.yaml
  kubectl get replicasets -n nginx
  kubectl get pods -n nginx -o wide
  kubectl delete -f replicasets.yaml
```

# daemonsets.yaml

```
  kubectl apply -f daemonsets.yaml
  kubectl get pods -n nginx -o wide
  kubectl delete -f daemonsets.yaml
```
