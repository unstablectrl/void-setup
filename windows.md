# Windows

[Set up your development environment on Windows](https://docs.microsoft.com/en-us/windows/dev-environment/)



## Dns

Checkout your interface aliases

```bash
Get-DnsClient
Get-DnsClientServerAddress -InterfaceAlias "Ethernet"
```

Setup [Cloudflare DNS](https://1.1.1.1/dns/) \(Open Terminal with Elevated Privileges\) 

```bash
Set-DnsClientServerAddress -InterfaceAlias "Ethernet" -ServerAddresses ("1.1.1.1","1.0.0.1", "2606:4700:4700::1111", "2606:4700:4700::1001")
Clear-DnsClientCache
```

## Windows Package Manager

Install [winget](https://docs.microsoft.com/en-us/windows/package-manager/winget/#install-winget)

## Apps

[winstall](https://winstall.app) \(Unofficial Store\)

[Unstable Pack](https://winstall.app/packs/lgSgBgqWf)

### DirectX

* [Website](https://www.microsoft.com/en-us/download/details.aspx?id=35)

## Fonts

[Fira Code](https://github.com/tonsky/FiraCode/wiki/Installing#windows)

[Nerd Fonts](https://www.nerdfonts.com/)

## Windows Terminal

[Current Settings](https://gist.github.com/unstablectrl/4b0e8f081d0487c3b2c1b96fa3f4dac0)

Compare Settings

```text
Compare-Object ((Invoke-WebRequest -Uri "https://gist.githubusercontent.com/unstablectrl/4b0e8f081d0487c3b2c1b96fa3f4dac0/raw/e3a00cc32593f13d265614743c4ae6e969a42552/settings.json" | select -ExpandProperty Content) -split '\r?\n') (Get-Content "$env:LOCALAPPDATA\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json")
```

Restore Settings

```text
Invoke-WebRequest -Uri "https://gist.githubusercontent.com/unstablectrl/4b0e8f081d0487c3b2c1b96fa3f4dac0/raw/e3a00cc32593f13d265614743c4ae6e969a42552/settings.json" -OutFile "$env:LOCALAPPDATA\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json"
```

### PowerShell

[Oh My Posh](https://ohmyposh.dev/docs/)

```bash
 Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
```

{% code title="~/Documents/WindowsPowerShell/Microsoft.PowerShell\_profile.ps1" %}
```bash
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```
{% endcode %}

