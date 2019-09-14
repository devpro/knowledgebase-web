---
title: ".NET"
date: 2019-09-13T11:42:25+02:00
draft: false
weight: 10
pre: "<i class='fa fa-circle'></i> "
---

**Official**: [dotnet.microsoft.com](https://dotnet.microsoft.com/), [docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/), [GitHub](https://github.com/Microsoft), [Twitter](https://twitter.com/dotnet)

**Tags**: Microsoft

## Content

{{% children sort="Name" %}}

## Learn

### Key components

- [**CoreCLR**](https://github.com/dotnet/coreclr) (Common Language Runtime) is the **runtime** for .NET Core. It includes the garbage collector, JIT compiler, primitive data types and low-level classes.
- [**Roslyn**](https://docs.microsoft.com/en-us/dotnet/csharp/roslyn-sdk/), .NET **compiler**, provides C# and Visual Basic languages with rich code analysis APIs. See [GitHub](https://github.com/dotnet/roslyn).

### Memory allocation

- Heap vs Stack
  - Value types (int, char, etc.) are created in the Stack
  - Reference types (string, class, interface, etc.) are created in the Heap
