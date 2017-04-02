# Echo Cache Cluster
This repository tracks the needed files for configuration and management of Echo Cache's production k8s cluster

# Installation and Usage

- Install `kubectl`:
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/darwin/amd64/kubectl
```
- Clone this repository
-  Move it's directory, and run the following:
```
kubectl --kubeconfig=kubeconfig proxy
```
- Naviage to `127.0.0.1:8001/ui` in a Browser

# Technical Debt

Right now this repository is tracking certificate files, which is less than ideal. Down the line, I would like to migrate this secret management to something like:
https://github.com/hashicorp/vault
