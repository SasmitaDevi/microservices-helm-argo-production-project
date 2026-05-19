# microservices-helm-argo-production-project
Production grade microservices app deployment with Helm and Argo CD
# Microservices Helm + Argo CD Portfolio

## Overview
This repository demonstrates a production-grade microservices deployment using:
- [Helm charts](ca://s?q=Helm_charts_structure) for frontend, backend, and database
- [Argo CD App of Apps](ca://s?q=Argo_CD_App_of_Apps_structure) for GitOps orchestration
- [CI/CD pipelines](ca://s?q=CI_CD_pipeline_structure) with GitHub Actions/Jenkins
- [Monitoring](ca://s?q=Kubernetes_monitoring_setup) via Prometheus and Grafana

## Architecture
![Architecture Diagram](docs/architecture.png)

- Frontend: Static site with ingress
- Backend: API service with secrets and hooks
- Database: PostgreSQL chart
- GitOps: Root + child applications managed by Argo CD

## Features
- Secrets management with Kubernetes Secrets
- Pre/post-install hooks in Helm
- Sync waves and RBAC in Argo CD
- Automated CI/CD pipeline for deployments
- Health checks and observability dashboards

## Repository Structure
- `charts/` → Helm charts for each service
- `argo-apps/` → Argo CD root + child applications
- `ci-cd/` → GitHub Actions and Jenkins pipelines
- `docs/` → Diagrams and documentation
- `monitoring/` → Prometheus/Grafana configs

## How to Deploy
1. Clone the repo
2. Install Helm and Argo CD
3. Apply the root application:
   ```bash
   kubectl apply -f argo-apps/root-app.yaml

