---
description: Basic setup for AD testing from Windows
---

# Setup

### Bypassing AV Signatures in PowerShell

#### Run AMSITrigger

```powershell
AmsiTrigger_x64.exe -i C:\AD\Tools\Invoke-PowerShellTcp_Detected.ps1
```

#### Run DefenderCheck

```powershell
DefenderCheck.exe PowerUp.ps1
```

For full obfuscation of PowerShell scripts, try:

{% embed url="https://github.com/danielbohannon/Invoke-Obfuscation" %}
Invoke-Obfuscation
{% endembed %}

### Set up

#### Run Invisi-Shell

```powershell
C:\AD\Tools\InviShell\RunWithRegistryNonAdmin.bat
```

#### Load PowerView

```powershell
. C:\AD\Tools\PowerView.ps1
```

#### Load AD Module

{% code overflow="wrap" %}
```powershell
Import-Module C:\AD\Tools\ADModule-master\Microsoft.ActiveDirectory.Management.dll
```
{% endcode %}

{% code overflow="wrap" %}
```powershell
Import-Module C:\AD\Tools\ADModule-master\ActiveDirectory\ActiveDirectory.psd1
```
{% endcode %}
