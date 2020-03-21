---
title: "vstest"
date: 2020-02-23T15:19:57+01:00
draft: false
weight: 77
---

> Visual Studio Test Platform is the runner and engine that powers test explorer and vstest.console.

[GitHub](https://github.com/microsoft/vstest), [Documentation](https://github.com/microsoft/vstest-docs)

## Configuration

- [Configure a test run](https://github.com/microsoft/vstest-docs/blob/master/docs/configure.md)

- [Configure unit tests by using a .runsettings file](https://docs.microsoft.com/en-us/visualstudio/test/configure-unit-tests-by-using-a-dot-runsettings-file)

- Interesting change brought by [PR #2128](https://github.com/microsoft/vstest/pull/2128)

```xml
<!-- File name extension must be .runsettings -->
<RunSettings>
  <RunConfiguration>
    <EnvironmentVariables>
      <!-- List of environment variables we want to set-->
      <DOTNET_ROOT>C:\ProgramFiles\dotnet</DOTNET_ROOT>
      <SDK_PATH>C:\Codebase\Sdk</SDK_PATH>
    </EnvironmentVariables>
  </RunConfiguration>
</RunSettings>
```
