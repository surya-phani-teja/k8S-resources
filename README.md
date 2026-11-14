# ☸️ Kubernetes Hands-on Practice | k8S-resources

<p align="center">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/Amazon_EKS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/YAML-CB171E?style=for-the-badge&logo=yaml&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</p>

## 🚀 About This Repository

Welcome to my Kubernetes hands-on practice repository!

This repository contains practical Kubernetes YAML manifests covering core Kubernetes concepts, workload management, application configuration, networking and service exposure.

I created these resources while learning Kubernetes and working with Amazon Elastic Kubernetes Service (EKS).

**My goal is to strengthen my practical DevOps skills through hands-on implementation, troubleshooting and real-world scenarios.**

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| ☸️ Kubernetes | Container orchestration |
| ☁️ Amazon EKS | Managed Kubernetes |
| 🐳 Docker | Containerization |
| 📄 YAML | Resource configuration |
| 💻 Linux | Command-line operations |
| 🔧 kubectl | Kubernetes management |
| 🐙 Git & GitHub | Version control |

---

## 📚 Learning Modules

### 🔹 01. Kubernetes Fundamentals

| File | Topic |
|---|---|
| `01-namespace.yaml` | Namespace Management |
| `02-pod.yaml` | Pod Creation |
| `03-multi-container.yaml` | Multi-container Pods |
| `04-lables.yaml` | Labels and Selectors |
| `05-errors.yaml` | Error Handling |
| `06-annotation.yaml` | Annotations |

### 🔹 02. Resource Management & Configuration

| File | Topic |
|---|---|
| `07-resources.yaml` | CPU and Memory Resources |
| `08-env.yaml` | Environment Variables |
| `09-configmap.yaml` | ConfigMap Creation |
| `10-podconfig.yaml` | ConfigMap Integration |
| `11-secretes.yaml` | Kubernetes Secrets |
| `12-podsecret.yaml` | Secret Integration |

### 🔹 03. Kubernetes Networking & Services

| File | Topic |
|---|---|
| `13-service.yaml` | Kubernetes Services |
| `14-podService.yaml` | Pod and Service Configuration |
| `15-nodeservice.yaml` | NodePort Service |
| `16-podnodeport.yaml` | Pod with NodePort |
| `17-service-lb.yaml` | LoadBalancer Service |
| `18-podlb.yaml` | Pod with LoadBalancer |

---

## ⚙️ Practical Implementation

Some of the hands-on activities covered in this repository:

- Creating and managing Kubernetes namespaces.
- Deploying single-container and multi-container Pods.
- Working with labels and annotations.
- Configuring CPU and memory requests and limits.
- Managing application configurations using ConfigMaps and Secrets.
- Exposing applications through ClusterIP, NodePort and LoadBalancer.
- Deploying Nginx applications on Amazon EKS.
- Accessing applications through AWS LoadBalancer DNS.
- Troubleshooting Kubernetes YAML and networking issues.

---

## 💻 Getting Started

**Prerequisites**

- AWS Account
- Amazon EKS Cluster
- AWS CLI
- kubectl
- Basic Linux and Docker knowledge

**Clone the repository**

```bash
git clone https://github.com/surya-phani-teja/k8S-resources.git
```

**Navigate to the repository**

```bash
cd k8S-resources
```

**Deploy a Kubernetes resource**

```bash
kubectl apply -f 02-pod.yaml
```

**Verify resources**

```bash
kubectl get pods -A
kubectl get svc -A
kubectl get nodes -o wide
```

---

## 🔍 Useful Kubernetes Commands

| Command | Description |
|---|---|
| `kubectl get pods -A` | List all Pods |
| `kubectl get svc -A` | List all Services |
| `kubectl get nodes -o wide` | View worker nodes |
| `kubectl get namespaces` | List Namespaces |
| `kubectl describe pod <name>` | Inspect a Pod |
| `kubectl logs <pod-name>` | View container logs |
| `kubectl get configmaps -A` | List ConfigMaps |
| `kubectl get secrets -A` | List Secrets |
| `kubectl top pods -A` | View Pod resource usage |
| `kubectl delete -f filename.yaml` | Delete resources |

---

## 🎯 Learning Objectives

My focus areas:

- Understanding Kubernetes architecture.
- Managing workloads and resource configurations.
- Implementing application networking.
- Understanding service discovery.
- Deploying applications on Amazon EKS.
- Troubleshooting Kubernetes workloads.
- Building practical cloud and DevOps experience.

---

## 🚧 Upcoming Learning

More Kubernetes concepts will be added as I progress:

- [ ] Deployments and ReplicaSets
- [ ] StatefulSets and DaemonSets
- [ ] Persistent Volumes and Claims
- [ ] Ingress Controllers
- [ ] Horizontal Pod Autoscaler (HPA)
- [ ] Helm Charts
- [ ] Kubernetes RBAC
- [ ] Monitoring and Logging

---

## 👨‍💻 Author

**Surya Phani Teja**

🔗 GitHub: [surya-phani-teja](https://github.com/surya-phani-teja)

📂 Repository: [k8S-resources](https://github.com/surya-phani-teja/k8S-resources)

---

<p align="center">
  <b>🚀 Learn • Practice • Break • Troubleshoot • Improve</b>
  <br/>
  <i>Building practical DevOps skills, one deployment at a time.</i>
</p>