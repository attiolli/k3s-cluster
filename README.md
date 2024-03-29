# Home Kubernetes cluster

## Structure ##

The Git repository contains the following directories under cluster.

* Flux directory is the entrypoint to Flux
* Config directory is for cluster config files
* Bootstrap directory contains a simple Kustomize resource to deploy Flux to an empty cluster.
* Apps directory is where my common applications are placed.

```
cluster
├── apps
├── bootstrap
├── config
└── flux
```

## Network ##
![net](https://user-images.githubusercontent.com/5729471/232335946-d11a40e4-2990-4911-bce0-496af82779b0.png)




## Nodes ##

Node   | Hostname | RAM | Storage | Function | OS
------ | -------- | --- | ------- | -------- | --
Lenovo ThinkCentre M900 i5 | k8s-master1 | 8GB | 256GB NVMe | Kube Master | Debian 12
VM on HPE Microserver (Proxmox) | k8s-worker1 | 4GB | 40GB NVMe | Kube Worker | Debian 12
HP Prodesk 400 g1 i5 | k8s-worker2 | 8GB | 256GB SSD | Kube Worker | Debian 12
HP Prodesk 400 g1 celeron | k8s-worker3 | 8GB | 256GB SSD | Kube Worker | Debian 12

## Storage ##
Node   | Hostname | RAM | Storage | Function | OS | vPlatform
------ | -------- | --- | ------- | -------- | -- | ---------
VM on HPE Microserver | nas1 | 1GB | 1x250GB NVMe, 2x2TB HDD, 2x1TB HDD | NFS Server | Debian 11 (CT) | Proxmox
