# windows store 설치
- windows terminal
- powershell
- winget (APP Installer 또는 앱 설치 관리자)

# Nerd Font 설치
- https://www.nerdfonts.com/font-downloads
- Meslo Nerd Font
- 윈도우 글꼴 설정에서 적용 할 것
- windows terminal 설정에서 폰트 설정

# oh-my-posh 설치
- 관리자 권한 windows terminal
```console
Install-Module posh-git -Scope AllUsers -Force
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
code $HOME/.my_theme.omp.json
```
```json
{
  "$schema": "https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/schema.json",
  "blocks": [
    {
      "alignment": "left",
      "segments": [
        {
          "background": "#61AFEF",
          "foreground": "#ffffff",
          "leading_diamond": "\ue0b6",
          "style": "diamond",
          "template": " {{ .UserName }}@{{ .HostName }} ",
          "trailing_diamond": "\ue0b0",
          "type": "session"
        },
        {
          "background": "#C678DD",
          "foreground": "#ffffff",
          "powerline_symbol": "\ue0b0",
          "properties": {
            "style": "full"
          },
          "style": "powerline",
          "template": " {{ .Path }} ",
          "type": "path"
        },
        {
          "background": "#95ffa4",
          "foreground": "#193549",
          "powerline_symbol": "\ue0b0",
          "style": "powerline",
          "template": " {{ .HEAD }} ",
          "type": "git"
        },
        {
          "background": "#FF6471",
          "foreground": "#ffffff",
          "leading_diamond": "<transparent,background>\ue0b0</>",
          "style": "diamond",
          "template": " {{ if .Error }}{{ .Error }}{{ else }}{{ if .Venv }}{{ .Venv }} {{ end }}{{ .Full }}{{ end }} ",
          "trailing_diamond": "\ue0b4",
          "type": "python"
        }
      ],
      "type": "prompt"
    }
  ],
  "final_space": true,
  "version": 2
}
```
```console
oh-my-posh --init --shell pwsh --config $HOME/.my_theme.omp.json | Invoke-Expression
```

# 테마 참조
- https://ohmyposh.dev/docs/themes
- https://github.com/JanDeDobbeleer/oh-my-posh/tree/main/themes
