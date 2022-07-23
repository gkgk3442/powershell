# oh-my-posh
```console
Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://ohmyposh.dev/install.ps1'))
```

```console
Install-Module oh-my-posh -Scope CurrentUser -Force
```
```console
Update-Module -Name oh-my-posh -AllowPrerelease -Scope CurrentUser -Force
```
```console
Get-PoshThemes
```
```console
code $PROFILE

oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\aliens.omp.json" | Invoke-Expression
```
