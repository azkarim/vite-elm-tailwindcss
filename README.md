# Vite with Elm and TailwindCSS

## Get Started

`npm install`

`npm run dev`


# Setting up from scratch

## Install Vite + TailwindCss + PostCSS + Autoprefixer

`npm init vite@latest`

`cd [project-name]`

`npm install`

`npm install -D tailwindcss@latest postcss@latest autoprefixer@latest`

`npx tailwindcss init -p`

`npm i -D vite-plugin-elm`

## Add to tailwind.config.js

```
content: ['./index.html', './src/**/*.{js,elm}'],
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

## Add to main.js

```
import { Elm } from '/src/Main.elm'

Elm.Main.init({
  node: document.getElementById('app'),
  flags: ""
})
```


## style.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Main.elm

`mkdir src`

`touch src/Main.elm`

```
module Main exposing (main)

import Html exposing (Html, div, text)
import Html.Attributes exposing (class)


main =
    div [ class "w-screen h-screen bg-blue-100" ]
        [ text "Hello World!" ]

```

## Getting ready to develop

`elm init`

`npm run dev`


