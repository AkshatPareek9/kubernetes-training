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
  kubectl get pods -n nginx
  kubectl delete -f deployment.yaml
```

