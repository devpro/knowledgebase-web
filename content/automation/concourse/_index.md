---
title: "Concourse"
date: 2019-09-13T15:10:09+02:00
draft: false
weight: 30
---

> Concourse is an open-source continuous thing-doer.
>
> Built on the simple mechanics of resources, tasks, and jobs, Concourse presents a general approach to automation that makes it great for CI/CD.

See [concourse-ci.org](https://concourse-ci.org/), [GitHub](https://github.com/concourse/concourse)

## Content

{{% children sort="Name" %}}

## Learn

Start with the [official documentation](https://concourse-ci.org/docs.html).

### Quick start

#### Run locally in 5 minutes

- Download the container configuration: `wget https://concourse-ci.org/docker-compose.yml`
- Start Docker Compose: `docker-compose up -d` (images can be seen with `docker images`)
- Open [localhost:8080](http://localhost:8080/) (login with test/test)
  - _Update (2020-03-02): login doesn't work for me on Firefox but works with Chrome_
- Look at the workers:  `fly -t localhost workers`
- Stop the containers: `docker-compose down`
- Stot and clean-up the resources: `docker-compose down --volumes` (volumes can be checked with `docker volume ls`)

To go further, feel free to have a look at [devpro/concourse-samples](https://github.com/devpro/concourse-samples).

### Presentations

- [A Pivotal Introduction to Concourse CI](https://www.youtube.com/watch?v=0bi_EWzhPvs&amp=&feature=youtu.be) - October 2, 2019
- [Concourse CI 102 - Taylor Silva & Scott Foerster, Pivotal](https://www.youtube.com/watch?v=H-4pvC7t2AI) - Sep 19, 2019
- [Concourse, Spinnaker, Cloud Foundry, Oh My! Creating Sophisticated Deployment Workflows - Cameron Stewart](https://www.slideshare.net/Pivotal/concourse-spinnaker-cloud-foundry-oh-my-creating-sophisticated-deployment-workflows-cameron-stewart) - Jun 17, 2019
- Introduction (French): [CD meetup](https://www.youtube.com/watch?v=IytJAamVdCs), [Devoxx](https://www.youtube.com/watch?v=moiSC3gmCew), [Paris Container Day](https://www.youtube.com/watch?v=Qv9FsIlyN-U) ([GitHub](https://github.com/Kehrlann/concourse-demo)) - March 22, 2018

### Tutorials

- [Concourse Tutorial by Stark & Wayne](https://concoursetutorial.com/)
- [Continuous Delivery of a Microservice Architecture using Concourse.ci, Cloud Foundry and Artifactory](https://specify.io/how-tos/concourse-ci-continious-integration-and-delivery-of-microservices)
- [Using Concourse CI/CD to publish Helm charts to ChartMuseum and report results to Slack (part #1)](https://medium.com/aptomi/using-concourse-ci-cd-to-publish-helm-charts-to-chartmuseum-and-report-results-to-slack-part-1-19d64dc7394b) - Feb 19, 2019

### Roadmap

- [Core roadmap: towards v10](https://blog.concourse-ci.org/core-roadmap-towards-v10/)

### Background

- [The Making of a Cloud-Native CI/CD Tool: The Concourse Journey](https://content.pivotal.io/blog/the-making-of-a-cloud-native-ci-cd-tool-the-concourse-journey) - July 2, 2019

### Samples

- [Official examples](https://concourse-ci.org/examples.html)
- [pivotalservices/concourse-pipeline-samples](https://github.com/pivotalservices/concourse-pipeline-samples)
- [Aptomi/concourse-pipelines](https://github.com/Aptomi/concourse-pipelines)

## Hosting

### Docker

- [micahyoung/concourse-docker-windows](https://github.com/micahyoung/concourse-docker-windows)

### Kubernetes

#### Helm

- [concourse/concourse-chart](https://github.com/concourse/concourse-chart)
- [Installing Concourse 5.0 on Kubernetes using Helm](https://medium.com/concourse-ci/installing-concourse-5-0-on-pivotal-container-service-using-helm-9f20e4e1b8bf) by Josh Ghiloni - Mar 29, 2019

### VM

- [How To Install Concourse CI on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-install-concourse-ci-on-ubuntu-16-04) - May 26, 2017
- [concourse/concourse-bosh-deployment](https://github.com/concourse/concourse-bosh-deployment)

### SaaS

- [aptomi](https://aptomi.io/) ([demo](https://cd.demo.aptomi.io/))

### Pivotal

- [Pivotal Concourse](https://docs.pivotal.io/p-concourse/v5/)

#### Cloud Foundation (GCP)

- [GoogleCloudPlatform/cloud-foundation-toolkit](https://github.com/GoogleCloudPlatform/cloud-foundation-toolkit/tree/master/infra)

## Tools

### Visual Studio Code

- Extension made by Pivotal: [Concourse CI Pipeline Editor](https://marketplace.visualstudio.com/items?itemName=Pivotal.vscode-concourse)
