---
title: "Azure CLI"
date: 2019-09-13T17:56:38+02:00
draft: false
weight: 20
---

## Quick start

### Install

You can install the Azure CLI on any platform, Windows or Linux (including Windows Subsystem for Linux)

- [Install the Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
  - [Install with apt on Debian or Ubuntu](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-apt)

### First steps

- Login to your Azure account

  ```bash
  az login
  ```

- Switch subscription

  ```bash
  az account set --subscription xxxx-xxxx-xxxx
  ```

- Example of use: [Create an App Service app and deploy files with FTP using Azure CLI](https://docs.microsoft.com/en-us/azure/app-service/scripts/cli-deploy-ftp)
