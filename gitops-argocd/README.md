# GitOps with ArgoCD and Helm

This repository demonstrates a **GitOps-based Kubernetes deployment model** using **ArgoCD** and **Helm**.

The goal is to achieve:
- Clear separation between **application logic** and **environment configuration**
- Safe, auditable, and scalable Kubernetes deployments
- Git as the **single source of truth**

---

## 🏗️ Architecture

![GitOps Architecture](docs/diagrams/gitops-architecture.png)

### High-level overview

- **Helm Charts** define *how* applications are deployed
- **GitOps Configuration** defines *where* and *how* they run
- **ArgoCD** continuously reconciles Kubernetes clusters with Git

No manual `kubectl apply` is required after bootstrap.

---
🔍 **What This argoapp.yaml Application Does**

Pulls Helm charts from the Helm repository
Pulls environment-specific values from the GitOps repository
Renders the Helm chart using those values
Deploys resources into the target namespace
Continuously keeps the cluster state in sync with Git

🔄 **How $values Works**

$values refers to the Git repository defined using
ref: values

Example:
$values/zone1/dev/myapp.yaml

This means:
Load zone1/dev/myapp.yaml from the GitOps repository
Inject it as Helm values during rendering


🚀 **How to Apply**
Prerequisites

Kubernetes cluster
ArgoCD v2.6 or later
Cluster registered with ArgoCD
Access to both Git repositories


Apply the Application (One-Time Bootstrap)
kubectl apply -f clusters/zone1/dev/apps/myapp.yaml -n argocd


After this step:
ArgoCD takes full control
No further manual deployments are required
🔁 Day-to-Day Usage (GitOps Workflow)

After bootstrap:
❌ No kubectl apply in production
❌ No manual cluster changes
✅ All changes go through Git

**To deploy updates:**
Modify Helm values or image version in Git
Commit and merge the change
ArgoCD automatically syncs the cluster



⭐ **Benefits**

Git as the single source of truth
Reusable Helm charts across environments
Automated drift detection and self-healing
Easy rollbacks using Git
Clear ownership boundaries
Scales across zones and clusters

🧭 **Summary**
This repository implements a clean and scalable GitOps pattern by combining:
Helm for application templating
ArgoCD for continuous reconciliation
Git for declarative infrastructure management
If it is not defined in Git, it should not exist in the cluster.
