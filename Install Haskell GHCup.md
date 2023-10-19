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
# Haskell
export GHCUP_HOME="${HOME}/.ghcup/bin"
export CABAL_HOME="${HOME}/.cabal/bin"
case ":${PATH}:" in
  *":${GHCUP_HOME}:"*) ;;
  *) export PATH="${PATH}:${GHCUP_HOME}" ;;
esac
case ":${PATH}:" in
  *":${CABAL_HOME}:"*) ;;
  *) export PATH="${PATH}:${CABAL_HOME}" ;;
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

- Install GHC, HLS, cabal, Stack

```shell
%> ghcup tui

### Press "i" to install
### Press "s" to set
### Press "q" to quit
### Press "enter" to continue
```

- Write default cabal configuration

```shell
% cabal user-config init -f
% code ${HOME}/.cabal/config
```

- Check GHC, HLS, cabal, Stack version

```shell
%> ghcup list
%> ghc --version
%> ghci --version
%> stack --version
%> cabal --version
%> haddock --version
%> haskell-language-server-wrapper --version
```

## Initial Haskell Project

- Initial Haskell Project

```shell
%> mkdir -p hello_haskell && code hello_haskell

%> cabal init --interactive
### Configuration
Should I generate a simple project with sensible defaults? [default: y] y
###
```

- Run Haskell Project

```shell
%> cabal update
%> cabal install
%> cabal build
%> cabal run
```
