---
title: "Design"
date: 2019-09-21T18:18:42+02:00
draft: false
weight: 30
---

## Inversion of control & dependency injection

- [Martin Fowler website page](https://www.martinfowler.com/articles/injection.html) - January 23, 2004

## Microservice

> Microservices are small, modular, and independently deployable services. Docker containers (for Linux and Windows) simplify deployment and testing by bundling a service and its dependencies into a single unit, which is then run in an isolated environment.

[source](https://blogs.msdn.microsoft.com/wriju/2017/12/18/microservices-docker-architecture-for-apps/) ([GitHub](https://github.com/dotnet-architecture/eShopOnContainers))

Articles:

- [Design a microservice-oriented application](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/microservice-application-design)

## DDD (Domain Driven Design)

Read:

- Definition on [wikipedia](https://en.wikipedia.org/wiki/Domain-driven_design)
- Starting point with [Tackle Business Complexity in a Microservice with DDD and CQRS Patterns](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/)

Code examples:

- [citerus/dddsample-core](https://github.com/citerus/dddsample-core)
- [kgrzybek/modular-monolith-with-ddd](https://github.com/kgrzybek/modular-monolith-with-ddd)

## Hexagonal Architecture

If you're French, you can look at this article from [Octo](https://blog.octo.com/architecture-hexagonale-trois-principes-et-un-exemple-dimplementation/).

## Feature flags

Feature flags are a great way to do continuous delivery with the latest source code and activate when needed new functionalities. But there is a cost that is described in an article from [opensource](https://opensource.com/article/18/7/does-progressive-exposure-really-come-cost).

## Communication

Two standards are recommended:

- REST
- gRPC

As of 2019, REST is still more widely used but gRPC contains great improvements and will be used more and more for new microservices.

You can easily find comparison between REST and gRPC on the internet, for example [code.tutsplus.com](https://code.tutsplus.com/tutorials/rest-vs-grpc-battle-of-the-apis--cms-30711). There is an interesting summary on [docs.microsoft.com](https://docs.microsoft.com/en-us/aspnet/core/grpc/comparison?view=aspnetcore-3.0).
