---
title: "Kubectl"
date: 2019-10-08T16:51:13+02:00
draft: false
weight: 40
---

[Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

Padok published an article (in French): [Les commandes à connaître avec Kubectl](https://www.padok.fr/blog/cluster-kubernetes-kubectl).

## Pods

```bash
kubectl get pods --namespace kube-system                    # Look at pods on kube-system namespace
kubectl get pods -A                                         # Get all pods
```

## Clean-up / removal

```bash
kubectl delete -f ./definition.json                   # Delete what was created by a manifest file
```
