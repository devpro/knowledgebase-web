---
title: "Puppet"
date: 2019-09-23T15:05:09+02:00
draft: false
weight: 70
---

See [puppet.com](https://puppet.com/).

## Learn

Puppet is a solution to automate the management of an infrastructure, it is an open source product with an important community. Current version is 6.3 (February 2019).
An enterprise edition is available with additional features that ease the use of the solution.

Entry points:

- [Puppet documentation](https://puppet.com/docs/puppet/latest)
- [Puppet training](https://learn.puppet.com/)
- [Presentation Dojo devpro](https://slides.com/devprofr/dojo-puppet)

### Architecture

Puppet is relying on the **agent-master** pattern:

1. An agent node sends a requests (with `facts`) to the master and asks for the desired state (`catalog`)
2. The master checks the node is known (and the communication is secured with HTTPS/certificate) and sends back the catalog based on its data repository (including the code to achieve the different configurations)
3. The agent applies the catalog and reports back the result of the actions

The Puppet master is also known as the `puppetserver`.

### Modules

#### Puppet Forge

Puppet is modular by design, first step is to look at existing modules for your needs (NB: don't reinvent the wheel and keep you code on added value). Module repository is Puppet forge at [forge.puppet.com](https://forge.puppet.com/).

Interesting modules:

| Name | Detail | Source |
|-|-|-|
| [puppetlabs/stdlib](https://forge.puppet.com/puppetlabs/stdlib) | Standard library of resources for Puppet modules. | [github](https://github.com/puppetlabs/puppetlabs-stdlib) |

#### Module creation

- [Module fundamentals](https://puppet.com/docs/puppet/6.3/modules_fundamentals.html)

### Pipeline

- [Continuous Deployment with Jenkins](https://www.slideshare.net/PuppetLabs/stephen-connolly)

### PDK (Puppet Development Kit)

- [Welcome to Puppet Development Kit](https://puppet.com/docs/pdk/1.x/pdk.html)
- [A guide to converting a module with PDK](https://puppet.com/blog/guide-converting-module-pdk)

### Bolt

- [Welcome to Bolt](https://puppet.com/docs/bolt/latest/bolt.html)
- [Check out the latest in Puppet Bolt](https://puppet.com/blog/check-out-latest-puppet-bolt)

### Tasks

- [Puppet tasks](https://puppet.com/docs/puppet/6.3/puppet_tasks.html)
- [Easily automate ad hoc work with new Puppet Tasks](https://puppet.com/blog/easily-automate-ad-hoc-work-new-puppet-tasks)

### r10k

- [puppetlabs/r10k](https://github.com/puppetlabs/r10k)
- [Managing code with r10k](https://puppet.com/docs/pe/2018.1/r10k.html)

### Training

- Puppet ([Course Catalog](https://learn.puppet.com/course-catalog))
  - [Self-paced Training](https://learn.puppet.com/category/self-paced-training)

### Azure

- [Azure Marketplace Image User Guide](https://puppet.com/docs/azure/1.0/azure_user_guide.html)

### Usecases

- [Using Node-Side Secrets with Puppet](https://puppet.com/blog/using-node-side-secrets-puppet)

### Docker

- [puppetlabs/pupperware](https://github.com/puppetlabs/pupperware/)
  - On Windows, edit the two files:

```yaml
# docker-compose.override.yml
version: '3.5'
```

```yaml
# docker-compose.yml
version: '3.5'
services:
   puppet:
     volumes:
       - /d/Projects/bthomas/opensource/pupperware/volumes/code:/etc/puppetlabs/code/
   networks:
     - proxynet

   postgres:
     ports:
       - 5432:5432
     networks:
       - proxynet

   puppetdb:
     hostname: puppetdb
     depends_on:
       - postgres
       - puppet
     networks:
       - proxynet

networks:
  proxynet:
    name: custom_network
```

## Practice

- [devpro/puppet-training-beginner](https://github.com/devpro/puppet-training-beginner)
