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
  kubectl logs pod/nginx-pod -n nginx
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
  kubectl get daemonset -n nginx -o wide
  kubectl get pods -n nginx -o wide
  kubectl delete -f daemonsets.yaml
```

# configmap.yaml

```
  kubectl apply -f configmap.yaml
  kubectl get configmap -n mysql -o wide
```

# secret.yaml

```
  kubectl apply -f secret.yaml
  kubectl get secret -n mysql -o wide
```

# statefulset-namespace.yaml

```
  kubectl apply -f statefulset-namespace.yaml
  kubectl get ns
```

# statefulset.yaml

```
  kubectl apply -f statefulset.yaml
  kubectl get pods -n mysql -o wide
  kubectl delete -f statefulset.yaml

  # for go inside mysql container
  kubectl exec -it mysql-stateful-0 -n mysql -- bash
```

# jobs.yaml

```
  kubectl apply -f jobs.yaml
  kubectl get job -n nginx -o wide
  kubectl delete -f jobs.yaml
```

# cronjobs.yaml

```
  kubectl apply -f cronjob.yaml
  kubectl get cronjob -n nginx -o wide
  kubectl delete -f cronjob.yaml
```

# persistentvolume.yaml

```
  kubectl apply -f persistentvolume.yaml
  kubectl get pv
  kubectl delete -f persistentvolume.yaml
```

# persistentvolumeclaim.yaml

```
  kubectl apply -f persistentvolumeclaim.yaml
  kubectl get pvc
  kubectl delete -f persistentvolumeclaim.yaml
```

# Add the volume to the deployment and again apply the deployment.yaml

```
  kubectl apply -f deployment.yaml
  kubectl get deployment -n nginx
  kubectl get pods -n nginx -o wide
  kubectl delete -f deployment.yaml
```

# service.yaml

```
  kubectl apply -f service.yaml
  kubectl get service -n nginx
  kubectl delete -f service.yaml
```

# Add forwarding port to access the pod using service from outside
  Browser: https://localhost:80 
  Error: Not working
  Reason: Cluster is docker container. We have to forward the port of docker container. Need to expose the ip address.

```
  kubectl port-forward service/nginx-service -n nginx 80:80 --address=0.0.0.0

  If permission denied then:
  sudo -E kubectl port-forward service/nginx-service -n nginx 80:80 --address=0.0.0.0
```

# ingress.yaml

Apply nginx-ingress-controller
```
kubectl apply -f https://kind.sigs.k8s.io/examples/ingress/deploy-ingress-nginx.yaml

kubectl get ns
# o/p: ingress-nginx | ACTIVE

kubectl get svc -n ingress-nginx
# o/p: ingress-nginx-controller | Type=LoadBalancer | ClusterIP = x.x.x.x
```

```
  kubectl apply -f ingress.yaml
  kubectl get ingress -n nginx
  kubectl delete -f ingress.yaml
```

# Add forwarding port to expose ingress-nginx-controller (service)

```
  sudo -E kubectl port-forward service/ingress-nginx-controller -n ingress-nginx 8080:80 --address=0.0.0.0
```

  on browser:  
    https://localhost:8080/nginx  
    https://localhost:8080/

# hpa.yaml

```
  kubectl apply -f hpa.yaml
  kubectl get hpa -n nginx
  kubectl delete -f hpa.yaml
```

# vpa.yaml

```
  kubectl apply -f vpa.yaml
  kubectl get vpa -n nginx
  kubectl delete -f vpa.yaml
```
