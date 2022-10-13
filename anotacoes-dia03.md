# Dia 03

## 1. Git

```bash
git init
```

## 2. Storybook Deployer

https://github.com/storybookjs/storybook-deployer

```bash
npm i @storybook/storybook-deployer --save-dev
```

### 2.1. Editar `./package.json`

```json
...
scripts: {
  ...
  "deploy-storybook": "storybook-to-ghpages"
}
...
```

### 2.2. Executar

```bash
npm run build-storybook
```
