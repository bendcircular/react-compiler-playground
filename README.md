# React 19 Compiler Playground

## How to get started

```
pnpm run dev
```

## Manual steps to setup react compiler

### dependencies

```sh
pnpm install --save react@19.0.0-rc-3f1436cca1-20240516 react-dom@19.0.0-rc-3f1436cca1-20240516
```

### devDependencies 

```sh
pnpm install --save-dev eslint-plugin-react-compiler babel-plugin-react-compiler
```


### Configure the babel plugin

```typescript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react({
    babel: {
      plugins: [["babel-plugin-react-compiler"]]
    }
  })],
})
```