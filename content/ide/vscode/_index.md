---
title: "Visual Studio Code"
date: 2019-09-19T11:03:08+02:00
draft: false
---

## Tips

### Shortcuts

Key combination | Action
--------------- | ------
`Shift + Tab` | Indent left
`Ctrl + :` | Toggle line comment

## Installation

### Windows

#### Windows Linux Subsystem

[Take your Linux development experience in Windows to the next level with WSL and Visual Studio Code Remote](https://devblogs.microsoft.com/commandline/take-your-linux-development-experience-in-windows-to-the-next-level-with-wsl-and-visual-studio-code-remote/) [Youtube - Visual Studio Code Remote - WSL](https://www.youtube.com/watch?time_continue=4&v=mIHprjsSO9o)

From wsl command window: `code .`

### Linux

[Visual Studio Code on Linux](https://code.visualstudio.com/docs/setup/linux)

- Download the package from the [Download](https://code.visualstudio.com/Download) page
- Open a command prompt and enter the subsystem: `wsl`
- Update apt: `sudo apt-get update`
- Execute the installation from the package: `sudo apt install /mnt/d/bertrand/Downloads/code_1.35.1-1560350270_amd64.deb`
- Uninstall: `sudo apt remove code`

## Extensions

- [VS Code Remote Development](https://code.visualstudio.com/docs/remote/remote-overview)
