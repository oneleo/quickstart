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

## Create React project

- Method 1: Via [Vite](https://vitejs.dev/guide/)

```shell
% pnpm create vite packages/${PKG1} --template react-swc-ts
? Package name: › webapp
```

- Method 2: Via [Next](https://nextjs.org/docs/pages/api-reference/create-next-app)

```shell
% (cd packages/ && pnpm create next-app ${PKG1} --typescript --tailwind --eslint --src-dir --import-alias "@/*" --use-pnpm)
```

## Add other React tools

```shell
pnpm --filter ${PKG1} install --save-dev html-react-parser
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
