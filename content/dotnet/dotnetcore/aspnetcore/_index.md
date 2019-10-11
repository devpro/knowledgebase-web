---
title: "ASP.NET Core"
date: 2019-09-13T16:07:03+02:00
draft: false
weight: 100
---

> ASP.NET Core is an open-source and cross-platform .NET framework for building modern cloud-based web applications on Windows, Mac, or Linux.

See the documentation on [docs.microsoft.com](https://docs.microsoft.com/en-us/aspnet/#pivot=core) the source code on [GitHub](https://github.com/aspnet/AspNetCore)

## Content

{{% children sort="Name" %}}

## Learn

### Fundamentals

- [Configuration](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration/)
- [Dependency Injection](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection)
- [Logging](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging/)
- [Multiple environments](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/environments)
- [Web server implementations](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/servers/)
- [Filters](https://docs.microsoft.com/en-us/aspnet/core/mvc/controllers/filters)
  - [Dependency Injection in Action Filters](https://www.devtrends.co.uk/blog/dependency-injection-in-action-filters-in-asp.net-core)
- [Host and Deploy](https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/index)
- [Identity](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity)
- [Integration tests](https://docs.microsoft.com/en-us/aspnet/core/test/integration-tests)
- [Routing](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/routing)

### Deep dive

- [Host and deploy](https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/)
- [Performance Best Practices](https://docs.microsoft.com/en-us/aspnet/core/performance/performance-best-practices)
  - [Performance and reliability](https://docs.microsoft.com/en-us/aspnet/core/performance/performance-best-practices?view=aspnetcore-3.0#performance-and-reliability)
- [The shared framework](https://natemcmaster.com/blog/2018/08/29/netcore-primitives-2/)

## Recipes

### Swagger

- [Get started with Swashbuckle and ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle)

### Logging

- [ASP.NET Core Logging with Azure App Service and Serilog](https://devblogs.microsoft.com/aspnet/asp-net-core-logging/)

### Performance

- [ASP.NET Core: Saturating 10GbE at 7+ million request/s](https://www.ageofascent.com/2019/02/04/asp-net-core-saturating-10gbe-at-7-million-requests-per-second/)
- [TechEmpower - Web Framework Benchmarks](https://www.techempower.com/benchmarks/)

### OData

- [Channel 9 - Supercharging your Web APIs with OData and ASP.NET Core](https://channel9.msdn.com/Shows/On-NET/Supercharging-your-Web-APIs-with-OData-and-ASPNET-Core)

### Securing

- [Securing ASP.NET Core 2.0 Applications with JWTs](https://auth0.com/blog/securing-asp-dot-net-core-2-applications-with-jwts/)

### Testing

- [Integration tests in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/test/integration-tests)
- 2018-05-23 [Real Browser Integration Testing with Selenium Standalone, Chrome, and ASP.NET Core 2.1](https://www.hanselman.com/blog/RealBrowserIntegrationTestingWithSeleniumStandaloneChromeAndASPNETCore21.aspx)
- [IntegrationTestsSample](https://github.com/aspnet/AspNetCore.Docs/tree/master/aspnetcore/test/integration-tests/samples/2.x/IntegrationTestsSample)

### Versioning

- [aspnet-api-versioning](https://github.com/Microsoft/aspnet-api-versioning)
- [Blog of Pi](https://www.blogofpi.com/versioning-web-api/)

### Health checks

- [Xabaril/AspNetCore.Diagnostics.HealthChecks](https://github.com/Xabaril/AspNetCore.Diagnostics.HealthChecks)

### Packaging

#### WebPack

Articles to review:

- [A complete containerized .NET Core Application microservice that is as small as possible](https://www.ryansouthgate.com/2017/08/29/asp-net-core-and-webpack-part-1/)
- [Setting up Webpack in ASP.NET Core](https://cecilphillip.com/setting-up-webpack-in-asp-net-core/)
- [ReactJs Webpack and ASP.NET Core](https://sensibledev.com/reactjs-webpack-and-asp-net-core/#postSummary)
- [How to use Webpack in ASP.Net core projects; a basic React Template sample](https://codeburst.io/how-to-use-webpack-in-asp-net-core-projects-a-basic-react-template-sample-25a3681a5fc2)
- [BUNDLING IN .NET CORE MVC APPLICATIONS WITH WEBPACK](https://dotnetcore.gaprogman.com/2017/01/05/bundling-in-net-core-mvc-applications-with-webpack/)
- [How to include Bootstrap in your project with Webpack](https://stevenwestmoreland.com/2018/01/how-to-include-bootstrap-in-your-project-with-webpack.html)

### Controller action status code

{{< highlight csharp >}}
public IActionResult Post([FromBody]string action)
{
    if (...)
    {
        return StatusCode(423);
    }

    return Ok(new ... {});
  }
}
{{< /highlight >}}

### Authentication

#### Use Azure Directory

- Go to Azure Portal and create an application in Azure Active Directory: [Integrating Azure AD into an ASP.NET Core web app](https://azure.microsoft.com/en-us/resources/samples/active-directory-dotnet-webapp-openidconnect-aspnetcore/)

- Examples: [GitHub Azure-Samples/active-directory-dotnet-webapp-openidconnect-aspnetcore](https://github.com/Azure-Samples/active-directory-dotnet-webapp-openidconnect-aspnetcore) or run `dotnet new mvc -o dotnetadauth --auth SingleOrg --client-id <clientId> --tenant-id <tenantId> --domain <domainName>`

- Edit csproj file

{{< highlight xml >}}
<PackageReference Include="Microsoft.AspNetCore.Authentication.AzureAD.UI" Version="2.1.1" />
{{< /highlight >}}

- Edit `appsettings.json` file

{{< highlight json >}}
"AzureAd": {
  "Instance": "https://login.microsoftonline.com/",
  "Domain": "<domainName>",
  "TenantId": "<tenantId>",
  "ClientId": "<clientId>",
  "CallbackPath": "/signin-oidc"
},
{{< /highlight >}}

- Edit `Startup.cs`:

{{< highlight csharp >}}
// in ConfigureServices()

services.Configure<CookiePolicyOptions>(options =>
{
    // This lambda determines whether user consent for non-essential cookies is needed for a given request.
    options.CheckConsentNeeded = context => true;
    options.MinimumSameSitePolicy = SameSiteMode.None;
});

services.AddAuthentication(AzureADDefaults.AuthenticationScheme)
    .AddAzureAD(options => Configuration.Bind("AzureAd", options));

services
    .AddMvc(options =>
    {
        var policy = new AuthorizationPolicyBuilder()
            .RequireAuthenticatedUser()
            .Build();
        options.Filters.Add(new AuthorizeFilter(policy));
    })
    .SetCompatibilityVersion(CompatibilityVersion.Version_2_1);

// in Configure()

if (env.IsDevelopment())
{
    app.UseDeveloperExceptionPage();
}
else
{
    app.UseExceptionHandler("/Error");
    app.UseHsts();
}

app.UseHttpsRedirection();
app.UseStaticFiles();
app.UseSpaStaticFiles();
app.UseCookiePolicy();

app.UseAuthentication();
{{< /highlight >}}
