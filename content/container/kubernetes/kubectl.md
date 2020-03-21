---
title: "Kubectl"
date: 2019-10-08T16:51:13+02:00
draft: false
weight: 40
---

[Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

## Resources

### Pods

```bash
# list pods of a specific namespace
kubectl get pods --namespace kube-system
# list pods of all namespaces
kubectl get pods -A
# get more information about a pod
kubectl describe pod
# get log information of a specific pod
kubectl logs
# get pod yaml definition
kubectl get pod -o yaml
```

### Deployments

```bash
kubectl get deployment
```

### Services

```bash
kubectl get services
```

## Configuration

### ConfigMaps

### Secrets

## Events

```bash
kubectl get events --sort-by=.metadata.creationTimestamp
```

## Scale

```bash
kubectl scale
```

## Port forwarding

```bash
kubectl port-forward xxx 8080:80
```

## Clean-up

```bash
# delete what was deployed by a manifest file
kubectl delete -f ./definition.json
```
