# Kubernetes Hands-on Practice 🚀

A practical Kubernetes learning repository covering core Kubernetes objects, workload management, networking, configuration, resource management, and application exposure.

This repository contains hands-on YAML manifests, deployment examples, troubleshooting scenarios, and real-world use cases to understand how Kubernetes works in production environments.

## 📚 Learning Roadmap

### 01. Kubernetes Fundamentals

| No. | Topic | YAML File |
|---|---|---|
| 01 | Namespace | `01-namespace.yaml` |
| 02 | Pod | `02-pod.yaml` |
| 03 | Multi-Container Pods | `03-multi-container.yaml` |
| 04 | Labels and Selectors | `04-labels.yaml` |
| 05 | Error Handling and Troubleshooting | `05-errors.yaml` |
| 06 | Annotations | `06-annotation.yaml` |
| 07 | Resource Requests and Limits | `07-resources.yaml` |
| 08 | Environment Variables | `08-env.yaml` |

### 02. Kubernetes Networking – Services

Understanding how Kubernetes exposes applications and enables communication between different components.

| No. | Topic | YAML File |
|---|---|---|
| 09 | Kubernetes Services | `09-service.yaml` |
| 10 | ClusterIP Service | `10-clusterip.yaml` |
| 11 | NodePort Service | `11-nodeport.yaml` |
| 12 | LoadBalancer Service | `12-loadbalancer.yaml` |

**Service types:**

- **ClusterIP:** Exposes an application internally within the Kubernetes cluster.
- **NodePort:** Exposes an application through a port on each Kubernetes node.
- **LoadBalancer:** Exposes an application externally using a cloud-provider load balancer when supported.

### 03. Upcoming Kubernetes Topics

- Deployments and ReplicaSets
- ConfigMaps and Secrets
- Liveness, Readiness and Startup Probes
- Persistent Volumes (PV)
- Persistent Volume Claims (PVC)
- Storage Classes
- StatefulSets
- DaemonSets
- Jobs and CronJobs
- Ingress and Ingress Controllers
- Horizontal Pod Autoscaler (HPA)
- RBAC and Service Accounts
- Network Policies
- Helm Charts
- Kubernetes Troubleshooting

---

## 🛠️ Prerequisites

Before practising these examples, ensure you have:

- Kubernetes Cluster (EKS / Minikube / Kind)
- kubectl
- AWS CLI (for EKS)
- Basic YAML knowledge
- Docker fundamentals

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd K8ss
```

### 2. Verify Cluster Connectivity

```bash
kubectl cluster-info
kubectl get nodes
kubectl get namespaces
```

### 3. Apply Kubernetes Manifests

```bash
kubectl apply -f 01-namespace.yaml
kubectl apply -f 02-pod.yaml
```

Or apply all manifests in the directory:

```bash
kubectl apply -f .
```

**Note:** Apply manifests individually when learning. Applying everything together can create unwanted resources or dependency issues.

## 🔍 Useful kubectl Commands

### Pods

```bash
kubectl get pods
kubectl get pods -A
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl exec -it <pod-name> -- /bin/sh
```

### Namespaces

```bash
kubectl get namespaces
kubectl create namespace dev
kubectl get pods -n dev
```

### Labels and Selectors

```bash
kubectl get pods --show-labels
kubectl get pods -l app=nginx
kubectl describe pod <pod-name>
```

### Services

```bash
kubectl get services
kubectl get svc
kubectl describe svc <service-name>
kubectl get endpoints
kubectl get endpointslices
```

### Resources

```bash
kubectl get all
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl top nodes
kubectl top pods
```

## 🌐 Understanding Kubernetes Service Networking

A Kubernetes Service provides a stable network endpoint for accessing a group of Pods selected through labels.

### ClusterIP

Internal communication between applications inside the cluster.

Example:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-clusterip
spec:
  type: ClusterIP
  selector:
    app: nginx
  ports:
    - protocol: TCP
      port: 80
      targetPort: 80
```

### NodePort

Exposes an application through a port on the Kubernetes nodes.

```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-nodeport
spec:
  type: NodePort
  selector:
    app: nginx
  ports:
    - protocol: TCP
      port: 80
      targetPort: 80
      nodePort: 30080
```

### LoadBalancer

Creates an externally accessible load balancer through a supported cloud integration.

```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-loadbalancer
spec:
  type: LoadBalancer
  selector:
    app: nginx
  ports:
    - protocol: TCP
      port: 80
      targetPort: 80
```

**Important:** In AWS EKS, a LoadBalancer Service can provision an AWS load balancer depending on the installed cloud integration and configuration. A cloud load balancer is not automatically created in every local Kubernetes cluster.

## 🧪 Troubleshooting Practice

Kubernetes troubleshooting is an important part of this repository.

Common errors to investigate:

| Error | Possible Cause |
|---|---|
| ImagePullBackOff | Invalid image name or image pull failure |
| ErrImagePull | Unable to pull container image |
| CrashLoopBackOff | Container repeatedly exits |
| CreateContainerConfigError | Invalid container configuration |
| Pending | Insufficient resources or scheduling constraints |
| OOMKilled | Container exceeded memory limit |
| FailedScheduling | Pod cannot be scheduled on available nodes |

Useful troubleshooting commands:

```bash
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl logs <pod-name> --previous
kubectl get events
kubectl get pods -o wide
```

## 🎯 Repository Objective

The objective of this repository is to develop practical Kubernetes administration and troubleshooting skills through hands-on implementation.

The learning progression follows:

**Kubernetes Fundamentals → Workloads → Networking → Configuration → Storage → Security → Scaling → Production Deployments**

Rather than focusing only on theoretical concepts, each topic is practised using Kubernetes YAML manifests and kubectl commands.

## 📈 Progress Tracker

- [x] Namespace
- [x] Pods
- [x] Multi-Container Pods
- [x] Labels and Selectors
- [x] Error Handling
- [x] Annotations
- [x] Resource Requests and Limits
- [x] Environment Variables
- [ ] Services
- [ ] ClusterIP
- [ ] NodePort
- [ ] LoadBalancer
- [ ] Deployments and ReplicaSets
- [ ] ConfigMaps and Secrets
- [ ] Probes
- [ ] Persistent Storage
- [ ] Ingress
- [ ] Autoscaling
- [ ] RBAC
- [ ] Helm
- [ ] Production-level deployments

---

**Author:** Kubernetes Hands-on Practice

**Focus Areas:** Kubernetes | Docker | AWS | EKS | YAML | DevOps | Container Orchestration

⭐ If you find this repository useful, feel free to explore, fork, and practise along with the examples.
