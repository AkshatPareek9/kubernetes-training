# Create cluster using kind

  1. Create kind-cluster.yaml file
     
  2. Run the create cluster command using config file
  ```
    kind create cluster --name my-kind-cluster --config kind-cluster.yaml
  ```

  3. Verify kind cluster
  ```
    kubectl cluster-info --context kind-my-kind-cluster
    kubectl get nodes
  ```

# Create cluster using minikube

  1. Minikube create the cluster directly using below command.
  ```
    minikube start --driver=docker --vm=true --cpus=4 --memory=4096
  ```

  2. Verify minikube cluster
  ```
    kubectl get nodes
  ```

# Switch between the cluster context

  1. To show the nodes of the particular context
  ```
    kubectl get nodes --context kind-my-kind-cluster
  ```

  2. To change the context
  ```
    kubectl config use-context kind-my-kind-cluster
    kubectl get nodes
  ```
