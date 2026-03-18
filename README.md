Argo CD GitOps Lab on AWS EKS

### Automate Kubernetes Deployments Using GitOps

This hands-on lab demonstrates how to **deploy and manage applications on Kubernetes using GitOps with Argo CD on AWS EKS**.

Modern cloud teams no longer deploy applications manually.
Instead, they use **Git as the single source of truth**, and tools like **Argo CD** automatically synchronize infrastructure and applications.

This lab shows how to build a **fully automated deployment pipeline** where:

* code is stored in Git
* Argo CD detects changes
* Kubernetes updates automatically

This approach is widely used by **DevOps and DevSecOps teams in production environments**.

---

# 🧠 What You Will Learn

This lab introduces key concepts of **GitOps and Kubernetes automation**:

| Concept                | Explanation                                   |
| ---------------------- | --------------------------------------------- |
| Amazon EKS             | Managed Kubernetes cluster on AWS             |
| Argo CD                | GitOps tool for continuous deployment         |
| Git Repository         | Source of truth for application configuration |
| Synchronization        | Automatically applying changes to Kubernetes  |
| Declarative Deployment | Infrastructure defined as code                |

These concepts are essential for **modern cloud-native deployments**.

---

# 🏗 Lab Architecture

The GitOps workflow implemented in this lab:

```id="6l0i27"
Git Repository
       ↓
Argo CD monitors changes
       ↓
Argo CD syncs with Kubernetes (EKS)
       ↓
Application deployed automatically
```

This architecture ensures that **any change in Git is automatically applied to the cluster**.

---

# ⚙️ Lab Steps

## Step 1 — Create a Kubernetes Cluster (EKS)

Start by creating an **Amazon EKS cluster**.

This cluster will:

* host applications
* run Kubernetes workloads
* serve as the target for Argo CD deployments

EKS simplifies Kubernetes management in AWS.

---

# ⚙️ Step 2 — Install Argo CD

Next, install **Argo CD** in the Kubernetes cluster.

Argo CD runs inside Kubernetes and is responsible for:

* monitoring Git repositories
* deploying applications
* synchronizing cluster state

Installation is typically done using:

```id="50b6l7"
kubectl apply -n argocd -f install.yaml
```

---

# 🔗 Step 3 — Connect to the Kubernetes Cluster

Configure access to the cluster using **kubectl**.

Example:

```id="u5kpfk"
kubectl get nodes
```

This confirms that:

* the cluster is running
* you can interact with Kubernetes

---

# 🌐 Step 4 — Access the Argo CD Interface

After installation, access the **Argo CD Web UI**.

From the interface, you can:

* visualize applications
* monitor deployment status
* manage synchronization

The UI provides a **clear view of your GitOps pipeline**.

---

# 🔗 Step 5 — Connect a Git Repository

Argo CD uses a Git repository as the **source of truth**.

Connect your repository containing:

* Kubernetes manifests
* deployment configurations

This allows Argo CD to **track changes in your application configuration**.

---

# 🚀 Step 6 — Deploy an Application

Create an application in Argo CD.

Argo CD will:

* read configuration from Git
* deploy resources to Kubernetes
* manage application lifecycle

This step demonstrates **automated deployment using GitOps**.

---

# 🔄 Step 7 — Enable Automatic Synchronization (GitOps)

Enable **auto-sync** in Argo CD.

Workflow:

```id="pqg9mm"
Change in Git
     ↓
Argo CD detects change
     ↓
Cluster automatically updated
```

This means:

* no manual deployment
* no direct cluster modification
* everything is controlled via Git

This is the core principle of **GitOps**.

---

# 🛡 Security & Best Practices Demonstrated

This lab demonstrates important **DevOps and GitOps best practices**:

✔ Infrastructure as Code (IaC)
✔ Git as single source of truth
✔ Automated deployments
✔ Reduced human error
✔ Continuous synchronization
✔ Secure Kubernetes operations

These practices are used in **modern production systems**.

---

# 🎯 Skills Demonstrated

Completing this lab demonstrates knowledge of:

* Kubernetes (EKS)
* GitOps workflows
* Argo CD configuration
* Automated deployment pipelines
* Infrastructure as Code principles

These skills are highly valuable for roles such as:

* DevOps Engineer
* DevSecOps Engineer
* Kubernetes Engineer
* Cloud Engineer

---

# 🚀 Why This Lab Matters

Traditional deployments are:

* manual
* error-prone
* difficult to track

GitOps solves these problems by:

* automating deployments
* ensuring consistency
* improving reliability

This lab demonstrates how to **implement a modern, automated, and scalable deployment strategy**.

