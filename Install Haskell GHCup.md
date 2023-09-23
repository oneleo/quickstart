# Install Haskell GHCup

## macOS & Linux

- Install [Homebrew](https://brew.sh/)

```shell
% /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- Install [GHCup](https://www.haskell.org/ghcup/)

```shell
% brew install ghcup

% code ~/.zshrc
### Edit ~/.zshrc
# GHCup
export GHCUP_HOME="${HOME}/.ghcup/bin"
case ":${PATH}:" in
  *":${GHCUP_HOME}:"*) ;;
  *) export PATH="${PATH}:${GHCUP_HOME}" ;;
esac
###
```

## Windows

- Before installation

```shell
> Set-ExecutionPolicy Bypass -Scope Process -Force;[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; try { Invoke-Command -ScriptBlock ([ScriptBlock]::Create((Invoke-WebRequest https://www.haskell.org/ghcup/sh/bootstrap-haskell.ps1 -UseBasicParsing))) -ArgumentList $true } catch { Write-Error $_ }
```

- Install [GHCup](https://www.haskell.org/ghcup/)

```shell
curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh
```

## Install GHC, HLS, cabal, Stack

```shell
%> ghcup tui

### Press "i" to install
### Press "s" to set
### Press "q" to quit
### Press "enter" to continue
```

## Check GHC, HLS, cabal, Stack version

```shell
%> ghc --version
%> ghci --version
%> stack --version
%> cabal --version
%> haddock --version
%> haskell-language-server-wrapper --version
```
