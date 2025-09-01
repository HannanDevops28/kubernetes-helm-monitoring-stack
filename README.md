# 🚀 Kubernetes Helm Monitoring Stack

This repository demonstrates how to deploy applications on **Kubernetes** using **Helm** along with a full **monitoring setup** using **Prometheus** and **Grafana**.  
The project is tested locally on **Minikube** but follows production-ready patterns.

---

## 📌 Features

- ✅ Kubernetes manifests for Pods, Services, ConfigMaps, and Secrets  
- ✅ Helm charts for:
  - Frontend (Next.js app)
  - Backend (Node.js REST API)
  - MongoDB (Bitnami chart)
- ✅ Monitoring with Prometheus & Grafana (via Helm)  
- ✅ Pre-configured Grafana dashboards (imported via IDs)  
- ✅ Example **stress test pod** for resource utilization monitoring  
- ✅ Alerting rules integrated with Grafana  

---

## 🛠️ Tech Stack

- **Kubernetes** – Container orchestration  
- **Helm** – Kubernetes package manager for charts  
- **Minikube** – Local Kubernetes cluster  
- **Prometheus** – Metrics collection & storage  
- **Grafana** – Visualization and alerting  
- **MongoDB** – Database (via Bitnami Helm chart)  
- **Next.js + Node.js** – Sample frontend & backend apps  

---

## 📂 Repository Structure

```bash
kubernetes-helm-monitoring-stack/
├── charts/
│   ├── frontend/          # Helm chart for Next.js frontend
│   ├── backend/           # Helm chart for Node.js backend
│   ├── mongodb/           # Helm chart for MongoDB (Bitnami)
│
├── environments/
│   ├── dev/
│   │   ├── values.yaml    # Dev environment overrides
│   ├── staging/
│   │   ├── values.yaml    # Staging environment overrides
│   ├── prod/
│       ├── values.yaml    # Prod environment overrides
│
├── monitoring/
│   ├── prometheus/        # Helm values for Prometheus
│   ├── grafana/           # Helm values for Grafana + dashboards
│   ├── alerts/            # Example alert rules
│
├── manifests/
│   ├── configmap.yaml     # App-level config
│   ├── secret.yaml        # App secrets
│   ├── ingress.yaml       # Ingress rules
│   ├── serviceaccount.yaml
│   ├── role.yaml
│   ├── rolebinding.yaml
│
└── README.md
