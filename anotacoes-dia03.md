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

## 3. Add-on de acessibilidade

https://storybook.js.org/addons/@storybook/addon-a11y

```bash
npm install @storybook/addon-a11y
```

## 4. Implementação do código

### 4.1. Logo - transformar em componente React

- No Figma, `Copy as SVG` (funciona no Chrome)
- Acessar `transform.tools` e obter código do componente React a partir do conteúdo copiado do Figma
