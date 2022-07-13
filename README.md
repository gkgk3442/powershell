# windows store 설치
- windows terminal
- powershell
- winget (APP Installer 또는 앱 설치 관리자)

# Nerd Font 설치
- https://www.nerdfonts.com/font-downloads
- Meslo Nerd Font
- 윈도우 글꼴 설정에서 적용 할 것
- windows terminal 설정에서 폰트 설정

# posh-git 설치
```console
Install-Module posh-git -Scope AllUsers -Force
```

# oh-my-posh 설치
- 관리자 권한 windows terminal
```console
Install-Module oh-my-posh -Scope AllUsers -Force
Update-Module -Name oh-my-posh -AllowPrerelease -Scope AllUsers -Force
```

- 일반 windows terminal
```console
New-Item -ItemType File -Path $PROFILE
Get-PoshThemes
Set-PoshPrompt -Theme aliens
```

# oh-my-posh 사용자 기본값 설정
```console
code $PROFILE
```
```console
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\aliens.omp.json" | Invoke-Expression
```

# 테마 참조
- https://ohmyposh.dev/docs/themes
- https://github.com/JanDeDobbeleer/oh-my-posh/tree/main/themes
