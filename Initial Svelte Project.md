# Initial React Project

## Initail

```shell
% PKG1="webapp"

% pnpm init

% mkdir -p packages/{${PKG1},}

% code pnpm-workspace.yaml
### Edit pnpm-workspace.yaml
packages:
  - "packages/*"
###
```

## Create Svelte project

- Via [Vite](https://vitejs.dev/guide/)

```shell
% pnpm create vite packages/${PKG1} --template svelte-ts
? Package name: › webapp
```

## Start project

```shell
% pnpm install
% pnpm --filter ${PKG1} dev
```

## Appendix: Change project name

```shell
% PKG1="webproject"
% cat <<< $(jq --arg P1 "$PKG1" '.name = $P1' packages/${PKG1}/package.json) > packages/${PKG1}/package.json
```
