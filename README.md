# Simple SW generator

## Instalation
You can install this repository as a package by running:
```
npm install bobbylej/simple-sw-generator
or
yarn add bobbylej/simple-sw-generator
```

## Use
Add script inside `package.json`
```
"sw": "node sw-generate.js"
```
you can also add there some flags, i.e.
```
"sw": "node sw-generate.js --source ./dist --dist ./dist/service-worker.js"
```
and run it when application is built
```
npm run sw
or
yarn sw
```

## Flags
Options to generator must be specified in the command line.

#### --source

Path to the directory where are stored files from builded application which you want to cache in browser.

default: `./dist/`

#### --dist

Path with filename of generated Service Worker.

default: `./dist/service-worker.js`

#### --template

Path to template file.

default: `./gw-template.js`

#### --cache

Name of the cache store, where you want to save all resources.

default: `your-cache-name`

#### --navigationFallback

Path to fallback file. Important when you have SPA.

default: `index.html`

## Technologies used
Node.js (with libraries `fs`, `minimist` and `glob`), ES6.

I wrote script and template using ES6 as Service Workers are supported only in browsers that also support ES6.
