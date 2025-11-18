# kubernetes-training

Kubernetes is an open-source platform that automates deploying, scaling, and managing containerized applications. It organizes containers into pods, handles load balancing, self-healing, and rolling updates, and provides a reliable, scalable environment for running modern cloud-native applications across clusters.

## Key components in Kubernetes:

  1. kubectl  : It gives the command to API Server
  2. API Server : It takes the request and respond accordingly - just like server for communication gateway.
  3. Scheduler : To schedule container/pods on Worker Nodes
  4. etcd : It is key-value pair database to store the information of master and worker nodes.
  5. Controller Manager : It is the manager for both master and worker nodes managing everything
  6. kubelet : Manages everything on Worker Node.
  7. Pods : It is smallest unit in kubernetes i.e Docker Container
  8. Server Proxy / kubeproxy : It is the service to provide access to the user to connect the container from outside.
  9. User : Person
  10. CNI Network : Network to create a communicate channel between the services of the Master and Worker Nodes.

## Architecture of Kubernetes

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/5cb32ace-eb25-42ce-9bdf-ced921905eb0" />  
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/7bcc58ca-5976-45aa-a2d4-ca6bd82375be" />

## Pre-requisite for Kubernetes Cluster Setup

**1. Kubernetes Core Packages**  

  **Local/Provisioning Tools** : kubeadm, minikube, kind  
  **Managed Kubernetes Services** : EKS, GKE, AKS

  *kubeadm* : install on production server to create kubernetes cluster.  
  *kind* : kubernetes in docker : install on docker container to create kubernetes cluster.  
  *minikube* : lightweight single node kubernetes means for learning and development purpose.  

**2. Docker container**  
  *Known Issue*  
    *Command: docker ps*  
    *Error: Permission denied*  
    *Resolution : sudo usermod -aG docker $USER && newgrp docker*  

**3. kubectl**  

## Setup Kubernetes Cluster

  Follow README.md under setup-cluster

## Namespace

  A unit in which all the resources are allocated to a group.

  ```
    kubectl get namespace
    kubectl get ns

    kubectl get pods
    Note: show the pods of default namespace

    kubectl get pods -n <namespace>
  ```

## Pod

  A Pod is the smallest deployable unit in Kubernetes.

### 🧠 Why does Kubernetes need Pods?

  Because Kubernetes does not manage containers directly. It manages Pods → Pods contain containers.
  
### Create Namespace and run the Pod

  ```
    # Creating namespace
    kubectl create ns nginx
    
    # run the pod
    kubectl run nginx-pod --image=nginx:latest --port=80 
    kubectl get pods

    # delete the pod
    kubectl delete pod nginx-pod

    # run the pod in the namespace nginx  
    kubectl run nginx-pod --image=nginx:latest --port=80 -n nginx
    kubectl get pods -n nginx

    # delete the pod in the namespace nginx
    kubectl delete pod nginx-pod -n nginx

    # delete the namespace
    kubectl delete ns nginx
  ```
