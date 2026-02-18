# Home Kubernetes cluster

## Structure ##

The Git repository contains the following directories under cluster:

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
Raspberry CM5 | k8s-master1 | 8GB | 250GB NVMe | Kube Master | Debian 13
Raspberry CM5 | k8s-worker5 | 8GB | 120GB NVMe | Kube Worker | Debian 13
Raspberry CM5 | k8s-worker6 | 8GB | 120GB NVMe | Kube Worker | Debian 13

## Storage ##
Node   | Hostname | RAM | Storage | Function | OS
------ | -------- | --- | ------- | -------- | --
Raspberry CM5 | nas3 | 8GB | 1x120GB NVMe, 1x10TB HDD | NFS Server | Debian 13
