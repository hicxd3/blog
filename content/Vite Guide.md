+++
hidden = true
date = '2025-09-13T18:53:24+03:00'
title = 'Vite full Guide'
draft = true
+++

## Vite One-Page Guide ^-^

This is a complete but short guide for Vite.  
From setup to production — in one single page.

### Setup

Create a new project:

```js
npm create vite@latest
```

Install dependencies:
```js
npm install
```

Run dev server:
```js
npm run dev
```

Optional installs:

React: 
```js
npm install react react-dom
```

TypeScript: 
```js
npm install -D typescript @types/react @types/react-dom
```

Tailwind: 
```js
npm install -D tailwindcss postcss autoprefixer && npx tailwindcss init -p
```

###  Commands

npm run dev — start dev server (default: localhost:5173)

npm run build — build for production

npm run preview — preview build locally

npx vite --host — expose server to local network

npm run dev -- --port=4000 — change port

CTRL + C — stop server

### Plugins

Install with npm and add to vite.config.js

@vitejs/plugin-react — React support

vite-plugin-svgr — import SVG as React components

vite-plugin-pwa — Progressive Web App support

vite-plugin-compression — gzip / brotli compression

vite-plugin-imp — optimize imports

### Config (vite.config.js)

Basic example:

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
  server: {
    port: 3000,
    open: true,
  },
  build: {
    outDir: 'dist',
  },
})
```

### Production

Build project:

```js
npm run build
```

Preview build:

```js
npm run preview
```

Deploy “dist” folder to hosting:

- Vercel (recommended for React/Next)

- Netlify

- GitHub Pages

Key Points ^-^

- Vite = fast dev + simple config
    
- Use plugins to extend functionality
    
- Deploy `dist` folder anywhere