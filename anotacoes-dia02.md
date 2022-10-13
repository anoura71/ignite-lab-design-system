# Dia 02

## 1. Criar projeto `lab-ds` React com TypeScript

https://vitejs.dev/

```bash
npm create vite@latest

cd lab-ds
npm i
```

## 2. Tailwind CSS

```bash
npm i -D tailwindcss postcss autoprefixer

npx tailwindcss init -p
```

## 2.1. Editar `./tailwind.config.cjs`

```js
...
  content: [
    './src/**/*.tsx',
  ],
...
```

## 3. Font _Inter_

https://fonts.google.com

Procurar font Inter >> View all styles >> Selecionar estilos >> Copiar código em `link` para dentro do `index.html`

```html
...
<head>
  <meta charset="UTF-8" />

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  ...
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap"
    rel="stylesheet"
  />
  <title>...</title>
</head>
...
```

## 3.1. Editar `./tailwind.config.cjs`

```js
...
  theme: {
    extend: {
      fontFamily: {
        sans: 'Inter, sans-serif',
      }
    },
  },
...
```

## 4. Storybook

https://storybook.js.org/

### 4.1. Instalar

```bash
npx sb init --builder @storybook/builder-vite --use-npm

// √ Do you want to run the 'npm7' migration on your project? ... no
```

### 4.2. Executar

```bash
npm run storybook
```

### 4.3. Mudar o tema

- Criar arquivo `./.storybook/manager.js`

```js
import { addons } from '@storybook/addons';
import { themes } from '@storybook/theming';

addons.setConfig({
  theme: themes.dark,
});
```

- Editar arquivo `./.storybook/preview.cjs`

```js
import { themes } from '@storybook/theming';

export const parameters = {
  ...,
  docs: {
    theme: themes.dark,
  },
}
```

## 5. CLSX

https://www.npmjs.com/package/clsx

```bash
npm install --save clsx
```

## 6. Radix UI

https://www.radix-ui.com/

https://www.radix-ui.com/docs/primitives/utilities/slot#installation

https://www.radix-ui.com/docs/primitives/components/checkbox

```bash
npm install @radix-ui/react-slot

npm install @radix-ui/react-checkbox
```

## 7. Ícones - Phosphor

https://www.npmjs.com/package/phosphor-react

```bash
npm i phosphor-react
```
