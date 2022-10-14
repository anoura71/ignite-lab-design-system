# Dia 04 [Aula Extra]

## 1. Testes com o Storybook

https://storybook.js.org/docs/react/writing-tests/interaction-testing

https://storybook.js.org/docs/react/essentials/interactions

https://storybook.js.org/addons/@storybook/addon-interactions

```bash
npm i @storybook/addon-interactions @storybook/jest @storybook/testing-library @storybook/test-runner -D
```

### 1.1. Editar `.storybook/main.cjs`

```js
...
  "features": {
    ...
    "interactionsDebugger": true
  },
...
```

### 1.2. Editar `./package.json`

```json
...
    "scripts": {
      ...
      "test-storybook": "test-storybook"
    }
...
```

```bash
npm run test-storybook
```

## 2. "Back-end"

### 2.1. Axios

```bash
npm i axios
```

### 2.2. Mock Service Worker (MSW)

https://mswjs.io/

https://github.com/mswjs/msw-storybook-addon

```bash
npm i msw msw-storybook-addon -D

npx msw init public/
```

#### 2.2.1. Editar `.storybook/main.cjs`

```js
...
  "staticDirs": [
    "../public"
  ],
...
```

#### 2.2. Editar `.storybook/preview.cjs`

```js
...
import { initialize, mswDecorator } from 'msw-storybook-addon';

// Initialize MSW
initialize();

// Provide the MSW addon decorator globally
export const decorators = [mswDecorator];
...
```

## Versionamento

```bash
git st
git cb extra
git add .
git commit -m "Extra: after"
git push origin extra
```
