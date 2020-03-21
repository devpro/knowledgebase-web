---
title: "NuGet"
date: 2019-09-16T17:23:06+02:00
draft: false
weight: 40
---

NuGet is the package manager for .NET code source.

See: [nuget.org](https://www.nuget.org/), [Documentation](https://docs.microsoft.com/en-us/nuget/)

## Common packages

Name | Website | Source
---- | ------- | ------
AutoMapper | [automapper.org](https://automapper.org/) |
Dapper | [dapper-tutorial.net](https://dapper-tutorial.net/dapper) | [GitHub](https://github.com/StackExchange/Dapper)
FluentAssertions | [fluentassertions.com](http://www.fluentassertions.com/) |
FluentValidation | [fluentvalidation.net](https://fluentvalidation.net/) |
ImageSharp | [sixlabors.com](https://docs.sixlabors.com/articles/ImageSharp/GettingStarted.html) | [GitHub](https://github.com/SixLabors/ImageSharp)
MediatR | | [GitHUb](https://github.com/jbogard/MediatR)
Moq | | [GitHub](https://github.com/Moq/moq4)
Selenium WebDriver | |
xUnit | | [GitHub](https://github.com/xunit/xunit)

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
MyGet | [myget.org](https://www.myget.org), [Working with upstream sources](https://docs.myget.org/docs/reference/upstream-sources)
ProGet | [inedo.com](https://inedo.com/proget)
NuGet Server | [nugetserver.net](http://nugetserver.net/)
NuGet Gallery | [GitHub](https://github.com/NuGet/NuGetGallery)
