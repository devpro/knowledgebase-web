---
title: "Kubernetes"
date: 2019-09-13T17:51:39+02:00
draft: false
weight: 40
---

> Kubernetes (K8s) is an open-source system for automating deployment, scaling, and management of containerized applications.

See [kubernetes.io](https://kubernetes.io/), [Documentation](https://kubernetes.io/docs/home/), [cheatsheet](https://devpro.github.io/kubernetes/cheatsheet.html).

## Content

{{% children sort="Name" %}}

## Learn

### Backgroung

Kubernetes was started by Google and, with its v1.0 release in July 2015, Google donated it to the [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/).

See Microsoft [What is Kubernetes?](https://aka.ms/k8slearning).

### Key elements

Pods

Controllers

Deployments

A [Services](https://kubernetes.io/docs/concepts/services-networking/service/) is an "abstract way to expose an application running on a set of Pods as a network service".

#### External traffic

- [Kubernetes NodePort vs LoadBalancer vs Ingress? When should I use what?](https://medium.com/google-cloud/kubernetes-nodeport-vs-loadbalancer-vs-ingress-when-should-i-use-what-922f010849e0)

### API

- [Overview](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.15/)

### Learning path

- [Microsoft](https://azure.microsoft.com/en-us/resources/kubernetes-learning-path/)

### Learning resources

- [List](https://docs.google.com/spreadsheets/d/10NltoF_6y3mBwUzQ4bcQLQfCE1BWSgUDcJXy-Qp2JEU/edit#gid=0) from [@kubernauts](https://twitter.com/kubernauts)
- [KodeKloud](https://kodekloud.com)
  - [Game of Pods](https://kodekloud.com/p/game-of-pods)
  - [Kubernetes for Beginners - Docker Introduction in 15 Minutes](https://www.youtube.com/watch?v=rmf04ylI2K0)
  - [Kubernetes Concepts Explained in 9 minutes!](https://www.youtube.com/watch?v=QJ4fODH6DXI)
- [awesome-kubernetes curated list](https://ramitsurana.github.io/awesome-kubernetes/)
- [Podcast](https://kubernetespodcast.com/)

### Posts

- [Key Kubernetes Concepts](https://towardsdatascience.com/key-kubernetes-concepts-62939f4bc08e)

### Tutorials

- [Running Background Tasks With Batch-Jobs](https://medium.com/google-cloud/kubernetes-running-background-tasks-with-batch-jobs-56482fbc853)
- [Superviser son cluster Kubernetes avec Prometheus et Grafana](https://blog.syloe.com/superviser-cluster-kubernetes-avec-grafana-et-prometheus/)

### Training

#### Online free training

- :heavy_check_mark: Intruqt [Kubernetes concepts](https://instruqt.com/public/tracks/kubernetes-concepts)
- Microsoft [Introduction to Azure Kubernetes Service](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-kubernetes-service/index)
- Linux Foundation [Introduction to Kubernetes (LFS158)](https://training.linuxfoundation.org/training/introduction-to-kubernetes/)
- Cognitive Class [Container & Kubernetes Essentials with IBM Cloud](https://cognitiveclass.ai/courses/kubernetes-course)
- Udacity [Scalable Microservices with Kubernetes](https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615)

#### Webinars

- Microsoft [Video series with Brendan Burns](https://aka.ms/k8s/lightboard)
- [Kubernetes Webinars](https://www.youtube.com/playlist?list=PLF3s2WICJlqOiymMaTLjwwHz-MSVbtJPQ&ref=hackr.io)

### Recipes

### Monitoring

- [The Complete Guide to Kubernetes Monitoring by sematext](https://sematext.com/guides/kubernetes-monitoring/)

#### Service Mesh

- [Kubernetes Service Mesh: A Comparison of Istio, Linkerd and Consul](https://platform9.com/blog/kubernetes-service-mesh-a-comparison-of-istio-linkerd-and-consul/)
- [Magalix Blog: What Is A Service Mesh?](https://www.magalix.com/blog/what-is-a-service-mesh) - Mar 10, 2020

#### Experiments

- [NTP in a Kubernetes cluster](https://tech.goglides.com/2020/03/09/manage-ntp-using-kubernetes/)

### Samples

- OpenShift team [Kubernetes By Example](http://kubernetesbyexample.com/)
- [sixeyed/k8s-win](https://github.com/sixeyed/k8s-win)

### Certifications

#### Certified Kubernetes Administrator (CKA)

- [Study guide from AutSoft](https://blog.autsoft.hu/certified-kubernetes-administrator/)
- [Review from Rieckpil](https://rieckpil.de/review-ckad-certified-kubernetes-application-developer-program/)

TODO :

- [Preparing for the Certified Kubernetes Administrator (CKA) Program](https://dzone.com/articles/preparing-for-the-certified-kubernetes-administrat?edition=542303&utm_source=Zone%20Newsletter&utm_medium=email&utm_campaign=cloud%202019-12-09)

## Ecosystem

### Tools

- [k14s](https://k14s.io/)

### Packaging

#### kpack

[Video TGI Kubernetes 091](https://www.youtube.com/watch?v=4zkRX9PSJ5k&feature=youtu.be)

## Managed environment

### Google Kubernetes Engine (GKE)

> Reliable, efficient, and secured way to run Kubernetes clusters

See [cloud.google.com](https://cloud.google.com/kubernetes-engine/).

Learning: [Getting Started by Coursera](https://www.coursera.org/learn/google-kubernetes-engine).

### Amazon Elastic Kubernetes Service (Amazon EKS)

> Highly available, scalable, and secure Kubernetes service

[aws.amazon.com](https://aws.amazon.com/eks/)

### Azure Kubernetes Service (AKS)

> Highly available, secure, and fully managed Kubernetes service

See [azure.microsoft.com](https://azure.microsoft.com/en-us/services/kubernetes-service/).

Also see [Empowering cloud-native developers on Kubernetes anywhere](https://cloudblogs.microsoft.com/opensource/2019/11/19/microsoft-kubecon-2019-announcements/) as an annoucement on KubeCon 2019 (November).

### Pivotal Container Service (PKS)

> Pivotal Container Service (PKS) is an enterprise Kubernetes platform, architected for rapid results, scaling, and reliability on any infrastructure.

See [pivotal.io](https://pivotal.io/platform/pivotal-container-service).

### Rancher

[rancher.com](https://rancher.com/)

### Deployment examples

- [cmeiklejohn/kubernetes-hello-world-example](https://github.com/cmeiklejohn/kubernetes-hello-world-example)
- [Kubernetes on Google Cloud Platform: deploy your app with Helm](https://www.padok.fr/en/blog/kubernetes-google-cloud-platform-app-helm)
