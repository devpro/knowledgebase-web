---
title: "Windows 10"
date: 2019-09-20T15:20:12+02:00
draft: false
---

## Commands

Command | Action
------- | ------
`winver` | Get general information on the Windows version and build number
`wmic os get caption` | Get OS caption
`wmic os get osarchitecture` | Get OS architecture

## Applications

### Windows Terminal (preview)

[Introducing Windows Terminal](https://devblogs.microsoft.com/commandline/introducing-windows-terminal/) - May 6th, 2019

Can be installed from Microsoft Store.

[Cascadia Code](https://devblogs.microsoft.com/commandline/cascadia-code/) - September 18th, 2019

Can be also available on MacOS with "brew install cask font-cascadia"

## Recipes

* [Disable Windows 10 On Screen Keyboard](https://appuals.com/fix-disable-windows-10-screen-keyboard/)

* Review what is scheduled to be launched at startup
  * Open the registory editor: `regedit`
    * Look at "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run key"

* [Temporarily prevent a driver update from reinstalling in Windows 10](https://support.microsoft.com/en-us/kb/3073930)

* [Have bash in Windows 10](http://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)

* Activate/Reenable Windows lock
  * Open the registory editor: `regedit`
    * Remove "DisableLockWorkStation"
  * Open Local Group Policy Editor: `gpedit.msc`
    * Disable "Remove Lock Computer" (in "Administrative Templates/System/Ctrl+Alt+Del Options")
