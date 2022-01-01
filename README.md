# REACT FROM SCRATCH

In order to fresh-start any React project (without create-react-app nor prebuilt packages.json), I have made personal blueprint which allows me to utilize latest packages. Most of packages included won't be deprecated nor replaced easily, but in those cases, this document will be updated in a manner of time.

In order to abbreviate repetitive explanations over all internet, every packages mentioned on script will have its own official document link above. If you feel lost in any of those packages, I STRONGLY RECOMMEND to read at least first few pages from its own documentation.

Few of packages are my personal tastes, so feel free to change on your forte.

## init

```sh
mkdir project-name
cd project-name
npm init
```

[Nodejs installation]: https://nodejs.org/en/download/
[Git installation]: https://github.com/git-guides/install-git

## React installation

```ssh
npm i react react-dom
```

[React]: https://en.reactjs.org/docs/react-api.html
[React-DOM]: https://en.reactjs.org/docs/react-dom.html

As those official documents are horrible at explaning each packages, to solely understand what each does I do recommend to check out its own npmjs document.

[React npm]: https://www.npmjs.com/package/react
[React-DOM npm]: https://www.npmjs.com/package/react-dom

## Webpack installation

```sh
npm i --save-dev webpack webpack-cli webpack-dev-server html-webpack-plugin css-loader
```

[webpack]: https://webpack.js.org/
[webpack-cli]: https://github.com/webpack/webpack-cli
webpack-dev-server]: https://github.com/webpack/webpack-dev-server
[html-webpack-plugin]: https://webpack.js.org/plugins/html-webpack-plugin/
[css-loader]: https://webpack.js.org/loaders/css-loader/

## Babel installation

```sh
npm i --save-dev @babel/core @babel/preset-env @babel/preset-react babel-loader
```

[@babel/core]: https://babeljs.io/docs/en/
[@babel/preset-env]: https://babeljs.io/docs/en/babel-preset-env
[@babel/preset-react]: https://babeljs.io/docs/en/babel-preset-react
[babel-loader]: https://github.com/babel/babel-loader

## Typescript installation

```sh
npm i --save-dev typescript @types/react @types/react-dom @babel/preset-typescript ts-loader
```

[typescript]: https://www.typescriptlang.org/
[@types/react]: https://www.npmjs.com/package/@types/react
[@types/react-dom]: https://www.npmjs.com/package/@types/react-dom
[@babel/preset-typescript]: https://babeljs.io/docs/en/babel-preset-typescript
[ts-loader]: https://github.com/TypeStrong/ts-loader

## Configurations

[.babelrc](configs/.babelrc)
[.gitignore](configs/.gitignore)
[tsconfig.json](configs/tsconfig.json)
[webpack.config.js](configs/webpack.config.json)

Generally simple as f. Please read the documentation and customize at your taste.

### Precautions
1. ESNext will allow you to use latest features on your code therefore stick with it.
1. Webpack configurations should assign `entry` and `HtmlWebpackPlugin.template` in order to make it run properly.

## package.json configuration

```json
...
  "scripts": {
    "start": "webpack serve --port 3000",
    "build": "NODE_ENV=production webpack"
  },
...
```

## Updates

- 2021.1.1 Released with React 17 (`^17.0.2`)
