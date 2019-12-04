---
title: "Helm"
date: 2019-12-04T17:12:58+01:00
draft: false
weight: 35
---

> Helm 3: The package manager for Kubernetes. It is the best way to find, share, and use software built for Kubernetes.

[helm.sh](https://helm.sh/) [GitHub](https://github.com/helm/helm) [docs](https://helm.sh/docs/)

## Quick start

### Installation

On Windows, get the zip file from the Release page and extract the exe file to a folder defined in the PATH environment variable.

Confirm it is ok by running `helm version`.

### Update repository

Add at least one repository, for instance `helm repo add stable https://kubernetes-charts.storage.googleapis.com/`.

Run `helm repo update` to update the repository.

You can look at what is available with `helm search repo stable`.

### First try with mysql

Install the first chart with `helm install stable/mysql --generate-name`.

The ouput of this command is very interesting:

  MySQL can be accessed via port 3306 on the following DNS name from within your cluster: mysql-xxxxxxx.default.svc.cluster.local

  To get your root password run: `MYSQL_ROOT_PASSWORD=$(kubectl get secret --namespace default mysql-xxxxxxx -o jsonpath="{.data.mysql-root-password}" | base64 --decode; echo)`

  To connect to your database:

  1. Run an Ubuntu pod that you can use as a client: `kubectl run -i --tty ubuntu --image=ubuntu:18.04 --restart=Never -- bash -il`

  2. Install the mysql client: `$ apt-get update && apt-get install mysql-client -y`

  3. Connect using the mysql cli, then provide your password: `$ mysql -h mysql-xxxxxxx -p`

  To connect to your database directly from outside the K8s cluster: MYSQL_HOST=127.0.0.1, MYSQL_PORT=3306. Execute the following command to route the connection: `kubectl port-forward svc/mysql-xxxxxxx 3306` and `mysql -h ${MYSQL_HOST} -P${MYSQL_PORT} -u root -p${MYSQL_ROOT_PASSWORD}`.

As usual, look at the progress with `kubectl get pods` ("STATUS" column).

At the end, clean your cluster `helm uninstall mysql-xxxxxxx`.

### CLI reference

Command | Action
------- | ------
`helm show chart stable/xxxx` | Get a simple idea of the features of chart stable/xxxx (stable/mysql for example)
`helm list` | See what has been released with Helm
`helm help xxx` | Get help message on xxx command (install for example)
