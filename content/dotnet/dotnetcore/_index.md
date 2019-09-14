---
title: ".NET Core"
date: 2019-08-09T23:27:59+02:00
draft: false
weight: 1
---

**Official**: [docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/core/) ([Roadmap](https://github.com/dotnet/core/blob/master/roadmap.md#upcoming-ship-dates))

**Tags**: Microsoft, OpenSource, CrossPlatform

## Content

{{% children sort="Name" %}}

## Learning

- [Learning about .NET Core futures by poking around at David Fowler's GitHub](https://www.hanselman.com/blog/LearningAboutNETCoreFuturesByPokingAroundAtDavidFowlersGitHub.aspx)

### Features

- [Configuration](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration)

## Recipes

### Scripting

- [Scott Hanselman - C# and .NET Core scripting with the "dotnet-script" global tool](https://www.hanselman.com/blog/CAndNETCoreScriptingWithTheDotnetscriptGlobalTool.aspx)

### Docker

- 2019-03-22 [Getting Started with .NET Core and Docker and the Microsoft Container Registry](https://www.hanselman.com/blog/GettingStartedWithNETCoreAndDockerAndTheMicrosoftContainerRegistry.aspx)
- 2019-03-15 [.NET Core Container Images now Published to Microsoft Container Registry](https://devblogs.microsoft.com/dotnet/net-core-container-images-now-published-to-microsoft-container-registry/)
- [dotnet/dotnet-docker](https://github.com/dotnet/dotnet-docker)
- [Dockerize an ASP.NET Core application](https://docs.docker.com/engine/examples/dotnetcore/)
- [Scott Hanselman - .NET Core and Docker](https://www.hanselman.com/blog/NETCoreAndDocker.aspx)
- [A complete containerized .NET Core Application microservice that is as small as possible](https://www.hanselman.com/blog/ACompleteContainerizedNETCoreApplicationMicroserviceThatIsAsSmallAsPossible.aspx)

### .NET Core on Kubernetes

- [Deploy ASP.NET Core app to Kubernetes on Google Kubernetes Engine](https://codelabs.developers.google.com/codelabs/cloud-kubernetes-aspnetcore/#0)
- [Deploy ASP.NET Core apps to Azure Kubernetes Service with Azure DevOps Projects](https://docs.microsoft.com/en-us/azure/devops-project/azure-devops-project-aks)
- [Access the Kubernetes web dashboard in Azure Kubernetes Service (AKS)](https://docs.microsoft.com/en-gb/azure/aks/kubernetes-dashboard)

### Background tasks

- 2019-01-07 [Implement background tasks in microservices with IHostedService and the BackgroundService class](https://docs.microsoft.com/en-us/dotnet/standard/microservices-architecture/multi-container-microservice-net-applications/background-tasks-with-ihostedservice)

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
