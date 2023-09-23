# Initial Plasmo Project

## Initail

```shell
% mkdir -p hello_plasmo && code hello_plasmo

% PKG1="extension"

% pnpm init

% mkdir -p packages/{${PKG1},}

% code pnpm-workspace.yaml
### +++++++++++++++++++++++++++++++++
packages:
  - "packages/*"
### +++++++++++++++++++++++++++++++++
```

## Create Plasmo project

```shell
% (cd packages/ && pnpm create plasmo ${PKG1} --with-src)

### +++++++++++++++++++++++++++++++++
🟡 Extension description: imToken account abstraction wallet.
🟡 Author name: imToken Labs <irara.chen@token.im>
### +++++++++++++++++++++++++++++++++
```

## Start project dev

- Start project dev

```shell
% pnpm install
% pnpm --filter ${PKG1} dev
```

- Turn on Chrome browser extension `developer mode`

```
chrome://extensions
```

## Pack project

- Method 1

```shell
% pnpm --filter ${PKG1} package
```

- Method 2

```shell
% pnpm --filter ${PKG1} build --zip
```

## Appendix: Change project name

```shell
% PKG1="extension"
% cat <<< $(jq --arg P1 "$PKG1" '.name = $P1' packages/${PKG1}/package.json) > packages/${PKG1}/package.json
```
