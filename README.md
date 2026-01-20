# k8s-autoscaling-lab
# Predictive Autoscaling in Kubernetes on AWS

# 🐳 Kubernetes HPA Home Lab using Vagrant & VirtualBox

This repository demonstrates **Horizontal Pod Autoscaling (HPA)** using a local multi-node Kubernetes cluster built with **Vagrant** and **VirtualBox**.

The project is based on and modified from the open-source project:  
👉 **[techiescamp/kubeadm-vagrant](https://github.com/techiescamp/kubeadm-vagrant)**

This setup is used to prove technical feasibility for Kubernetes autoscaling and serves as a foundation for future research on predictive autoscaling in **AWS EKS**.

---

## 🎯 Purpose of This Repository

This project is created to:

- **Demonstrate** Horizontal Pod Autoscaler (HPA) behavior
- **Observe** pod scaling under CPU load
- **Visualize** scaling using Kubernetes Dashboard
- **Validate** autoscaling concepts before moving to AWS EKS
- **Serve** as a technical demo for academic research

---

## ⚖️ License & Attribution

This project is a **modified and enhanced version** of:

🔗 **[techiescamp/kubeadm-vagrant](https://github.com/techiescamp/kubeadm-vagrant)**  
Licensed under **GPL-3.0**

All modifications in this repository are also released under **GPL-3.0**, in compliance with the original license.

See **[LICENSE.md](LICENSE.md)** for details.

---

## ✨ Enhancements & Work Done in This Version

Compared to the original project, this repository includes:

✅ **Fully working multi-node Kubernetes home lab**  
✅ **Kubernetes Dashboard installation & access**  
✅ **Metrics Server installation for HPA**  
✅ **CPU-based Horizontal Pod Autoscaler demo**  
✅ **Load generation to trigger pod scaling**  
✅ **Step-by-step demo documentation**  
✅ **Clean structure for academic use**

---
# 📋 Requirements

Make sure the following are installed on your host machine:

- **Ubuntu** (recommended)
- **VirtualBox**
- **Vagrant ≥ 2.2**

**Verify requirements:**
```bash
./scripts/check-requirements.sh
```
# 🚀 How to Run the Cluster
##1️⃣ Clone the Repository
```bash
git clone <your-repo-url>
cd k8s-hpa-homelab
```
##2️⃣ Start the Cluster
```bash
vagrant up
```
##2️⃣ Start the Cluster
```bash
vagrant up
```
This will:
-Create VirtualBox VMs
-Initialize Kubernetes using kubeadm
-Join worker nodes automatically

#🕹️ Access the Cluster
##SSH into Control Plane
```bash
vagrant ssh controlplane
```
##Verify Nodes
```bash
kubectl get nodes
```
#📊 Kubernetes Dashboard
##SSH into Control Plane
```bash
./scripts/dashboard.sh
```
# 📈 HPA Demo (Main Contribution)

## 1️⃣ Install Metrics Server
-Required for autoscaling metrics.
## 2️⃣ Deploy CPU Load Application
-CPU-intensive container.
-Single replica initially.
## 3️⃣ Create Horizontal Pod Autoscaler
-Scales pods based on CPU usage.
##4️⃣ Generate Load
-Artificial CPU stress
-Observe pod scaling in real time
## 5️⃣ Observe Results
-Pods increase automatically
-Visible in:
    kubectl get pods -w
    Kubernetes Dashboard
📌 This confirms Kubernetes autoscaling works correctly in the home lab.

#🛠️ Configuration
##Change number of worker nodes:
worker_nodes: 2
##Apply changes:
```bash
vagrant up --provision
```

#🧹 Cleanup
##Destroy the cluster completely:
```bash
./scripts/cleanup.sh
```

k8s-hpa-homelab/\
├── configs/          # Kubernetes configs\
├── scripts/          # Provisioning & helper scripts\
├── manifests/        # HPA demo manifests\
├── demo/             # Demo steps & documentation\
├── settings.yaml     # Worker node count\
├── Vagrantfile\
├── kubeconfig.txt\
└── README.md\

#🔮 Future Work
-Migrate setup to AWS EKS
-Integrate AI-based predictive autoscaler
-Compare HPA vs Predictive Scaling
-Add Prometheus & Grafana monitoring

#🔮 Future Work
## GPL-3.0
## Original project: https://github.com/techiescamp/kubeadm-vagrant
