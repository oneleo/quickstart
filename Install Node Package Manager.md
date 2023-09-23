# Node Package Manager

## macOS & Linux

- Install [NVM](https://github.com/nvm-sh/nvm)

```shell
% brew install nvm

% mkdir -p "$HOME/.nvm" && code ~/.zshrc
### Edit ~/.zshrc
  export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && \. "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
###
```

- Add [NPM](https://www.npmjs.com/), [PNPM](https://pnpm.io/), and [Yarn](https://yarnpkg.com/) V1

```shell
% nvm install 20 && nvm use 20
% npm install --global npm pnpm yarn@1

### Check version
% npm --version
% pnpm --version
% yarn --version
```

## Windows

- Install [NVM](https://github.com/nvm-sh/nvm)

```shell
> choco install -y nvm
```

- Add [NPM](https://www.npmjs.com/), [PNPM](https://pnpm.io/), and [Yarn](https://yarnpkg.com/) V1

```shell
> nvm install 20
> nvm use 20
> npm install --global npm pnpm yarn@1

### Check version
> Set-ExecutionPolicy Bypass -Scope Process -Force; npm --version
> Set-ExecutionPolicy Bypass -Scope Process -Force; pnpm --version
> Set-ExecutionPolicy Bypass -Scope Process -Force; yarn --version
```
