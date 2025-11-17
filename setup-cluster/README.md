# Create cluster using kind

  ```
    kind create cluster --name my-kind-cluster --config kind-cluster.yaml
  ```

  ### Verify kind cluster

  ```
    kubectl cluster-info --context kind-my-kind-cluster
    kubectl get nodes
  ```
