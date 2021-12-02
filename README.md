# Setting up Vite for Elm and TailwindCss

## Install Vite + TailwindCss + PostCSS + Autoprefixer

`npm init vite@latest`
`npm install -D tailwindcss@latest postcss@latest autoprefixer@latest`
`npx tailwindcss init -p`
`npm i -D vite-plugin-elm`

## tailwind.config.js
`touch tailwind.config.js`

```
mode: 'jit,
purge: ['./index.html', '.src/**/*.{js,elm}'],
```

## vite.config.js
`touch vite.config.js`

```
import { defineConfig } from 'vite'
import elmPlugin from 'vite-plugin-elm'

export default defineConfig({
  plugins: [elmPlugin({ debug: true })]
})
```

*Note : change to {debug: false} when you compile for production*

## Getting ready to develop
`git init`
`elm init`
`npm run dev`

