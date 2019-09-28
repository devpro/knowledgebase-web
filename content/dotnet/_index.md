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

### Videos

- [.NET Videos](https://dotnet.microsoft.com/learn/videos)

### Playgrounds

- [The Sandbox](https://docs.microsoft.com/en-us/sandbox/)

### Concepts

#### Memory allocation

- Heap vs Stack
  - Value types (int, char, etc.) are created in the Stack
  - Reference types (string, class, interface, etc.) are created in the Heap

### Namespaces

System.* are for the .NET Framework
Microsoft.* are built by Microsoft

### Recipes

### Package management

- FuGet
  - [Scott Hansleman - NuGet's fancy older sibling FuGet gives you a whole new view of the .NET packaging ecosystem](https://www.hanselman.com/blog/NuGetsFancyOlderSiblingFuGetGivesYouAWholeNewViewOfTheNETPackagingEcosystem.aspx)
- Nukeeper
  - [Scott Hanselman - NuKeeper for automated NuGet Package Reference Updates on Build Servers](https://www.hanselman.com/blog/NuKeeperForAutomatedNuGetPackageReferenceUpdatesOnBuildServers.aspx)
- Dependabot
  - [Scott Hanselman - Dependabot for .NET Core dependency tracking in GitHub](https://www.hanselman.com/blog/DependabotForNETCoreDependencyTrackingInGitHub.aspx)
- SourceLink
  - [Scott Hanselman - Exploring .NET Core's SourceLink - Stepping into the Source Code of NuGet packages you don't own](https://www.hanselman.com/blog/ExploringNETCoresSourceLinkSteppingIntoTheSourceCodeOfNuGetPackagesYouDontOwn.aspx)

### Code analysis

- [.NET API analyzer](https://docs.microsoft.com/en-us/dotnet/standard/analyzers/api-analyzer)
- [Overview of static code analysis for managed code in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/code-quality/code-analysis-for-managed-code-overview?view=vs-2017)

To be reviewed:

- VS 2017 extension [Microsoft Code Analysis 2017](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.MicrosoftCodeAnalysis2017)
- FxCop
- StyleCop
- How to integrate in an Azure Pipeline?

### CodeEditor

- [EditorConfig code formatting from the command line with .NET Core's dotnet format global tool](https://www.hanselman.com/blog/EditorConfigCodeFormattingFromTheCommandLineWithNETCoresDotnetFormatGlobalTool.aspx)

### Performances

- [BenchmarkDotNet](https://benchmarkdotnet.org) ([GitHub](https://github.com/dotnet/BenchmarkDotNet))

### Others

- [App Metrics](https://www.app-metrics.io/)
- [nuke](http://www.nuke.build/index.html)
