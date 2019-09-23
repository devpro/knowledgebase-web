---
title: "Windows Subsystem for Linux"
date: 2019-09-23T15:37:57+02:00
draft: false
---

## Windows Subsystem for Linux

### Installation

[Microsoft learn > Get started with Windows Subsystem for Linux](https://docs.microsoft.com/en-us/learn/modules/get-started-with-windows-subsystem-for-linux/)

### Readings about WSL

- Microsoft
  - [Windows Subsystem for Linux Documentation](https://docs.microsoft.com/en-us/windows/wsl/about)
- Scott Hanselman
  - [The year of Linux on the (Windows) Desktop - WSL Tips and Tricks](https://www.hanselman.com/blog/TheYearOfLinuxOnTheWindowsDesktopWSLTipsAndTricks.aspx)
  - [Using Enhanced Mode Ubuntu 18.04 for Hyper-V on Windows 10](https://www.hanselman.com/blog/UsingEnhancedModeUbuntu1804ForHyperVOnWindows10.aspx)

### Recipes

#### Connect to Windows Docker

- In Docker settings, make sure to expose the daemon (in Settings > General > Expose daemon on tcp://localhost:2375 without TLS)

- In Linux, make sure the DOCKER_HOST environment variable is set

  > $ echo $DOCKER_HOST
  >
  > localhost:2375
