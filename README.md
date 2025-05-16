# distributed-systems Kubernetes Hackathon

##  Overview

This project demonstrates deploying and managing the **Widgetario** microservices application in a **Kubernetes environment**, with a strong focus on **observability** using:

- **Prometheus + Grafana** for monitoring metrics
- **Elasticsearch + Fluent Bit + Kibana (EFK)** for centralized logging

## 📁 Repository Structure



---

##  Installation & Setup

### 1. Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop) with Kubernetes enabled
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Helm](https://helm.sh/)
- Git (optional)

### 2. Clone the Repository

git clone https://github.com/Alison-Kipyegon/distributed-systems.git
cd

### 3. Install Monitoring Stack (Prometheus + Grafana)

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install monitoring prometheus-community/kube-prometheus-stack --namespace monitoring --create-namespace

### 4. Install Logging Stack (Elasticsearch + Kibana + Fluent Bit)

helm repo add elastic https://helm.elastic.co
helm repo update
helm install elasticsearch elastic/elasticsearch --namespace logging --create-namespace
helm install kibana elastic/kibana --namespace logging


### 




