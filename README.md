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

## Nodes ##

Node   | Hostname | RAM | Storage | Function | OS
------ | -------- | --- | ------- | -------- | --
Lenovo ThinkCentre M900 i5 | k8s-master1 | 8GB | 256GB NVMe | Kube Master | Debian 12
Raspberry CM5 | k8s-worker4 | 8GB | 120GB NVMe | Kube Worker | Debian 12
Raspberry CM5 | k8s-worker5 | 8GB | 120GB NVMe | Kube Worker | Debian 12
Raspberry CM5 | k8s-worker6 | 8GB | 120GB NVMe | Kube Worker | Debian 12

## Storage ##
Node   | Hostname | RAM | Storage | Function | OS
------ | -------- | --- | ------- | -------- | --
Raspberry CM5 | nas3 | 8GB | 1x120GB NVMe, 1x2TB HDD | NFS Server | Debian 12
