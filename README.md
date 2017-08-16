# Percona XtraDB Cluster (PXC) on Kubernetes

## Introduction
This repository contains files to spawn a PXC cluster on Kubernetes.
Kubernetes can ease the deployment and management of PXC cluster by leveraging some of Kubernetes advanced features including:

- Advanced Scheduling: Affinity and Anti-affinity
- Pod Disruption Budgets
- Dynamic Storage Provisioning
- Stateful Applications

There are deploymemnts variants with different storage options:
- host path storage (mount host directory inside container)
- dynamically provisioned storage (using custom storage class already defined in the cluster)
- dynamically provisioned local storage (using local storage class)
