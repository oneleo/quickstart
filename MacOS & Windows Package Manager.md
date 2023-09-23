# MacOS & Windows Package Manager

## macOS

- Install [Homebrew](https://brew.sh/)

```shell
% /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- Add [drives](https://github.com/Homebrew/homebrew-cask-drivers) and [fonts](https://github.com/Homebrew/homebrew-cask-fonts) repositories

```shell
% brew tap homebrew/cask-drivers
% brew tap homebrew/cask-fonts

### Add Logi Options+
% brew install --cask logi-options-plus

### Add Garamond font
% brew install font-eb-garamond font-cormorant-garamond
```

- Add other desktop tools

```shell
### System and development
% brew install --cask cakebrew blackhole-2ch karabiner-elements gpg-suite-no-mail

### Development
% brew install --cask postman github ganache ghcup graphql-playground visual-studio-code

### Browser
% brew install --cask firefox google-chrome microsoft-edge

### Community
% brew install --cask slack wechat discord telegram voov-meeting

### Media
% brew install --cask vlc obs avidemux audacity videofusion
```

- Add other command line tools

```shell
% brew install git nvm podman ffmpeg lame imagemagick yt-dlp

% mkdir -p "$HOME/.nvm" && code ~/.zshrc
### Edit ~/.zshrc
  export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && \. "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion

  # Git language
  alias git='LC_ALL=en_GB git'
###
```

- Add other desktop tools from App Store
  - [Xcode](https://apps.apple.com/us/app/xcode/id497799835)
  - [Keynote](https://apps.apple.com/tw/app/keynote/id409183694)
  - [Numbers](https://apps.apple.com/us/app/numbers/id409203825)
  - [Pages](https://apps.apple.com/tw/app/pages/id409201541)
  - [iMovie](https://apps.apple.com/tw/app/imovie/id408981434)
  - [ColorSlurp](https://apps.apple.com/tr/app/colorslurp/id1287239339)
  - [Gifski](https://apps.apple.com/app/id1351639930)

## Windows

- Install [Chocolatey](https://community.chocolatey.org/)

```shell
> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

- Add other desktop tools

```shell
### System
> choco upgrade -y chocolatey chocolateygui intel-dsa nvidia-display-driver dontsleep.install hwinfo.install crystaldiskinfo treesizefree chrome-remote-desktop-host wincdemu

### Development
> choco install -y git.install --params '/NoShellIntegration'
> choco install -y cmake --installargs 'ADD_CMAKE_TO_PATH=User'
> choco install -y openjdk golang python3 nvm unxutils mingw dotnetcore sqlite postman sqlitebrowser sysinternals powertoys vscode github-desktop

### Community
> choco install -y telegram.install

### Media
> choco install -y obs-studio vlc k-litecodecpackbasic yt-dlp ffmpeg lame avidemux audacity audacity-ffmpeg audacity-lame imagemagick.app

### Tools
> choco install -y notepadplusplus.install vmwareworkstation adobereader 7zip.install winrar rufus winscp.install

### Need license Keys: treesizefree, vmwareworkstation, and winrar

### Office
> choco install -y microsoft-office-deployment --params="'/64bit /DisableUpdate:TRUE /Product:ProPlus2021Volume,VisioPro2021Volume,ProjectStd2021Volume /ProofingToolLanguage:zh-tw /Exclude:OneDrive,Lync /RemoveMSI /LicenseKey:FXYTK-NJJ8C-GB6DW-3DYQT-6F7TH'"

### Obtain Office KMS authorization
### Office KMS Keys: https://learn.microsoft.com/zh-cn/deployoffice/vlactivation/gvlks
> cd "C:\Program Files\Microsoft Office\Office16"
> cscript ospp.vbs /sethst:"<YOUR KMS SERVER URL>"
> cscript ospp.vbs /act
> cscript ospp.vbs /dstatus
```
