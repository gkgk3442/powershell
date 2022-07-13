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

# oh-my-posh
- 참조 : https://ohmyposh.dev/
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

# vscode settings.json
```json
"terminal.integrated.fontFamily": "'MesloLGS NF'"
```

# wsl 설정
```consle
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
mkdir ~/.poshthemes
wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/themes.zip -O ~/.poshthemes/themes.zip
unzip ~/.poshthemes/themes.zip -d ~/.poshthemes
chmod u+rw ~/.poshthemes/*.omp.*
rm ~/.poshthemes/themes.zip
vi ~/.profile
```

```console
eval "$(oh-my-posh --init --shell bash --config ~/.poshthemes/aliens.omp.json)"
```
