# Create cluster using kind

  1. Create kind-cluster.yaml file
  2. Run the create cluster command using config file

  ```
    kind create cluster --name my-kind-cluster --config kind-cluster.yaml
  ```

  ### Verify kind cluster

  ```
    kubectl cluster-info --context kind-my-kind-cluster
    kubectl get nodes
  ```

# Create cluster using minikube

  1. Minikube create the cluster directly using below command.

  ```
    minikube start --driver=docker --vm=true --cpus=4 --memory=4096
  ```
