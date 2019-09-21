---
title: ".NET"
date: 2019-09-13T11:42:25+02:00
draft: false
weight: 5
pre: "<i class='fa fa-dot-circle'></i> "
---

See [dotnet.microsoft.com](https://dotnet.microsoft.com/), [docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/), [GitHub](https://github.com/Microsoft), [Twitter](https://twitter.com/dotnet).

## Content

{{% children sort="Name" %}}

## Learn

### Key components

- [**CoreCLR**](https://github.com/dotnet/coreclr) (Common Language Runtime) is the **runtime** for .NET Core. It includes the garbage collector, JIT compiler, primitive data types and low-level classes.
- [**Roslyn**](https://docs.microsoft.com/en-us/dotnet/csharp/roslyn-sdk/), .NET **compiler**, provides C# and Visual Basic languages with rich code analysis APIs. See [GitHub](https://github.com/dotnet/roslyn).

### Guides

- [.NET Architecture Guides](https://dotnet.microsoft.com/learn/dotnet/architecture-guides)
  - [.NET Microservices Architecture Guidance](https://dotnet.microsoft.com/learn/aspnet/microservices-architecture) ([Microservice architecture with ASP.NET Core](https://channel9.msdn.com/Events/Build/2017/T6051) May 08, 2017, [dotnet-architecture/eShopOnContainers](https://github.com/dotnet-architecture/eShopOnContainers))

### Playgrounds

- [The Sandbox](https://docs.microsoft.com/en-us/sandbox/)

### Concepts

#### Memory allocation

- Heap vs Stack
  - Value types (int, char, etc.) are created in the Stack
  - Reference types (string, class, interface, etc.) are created in the Heap
