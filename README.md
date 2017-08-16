# Percona XtraDB Cluster (PXC) on Kubernetes

## Introduction
This repository contains files to spawn a PXC cluster on Kubernetes.
Kubernetes can ease the deployment and management of PXC cluster by leveraging some of Kubernetes advanced features including:

- Advanced Scheduling: Affinity and Anti-affinity
- Pod Disruption Budgets
- Dynamic Storage Provisioning
- Stateful Applications

## Setup
There are deploymemnts variants with different storage options:
- host path storage (mount host directory inside container)
```
kubectl create -f pxc-host-path-storage.yaml
kubectl create -f pxc-pdb.yaml
```
- dynamically provisioned storage (using custom storage class already defined in the cluster)
```
kubectl create -f pxc-dynamically-provisioned-storage.yaml
kubectl create -f pxc-pdb.yaml
```
- dynamically provisioned local storage (using local storage class)
```
kubectl create -f pv-local.yaml
kubectl create -f pxc-dynamically-provisioned-local-storage.yaml
kubectl create -f pxc-pdb.yaml
```
