---
title: "Console"
date: 2019-09-23T11:21:36+02:00
draft: false
weight: 120
---

## Learn

### Deployment

- [Deploying .NET Core apps with command-line interface (CLI) tools](https://docs.microsoft.com/en-us/dotnet/core/deploying/deploy-with-cli)

## Recipes

### Working with processes

- Get the list of active processes

{{< highlight csharp >}}
var processes = System.Diagnostics.Process.GetProcesses();
{{< /highlight >}}

- Start a new process

{{< highlight csharp >}}
using System.Diagnostics;
using (var process = new Process()
{
    StartInfo = new ProcessStartInfo
    {
        FileName               = "my\path\file.exe",
        Arguments              = "my arguments",
        RedirectStandardOutput = true,
        UseShellExecute        = false,
        CreateNoWindow         = true,
        Verb                   = "runas"
    }
})
{
    process.Start();
    var result = process.StandardOutput.ReadToEnd();
    process.WaitForExit();
    return result;
}
{{< /highlight >}}
