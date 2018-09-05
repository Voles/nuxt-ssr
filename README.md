Nuxt SSR
========

## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

## Deploy

Best to deploy to Surge, which understands the `200.html` file. Used when linking to a nested route.

``` bash
$ npm i -g surge
$ surge dist
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).
