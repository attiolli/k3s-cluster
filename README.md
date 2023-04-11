# Home Kubernetes cluster

## Structure ##

The Git repository contains the following directories under cluster.

* Flux directory is the entrypoint to Flux.
* Bootstrap directory contains a simple Kustomize resource to deploy Flux to an empty cluster.
* Apps directory is where my common applications are placed.

´´´
cluster
├── apps
├── bootstrap
├── charts
├── config
├── core
├── crds
└── flux
´´´

## Nodes ##

Node   | Hostname | RAM | Storage | Function | OS
------ | -------- | --- | ------- | -------- | --
Lenovo ThinkCentre M900 i5 | k8s-master1 | 8GB | 120GB SSD | Kube Master | Debian 11
VM on HPE Microserver (Proxmox) | k8s-worker1 | 4GB | 40GB SSD | Kube Worker | Debian 11
HP Prodesk 400 g1 i5 | k8s-worker2 | 8GB | 120GB SSD | Kube Worker | Debian 11
HP Prodesk 400 g1 celeron | k8s-worker3 | 8GB | 120GB SSD | Kube Worker | Debian 11

## Storage ##
Node   | Hostname | RAM | Storage | Function | OS | vPlatform
------ | -------- | --- | ------- | -------- | -- | ---------
VM on HPE Microserver | nas1 | 1GB | 2x2TB HDD, 2x1TB HDD | NFS Server | Debian 11 (CT) | Proxmox
