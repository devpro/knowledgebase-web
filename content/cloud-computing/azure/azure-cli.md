---
title: "Azure CLI"
date: 2019-09-13T17:56:38+02:00
draft: false
weight: 20
---

Azure Command-Line Interface (CLI) [documentation](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest).

## Quick start

### Install

You can install the Azure CLI on any platform, Windows or Linux (including Windows Subsystem for Linux)

- [Install the Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)

### First steps

- Login to your Azure account

  ```bash
  az login
  ```

- Switch subscription

  ```bash
  az account set --subscription xxxx-xxxx-xxxx
  ```

- Display current subscription that is currenly set

```bash
az account show
```

- Example of use: [Create an App Service app and deploy files with FTP using Azure CLI](https://docs.microsoft.com/en-us/azure/app-service/scripts/cli-deploy-ftp)
