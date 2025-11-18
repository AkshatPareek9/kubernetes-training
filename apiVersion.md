# apiVersion list

Which apiVersion should I use?

```
| Resource    | apiVersion |
| ----------- | ---------- |
| Deployment  | `apps/v1`  |
| StatefulSet | `apps/v1`  |
| DaemonSet   | `apps/v1`  |
| ReplicaSet  | `apps/v1`  |
| Pod         | `v1`       |


| Resource      | apiVersion             |
| ------------- | ---------------------- |
| Service       | `v1`                   |
| Ingress       | `networking.k8s.io/v1` |
| NetworkPolicy | `networking.k8s.io/v1` |

| Resource       | apiVersion |
| -------------- | ---------- |
| ConfigMap      | `v1`       |
| Secret         | `v1`       |
| ServiceAccount | `v1`       |

| Resource           | apiVersion                     |
| ------------------ | ------------------------------ |
| Role               | `rbac.authorization.k8s.io/v1` |
| ClusterRole        | `rbac.authorization.k8s.io/v1` |
| RoleBinding        | `rbac.authorization.k8s.io/v1` |
| ClusterRoleBinding | `rbac.authorization.k8s.io/v1` |

| Resource                    | apiVersion          |
| --------------------------- | ------------------- |
| PersistentVolume (PV)       | `v1`                |
| PersistentVolumeClaim (PVC) | `v1`                |
| StorageClass                | `storage.k8s.io/v1` |
| VolumeAttachment            | `storage.k8s.io/v1` |

| Resource                    | apiVersion                      |
| --------------------------- | ------------------------------- |
| HorizontalPodAutoscaler     | `autoscaling/v2` (recommended)  |
| VerticalPodAutoscaler (VPA) | `autoscaling.k8s.io/v1` (addon) |

| Resource | apiVersion |
| -------- | ---------- |
| Job      | `batch/v1` |
| CronJob  | `batch/v1` |

| Resource                 | apiVersion                |
| ------------------------ | ------------------------- |
| CustomResourceDefinition | `apiextensions.k8s.io/v1` |

| Resource    | apiVersion           |
| ----------- | -------------------- |
| Certificate | `cert-manager.io/v1` |
| Issuer      | `cert-manager.io/v1` |
```
