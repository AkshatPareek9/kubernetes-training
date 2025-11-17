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
  **Managed Kubernetes Services** : EKS, GKE, AKS → Managed Kubernetes Services

  *kubeadm* : install on production server to create kubernetes cluster.  
  *kind* : kubernetes in docker : install on docker container to create kubernetes cluster.  
  *minikube* : lightweight single node kubernetes means for learning and development purpose.  

