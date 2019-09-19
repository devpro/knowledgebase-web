---
title: "NuGet"
date: 2019-09-16T17:23:06+02:00
draft: false
weight: 20
---

NuGet is the package manager for .NET code source.

See: [nuget.org](https://www.nuget.org/), [Documentation](https://docs.microsoft.com/en-us/nuget/)

## Common packages

Name | Site
---- | ----
AutoMapper | [automapper.org](https://automapper.org/)
FluentValidation | [fluentvalidation.net](https://fluentvalidation.net/)

## NuGet CLI

### CLI documentation

- [NuGet CLI reference](https://docs.microsoft.com/en-us/nuget/reference/nuget-exe-cli-reference)

### CLI useful commands

- Self-update: `nuget update -self`
- Create spec file: `nuget spec`
- Create packages: `nuget pack`

## Recipes

### Create a package

- [Package creation workflow](https://docs.microsoft.com/en-us/nuget/create-packages/overview-and-workflow)

### Publish NuGet packages from AzureDevOps

- [Versioning and publishing NuGet packages automatically using Azure DevOps Pipelines](https://whereslou.com/2018/09/versioning-and-publishing-nuget-packages-automatically-using-azure-devops-pipelines/)
- [Customize your build (C#, Visual Basic)](https://docs.microsoft.com/en-us/visualstudio/msbuild/customize-your-build?view=vs-2017)

### Host public/private feeds

Name | Site
---- | ----
Azure Packages | Provided by Azure DevOps
MyGet | [myget.org](https://www.myget.org)
ProGet | [inedo.com](https://inedo.com/proget)
NuGet Server | [nugetserver.net](http://nugetserver.net/)
NuGet Gallery | [GitHub](https://github.com/NuGet/NuGetGallery)
