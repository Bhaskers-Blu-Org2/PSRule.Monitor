# Install instructions

## Prerequisites

- Windows PowerShell 5.1 with .NET Framework 4.7.2+ or
- PowerShell Core 6.2 or greater on Windows, MacOS and Linux

For a list of platforms that PowerShell Core is supported on [see](https://github.com/PowerShell/PowerShell#get-powershell).

The `PSRule` module is required for `PSRule.Monitor` to work.
The required version will automatically be installed along-side `PSRule.Monitor` when using `Install-Module` or `Update-Module` cmdlets.

## Getting the modules

### PowerShell Gallery

Install from [PowerShell Gallery][module] for all users (requires permissions):

```powershell
# Install module
Install-Module -Name 'PSRule.Monitor' -Repository PSGallery;
```

Install from [PowerShell Gallery][module] for current user only:

```powershell
# Install module
Install-Module -Name 'PSRule.Monitor' -Repository PSGallery -Scope CurrentUser;
```

Save for offline use from PowerShell Gallery:

```powershell
# Save module, in the .\modules directory
Save-Module -Name 'PSRule', 'PSRule.Monitor' -Path '.\modules';
```

> For pre-release versions the `-AllowPrerelease` switch must be added when calling `Install-Module` or `Save-Module`.
>
> To install pre-release module versions, upgrading to the latest version of _PowerShellGet_ may be required. To do this use:
>
> `Install-Module -Name PowerShellGet -Repository PSGallery -Scope CurrentUser -Force`

[module]: https://www.powershellgallery.com/packages/PSRule.Monitor
