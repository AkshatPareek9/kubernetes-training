# namespace.yaml

```
  kubectl apply -f namespace.yaml
  kubectl get ns
```

# pod.yaml

```
  kubectl apply -f pod.yaml
  kubectl get pods -n nginx
```

# kubernetes debug command

```
  kubectl exec -it pod/nginx-pod -n nginx -- bash
  kubectl describe pod/nginx-pod -n nginx
```
