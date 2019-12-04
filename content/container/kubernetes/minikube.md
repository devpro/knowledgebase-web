---
title: "Minikube"
date: 2019-12-04T20:42:09+01:00
draft: false
weight: 50
---

> Local Kubernetes, focused on application development & education

[minikube.sigs.k8s.io](https://minikube.sigs.k8s.io/) [GitHub](https://github.com/kubernetes/minikube)

## Quick start

### Installation

Follow the instructions given in the [Getting Started page](https://minikube.sigs.k8s.io/docs/start/).

### Run/stop

If you're on Windows, make Hyper-V the default driver: `minikube config set vm-driver hyperv`.

Run `minikube start` to start the Kubernetes node and `minikube stop` to stop it.

### Clean-up

Run `minikube` and if needed, delete the `.kube` and `.minikube` folder in your home directory.

### Dashboard

Run `minikube dashboard` to open the web dashboard.

## CLI reference

Command | Action
------- | ------
`minikube service xxx --url` | Display url for a given service (xxx)
`minikube config set memory 4096` | Set memory value (2048 by default)
