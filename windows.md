# Windows

[Set up your development environment on Windows](https://docs.microsoft.com/en-us/windows/dev-environment/)

## Windows Package Manager

Install [winget](https://docs.microsoft.com/en-us/windows/package-manager/winget/#install-winget)

### Apps

[winstall](https://winstall.app) \(Unofficial Store\)

[Unstable Pack](https://winstall.app/packs/lgSgBgqWf)

## Fonts

[Fira Code](https://github.com/tonsky/FiraCode/wiki/Installing#windows)

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

