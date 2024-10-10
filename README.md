# Odoo Kubernetes Deployment

This repository contains Kubernetes manifests for deploying Odoo, an open-source ERP and CRM platform, on a Kubernetes cluster. The provided YAML files configure various Kubernetes resources required to run Odoo efficiently and securely.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Files in this Repository](#files-in-this-repository)
- [Deployment Steps](#deployment-steps)
- [Resource Details](#resource-details)
- [Cleanup](#cleanup)
- [License](#license)

## Prerequisites
- A running Kubernetes cluster (v1.14 or later recommended)
- `kubectl` configured to interact with your cluster
- Persistent storage provisioner in your cluster (for PersistentVolumeClaims)
- Basic knowledge of Kubernetes resources

## Files in this Repository

| File                 | Description                                                   |
|----------------------|---------------------------------------------------------------|
| `class.yaml`          | Defines the StorageClass for persistent storage               |
| `configmap.yaml`      | Contains configuration data for Odoo                          |
| `ingress.yaml`        | Sets up Ingress resource for external access                  |
| `odoo-deployment.yaml`| Deployment resource for Odoo application                      |
| `odoo-service.yaml`   | Service resource to expose Odoo pods                          |
| `pv-claim.yaml`       | PersistentVolumeClaim for Odoo data storage                   |
| `pv-workload.yaml`    | Defines the PersistentVolume (if not dynamically provisioned) |
| `rbac.yaml`           | Role-Based Access Control settings                            |

## Deployment Steps

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/odoo-kubernetes-deployment.git
cd odoo-kubernetes-deployment
