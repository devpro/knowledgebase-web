---
title: ".NET Core"
date: 2019-08-09T23:27:59+02:00
draft: false
weight: 1
---

.NET Core is the cross-platform version of .NET Framework, it is also the future of the .NET technology.

See [docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/core/) ([Roadmap](https://github.com/dotnet/core/blob/master/roadmap.md#upcoming-ship-dates)).

## Content

{{% children sort="Name" %}}

## Learn

> .NET Core is a general purpose, modular, cross-platform and open source implementation of the .NET Standard. It contains many of the same APIs as the .NET Framework (but .NET Core is a smaller set) and includes runtime, framework, compiler and tools components that support a variety of operating systems and chip targets. The .NET Core implementation was primarily driven by the ASP.NET Core workloads but also by the need and desire to have a more modern implementation. It can be used in device, cloud and embedded/IoT scenarios.

From [.NET Core and Open-Source](https://docs.microsoft.com/en-us/dotnet/framework/get-started/net-core-and-open-source).

### Features

- [Configuration](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration)
- [Learning about .NET Core futures by poking around at David Fowler's GitHub](https://www.hanselman.com/blog/LearningAboutNETCoreFuturesByPokingAroundAtDavidFowlersGitHub.aspx)
- Memory: poster from [Pro .NET Memory](https://prodotnetmemory.com/)

### Versions

You can find all the release notes on [GitHub](https://github.com/dotnet/core/tree/master/release-notes).

### Tutorials

Start with [.NET Tutorial - Hello World in 10 minutes](https://dotnet.microsoft.com/learn/dotnet/hello-world-tutorial/intro) then [Learn .NET Core and the .NET Core SDK tools by exploring these Tutorials](https://docs.microsoft.com/en-us/dotnet/core/tutorials/).

## Recipes

### Scripting

- [Scott Hanselman - C# and .NET Core scripting with the "dotnet-script" global tool](https://www.hanselman.com/blog/CAndNETCoreScriptingWithTheDotnetscriptGlobalTool.aspx)

### Docker

.NET Core runs really well on Docker.

[dotnet/dotnet-docker](https://github.com/dotnet/dotnet-docker) is the GitHub repository for .NET Core Docker official images, which are now hosted on [Microsoft Container Registry (MCR)](https://azure.microsoft.com/en-us/services/container-registry/). To know more read this arcticle [.NET Core Container Images now Published to Microsoft Container Registry](https://devblogs.microsoft.com/dotnet/net-core-container-images-now-published-to-microsoft-container-registry/) published on March 15, 2019.

[Julien Chable](http://julien.chable.net/) has an interesting blog to follow with articles on .NET Core and Docker.

Official images repository:

- [ASP.NET Core Runtime](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/)
- [.NET Core Samples](https://hub.docker.com/_/microsoft-dotnet-core-samples)
- [.NET Core](https://hub.docker.com/_/microsoft-dotnet-core)

To review:

- [Getting Started with .NET Core and Docker and the Microsoft Container Registry](https://www.hanselman.com/blog/GettingStartedWithNETCoreAndDockerAndTheMicrosoftContainerRegistry.aspx) 2019-03-22
- [Dockerize an ASP.NET Core application](https://docs.docker.com/engine/examples/dotnetcore/)
- [Scott Hanselman - .NET Core and Docker](https://www.hanselman.com/blog/NETCoreAndDocker.aspx)
- [A complete containerized .NET Core Application microservice that is as small as possible](https://www.hanselman.com/blog/ACompleteContainerizedNETCoreApplicationMicroserviceThatIsAsSmallAsPossible.aspx)

### .NET Core on Kubernetes

- [Deploy ASP.NET Core app to Kubernetes on Google Kubernetes Engine](https://codelabs.developers.google.com/codelabs/cloud-kubernetes-aspnetcore/#0)
- [Deploy ASP.NET Core apps to Azure Kubernetes Service with Azure DevOps Projects](https://docs.microsoft.com/en-us/azure/devops-project/azure-devops-project-aks)
- [Access the Kubernetes web dashboard in Azure Kubernetes Service (AKS)](https://docs.microsoft.com/en-gb/azure/aks/kubernetes-dashboard)

### Background tasks

- [Implement background tasks in microservices with IHostedService and the BackgroundService class](https://docs.microsoft.com/en-us/dotnet/standard/microservices-architecture/multi-container-microservice-net-applications/background-tasks-with-ihostedservice) 2019-01-07

### Excel

- [Converting an Excel Worksheet into a JSON document with C# and .NET Core and ExcelDataReader](https://www.hanselman.com/blog/ConvertingAnExcelWorksheetIntoAJSONDocumentWithCAndNETCoreAndExcelDataReader.aspx)

### HTTP Client with NTLM authentication

{{< highlight csharp >}}
// Startup.cs
public void ConfigureServices(IServiceCollection services)
{
    services.AddHttpClient(apiClientConfiguration.HttpClientName)
        .ConfigurePrimaryHttpMessageHandler(
            x => new HttpClientHandler
            {
                Credentials = new CredentialCache {
                {
                  new Uri(apiClientConfiguration.EndpointDomain), "NTLM", new NetworkCredential(_configuration.CustomApiClientUsername, _configuration.CustomApiClientPassword)
                }
            }
        });
}
{{< /highlight >}}

### CMS

- [OrchardCMS](https://github.com/OrchardCMS/OrchardCore)
- nopCommerce
  - [Scott Hanselman - Exploring nopCommerce - open source e-commerce shopping cart platform in .NET Core](https://www.hanselman.com/blog/ExploringNopCommerceOpenSourceEcommerceShoppingCartPlatformInNETCore.aspx)
- [Scott Hanselman - Headless CMS and Decoupled CMS in .NET Core](https://www.hanselman.com/blog/HeadlessCMSAndDecoupledCMSInNETCore.aspx)

## .NET Core & PHP

- [Scott Hanselman - The whole of WordPress compiled to .NET Core and a NuGet Package with PeachPie](https://www.hanselman.com/blog/TheWholeOfWordPressCompiledToNETCoreAndANuGetPackageWithPeachPie.aspx)

## Angular & ASP.NET Core

- [Use the Angular project template with ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/client-side/spa/angular)
