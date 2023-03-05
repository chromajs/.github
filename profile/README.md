# Chroma

**IMPORTANT: Chroma is still in beta and is not usable yet.**

Chroma is a ridiculously simple framework for integrating Markdown everywhere. You can use it with our own CLI, a vite plugin, and a static compiler and it will compile and markdown in your code to HTML:

```js
document.body.innerHTML = '<chroma># This is **markdown**</chroma>';
// will become
document.body.innerHTML = '<h1>This is <b>markdown</b></h1>';
```

In addition, you can customize the styling with CSS and a specialized `chroma.config.js` file.

## Usage

> We'd recommend using our docs instead: [URL Coming Soon]

You can use Chroma through a CLI (recommended), Vite plugin, or static compiler:

**CLI**
```shell
npm create chroma
npm install
npm run dev
```

**Vite Plugin**
```shell
npm create vite
npm install
npm install vite-plugin-chroma
```
*Inside /vite.config.js*:

ESModules:
```ts
import { defineConfig } from "vite";
import chroma from "vite-plugin-chroma";
export default defineConfig({
    ...
	plugins: [chroma()],
});
```

Common JS:
```js
const { defineConfig } = require("vite");
const chroma = require("vite-plugin-chroma");
export default defineConfig({
    ...
	plugins: [chroma()],
});
```

**Static Compiler**
[Instruction Coming Soon]

## About

Chroma is being built for [SvelteHack](https://hack.sveltesociety.dev/) by two fullstack developers.
