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
